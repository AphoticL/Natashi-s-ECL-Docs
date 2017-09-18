Here are the basic syntaxes you might want to know first before going into the codes.

# formless
Pushes a variable to either the float or integer stack, depending on the type of variable used.

**Examples:**
```ecl
1.0f;		// Pushes a float with the value of 1.0 to the float stack.
6;			// Pushes an int with the value of 6 to the integer stack.
-6;         // Negative values are valid.
-34.355f;	// Same goes to floats.
```
Danmakufu Equivalent: **Absent**; stacks do not exist in dmf.

# []
Pops a variable with the specified order from a stack to be used.

**Examples:**
```ecl
[-1]	    // Pops the topmost variable from the integer stack.
[-2]	    // Pops the second variable from the integer stack.
[-1.0f]     // Pops the topmost variable from the float stack.
[-3.0f]     // Pops the third variable from the float stack.
[-1.6f]     // Invalid.
```
Danmakufu Equivalent: **Absent**; stacks do not exist in dmf.

# anim
Used as a preprocessor, imports *ANM* scripts.

**Examples:**
```ecl
anim{ "enemy.anm"; }
anim{ "enemy.anm"; "st06enm.anm"; }
```
Danmakufu Equivalent: **Absent**

# ecli
Used as a preprocessor, includes *ECL* scripts.

**Examples:**
```ecl
ecli{ "default.ecl"; };
ecli{ "default.ecl"; "st06bs.ecl" };
```
Danmakufu Equivalent: ``#include``

# sub
Defines a *subroutine*. Rounded brackets cannot be omitted. Parameters are defined with only spaces seperating them.

**Examples:**
```ecl
sub Something(){}
sub Something( A B C D E ){}
sub Something( count graphic wait way ){}
```

Danmakufu Equivalent:
```dmf
task Something(){}
task Something(A, B, C, D, E){}
```

# var
Defines local *variables*. Must be present at the start of all subroutines, but does not need to always create a variable.
*Variables* are defined in series, with only spaces seperating them.

**Examples:**
```ecl
var A;
var A B C;
```

Danmakufu Equivalent:
```js
let A;
let A, B, C;
```

# !
Pushes variable(s) to the top of the stack based on difficulty level. (E = easy, N = normal, H = hard, L = lunatic, O = overdrive, * = all difficulties)

**Examples:**
```ecl
!E
	60;
!N
	40;
!HL
	20;
!*
	ins_23([-1]);
```

Danmakufu Equivalent: **Absent**; difficulties aren't hardcoded into dmf.

# xx:

There are two cases:

### When the `xx` is an integer:
Time label, tells the engine to execute the following block of code once an xx amount of **frames** has passed after subroutine activation.

**Examples:**
```ecl
60:		    // 60 frames delay.
3:		    // 3 frames delay.
99999:	    // 99999 frames delay.
-30:	    // Invalid.
20.41:	    // Invalid.
```
Danmakufu Equivalent: **Absent**; labels do not exist in dmf.

### When the `xx` is a string:
Label for jumps and gotos. Label names generated for decompiled ECL scripts are in ``"[Subroutine name]_[Numerical ID]"``.

**Examples:**
```ecl
Boss1_at_239:
WhateverLabelThisIs:
```
Danmakufu Equivalent: **Absent**; labels do not exist in dmf.

# $
Signifies an integer variable.

**Examples:**
```ecl
$A;			// Pushes an integer variable to top of the int stack.
$B = 8;     // Writes an integer to a variable.
```
Danmakufu Equivalent: **Absent**; as stacks and real number types do not exist in dmf.

# %
Signifies an float variable.

**Examples:**
```ecl
%A;			// Pushes a float variable to top of the int stack.
%B = -18.55;     // Writes a float to a variable.
```
Danmakufu Equivalent: **Absent**; as stacks and real number types do not exist in dmf.

# _SS
Passes an integer as an argument of a subroutine.
# _ff
Passes a float as an argument of a subroutine.
# _fS
Converts an integer to a float when passing an argument to a subroutine.
# _Sf
Converts a float to an integer when passing an argument to a subroutine.

# _S
Convert to an integer.

**Examples:**
```ecl
_S(6.0f);	    // Converted to 6.	
_S(89.24f);	    // Converted to 89.
_S(%A);		    // A's value is temporarily converted to an int, but A's actual value remains the same as a float.
```
Danmakufu Equivalent: ``round();``

# _f
Converts to a float.

**Examples:**
```ecl
_f(192);	    // Converted to 192.0f.
_f($A);		    // A's value is temporarily converted to a float, but A's actual value remains the same as an int.
```
Danmakufu Equivalent: ``truncate();``

# [-99xx]
A build-in register that returns an int. An in-depth list can be found [here](registers).

**Examples:**
```ecl
[-9903];
[9903];		    // Invalid.
[-10000];	    // Highest register.
```
# [-99xx.0f]
A build-in register that returns a float. An in-depth list is currently [here](registers).

**Examples:**
```ecl
[-9998.0f];
[9938.0f];	    // Invalid.
```