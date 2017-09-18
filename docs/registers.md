Here is the list of known ECL Registers

# [-9903] 
Supported in: Hidden Star in Four Seasons (**16**)

Returns the type of seasonal subshot the player is using. 

(**0** = **Spring**, **1** = **Summer**, **2** = **Fall**, **3** = **Winter**)


# [-9913] 
Supported in: Double Spoiler (**12.5**)

Returns number of photos taken.
		

# [-9915.0f] ~ [-9922.0f]
Global float, free for reading and writing.


# [-9923] ~ [-9926]
Global int, free for reading and writing.


# [-9930]
Returns current power level.

Danmakufu Equilavent: ``GetPlayerPower();``


# [-9932.0f] ~ [-9935.0f]
Local float, free for reading and writing.


# [-9936.0f] ~ [-9939.0f], [-9940] ~ [-9943]
Local boss variables, free for reading and writing.

# [-9944.0f]

Returns distance from the unit to the player.

Danmakufu Equivalent: ``GetObjectDistance(unit, GetPlayerObjectID());``

# [-9945]

Returns Player Type

# [-9946]

Returns current number of active units on-screen.

Danmakufu Equivalent: ``length(GetAllEnemyID());``

# [-9947]

Returns whether the player has lost a life or used a bomb in an attack. Returns 0 Either a life has been lost or a bomb has been used, returns 1 otherwise.

*Must be manually reset.*
			
Danmakufu Equivalent: ``ObjEnemyBossScene_GetInfo(scene, INFO_PLAYER_SPELL_COUNT);`` *or* ``ObjEnemyBossScene_GetInfo(scene, INFO_PLAYER_SHOOTDOWN_COUNT);``

# [-9948]
Returns number of bombs used.

*Must be manually reset.*

Danmakufu Equivalent: ``ObjEnemyBossScene_GetInfo(scene, INFO_PLAYER_SPELL_COUNT);``

#[-9949]

Returns number of lives lost. 

*Must be manually reset.*

Danmakufu Equivalent: ``ObjEnemyBossScene_GetInfo(scene, INFO_PLAYER_SHOOTDOWN_COUNT);``
		
# [-9950]

Returns 1 when the difficulty is **Lunatic**, 0 otherwise.

# [-9951]

Returns 1 when the difficulty is **Hard**, 0 otherwise.

# [-9952]

Returns 1 when the difficulty is **Normal**, 0 otherwise.

# [-9953]

Returns 1 when the difficulty is **Easy**, 0 otherwise.

# [-9954]

Current life of a unit.

Danmakufu Equivalent: ``ObjEnemy_GetInfo(unit, INFO_LIFE);``
		
# [-9955.0f]

Returns angle of a unit to the player.

Danmakufu Equivalent: ``GetAngleToPlayer(unit);``

# [-9956.0f]

Returns absolute angle of a unit to the player.

Danmakufu Equivalent: ``GetAngleToPlayer(unit);``

# [-9958.0f]

Movement angle of a unit. 0 is returned if the unit is not moving.

Danmakufu Equivalent: ``ObjMove_GetAngle(unit);``
		
# [-9959]

Returns difficulty level. 

(**0** = **Easy**, **1** = **Normal**, **2** = **Hard**, **3** = **Lunatic**)

# [-9960]

Returns the current rank(?).

# [-9962.0f]

Return unit's Y position.

Danmakufu Equivalent: ``ObjMove_GetY(unit);``

# [-9963.0f]

Return Unit's X position.

Danmakufu Equivalent: ``ObjMove_GetX(unit);``

# [-9964.0f]

Returns the Player's Y position.

Danmakufu Equivalent: ``GetPlayerY();``

# [-9965.0f]

Returns the Player's X position.

Danmakufu Equivalent: ``GetPlayerX();``
		
# [-9971.0f]

Movement angle of a unit. 0 is returned if the unit is not moving.

Danmakufu Equivalent: ``ObjMove_GetAngle(unit);``
			
# [-9979.0f] ~ [-9981.0f]

Local unit float, free for reading and writing. Shared across all subroutines created by the unit.
		
# [-9982] ~ [-9985]

Local unit int, free for reading and writing. Shared across all subroutines created by the unit.
		
# [-9986]

Returns 0 if the previous attack has been timed out, 1 otherwise.

Danmakufu Equivalent: ``ObjEnemyBossScene_GetInfo(scene, INFO_TIMERF) <= 0;``
		
# [-9987.0f]

Random float between -1.0f and 1.0f.

Danmakufu Equivalent: ``rand(-1,1);``
			
# [-9988]

Amount of time passed in frames.

Danmakufu Equivalent: ``ObjEnemyBossScene_GetInfo(scene, INFO_ORGTIMERF) - ObjEnemyBossScene_GetInfo(scene, INFO_TIMERF);``
			
# [-9989.0f]

Angle of a unit to the player.

Danmakufu Equivalent: ``GetAngleToPlayer(unit);``
		
# [-9990.0f]

Player's Y position.

Danmakufu Equivalent: ``GetPlayerY();``

# [-9991.0f]

Player's X position.

Danmakufu Equivalent: ``GetPlayerX();``

# [-9992.0f]

Unit's Y position relative to the player.

Danmakufu Equivalent: ``ObjMove_GetY(unit) - GetPlayerY;``

# [-9993.0f]

Unit's X position relative to the player.

Danmakufu Equivalent: ``ObjMove_GetX(unit) - GetPlayerX;``

# [-9994.0f]

Unit's Y position.

Danmakufu Equivalent: ``ObjMove_GetY(unit);``

# [-9995.0f]

Unit's X position.

Danmakufu Equivalent: ``ObjMove_GetX(unit);``

# [-9996.0f]

Unit's Y position.

Danmakufu Equivalent: ``ObjMove_GetY(unit);``

# [-9997.0f]

Unit's X position.

Danmakufu Equivalent: ``ObjMove_GetX(unit);``

			
# [-9998.0f]

Random float between ``-3.1415926535.0f`` and ``3.1415926535.0f``.

# [-9999.0f]

Random float between ``0.0f`` and ``1.0f``.

# [-10000]

Random int.
