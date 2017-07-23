## Arrow 
**Command:**  
`/rpgitem [Item] power arrow [Cooldown]`  
**Variables:**  
- Cooldown: integer, default 20 ticks
  
**Effect:**  
Fires an arrow on right click.  

## Command 
**Command:**  
Version 1:  
`/rpgitem [Item] power command [Cooldown] [left/right] [Display] [Command] [Permission]`  
Version 2:  
`/rpgitem [Item] power command [Cooldown] [left/right] [Arguments]`  
**Variables:**  
Version 1:  
- Cooldown: integer, no default  

- Display: string, sets tooltip display, no default  

- Command: string, no default  

- Permission: string, default none 

Version 2:
- Arguments: string, | seperated list of display,command, and permission variables from version 1  

**Effect:**  
Runs specified command on left/right click, gives set permission for the command if a permission is set.  

You can use some template in command string. e.g. `{player}` for the player using the item.
Templates supported now:
* `player` player's name
* `yaw` player's eye's yaw, Decimal
* `pitch` player's eye's pitch， Decimal

## CommandHit
**Command:**  
`/rpgitem [Item] power commandhit [Cooldown] [Display] [Command] [Permission]`  
**Variables:**  
- Cooldown: integer, no default  

- Display: string, sets tooltip display, no default  

- Command: string, no default  

- Permission: string, default none 

**Effect:**  
Runs specified command when player hits a LivingEntity, gives set permission for the command if a permission is set.  

You can use some template in command string. e.g. `{player}` for the player using the item.
Templates supported now:
* `entity` entity's name
* `entity.uuid` entity's UUID
* `entity.x` entity's X coordinate, integral
* `entity.y` entity's Y coordinate, integral
* `entity.z` entity's Z coordinate, integral
* `entity.yaw` entity's eye's yaw, Decimal
* `entity.pitch` entity's eye's pitch， Decimal
* `player` player's name
* `player.x` player's X coordinate, integral
* `player.y` player's Y coordinate, integral
* `player.z` player's Z coordinate, integral
* `player.yaw` player's eye's yaw, Decimal
* `player.pitch` player's eye's pitch， Decimal

## Consume 
**Command:**  
 `/rpgitem [Item] power consume`  
**No variables**  
**Effect:**  
Removes the item on right click.
## Fire
**Command:**  
`/rpgitem [Item] power fire [Cooldown] [Distance] [Burnduration]`  
**Variables:**  
- Cooldown: integer, in ticks, no default 
- Distance: integer, in blocks, no default
- Burnduration: integer, in ticks, no default

**Effects:**  
Shoots fire on right click. 
## Fireball 
**Command:**  
`/rpgitem [Item] power fireball [Cooldown]`  
**Variables:**  
- Cooldown: integer, default 20 ticks  

**Effects:**  
Fires a fireball on right click.  
## Flame ##
**Command:**  
`/rpgitem [Item] power flame [Burntime]`  
**Variables:**  
- Burntime: integer, in ticks, default 20 ticks     

**Effect:**   
Sets the target on fire on hit.  
## Food 
**Command:**  
`/rpgitem [Item] power food [Food Points]`  
**Variables:**  
- Food Points: integer, default 5 food points
  
**Effect:**  
Consumes the item and adds [Food Points] food points to the player. (As if we they food).
## Ice ##
**Command:**  
`/rpgitem [Item] power ice [Cooldown]`  
**Variables:**  
- Cooldown: integer, default 20 ticks 
 
**Effect:**  
Fires an ice block on right click which will then create a box of ice on impact, the ice will slowly remove itself.  
## Knockup ##
**Command:**  
`/rpgitem [Item] power knockup [Chance] [Power]`  
**Variables:**
- Chance: integer, default 20
- Power: double, default 2  

**Effect**  
Chance 1/`[Chance]`, that the hit will send the target flying.  
## Lightning ##
**Command:**  
`/rpgitem [Item] power lightning [Chance]`  
**Variables:**  
- Chance: integer, default 2O  

**Effect:**  
Chance 1/`[Chance]`, that the hit will summon a lightning upon the target.  
## Potion Hit ##
**Command:**  
`/rpgitem [Item] power potionhit [Chance] [Duration] [Amplifier] [Effect]`  
**Variables:**  
- Chance: integer, no default  
- Duration: integer, no default, in ticks  
- Amplifier: integer, no default, level of the effect
- Effect: string, no default, [possible effects](https://github.com/TheCreeperOfRedstone/RPG-Items-2/wiki/Potion-Effects)  

**Effect:**  
Applies potion effect with chance 1/`[Chance]`.
## Potion Self ##
**Command:**  
`/rpgitem [Item] power potionself [Cooldown] [Duration] [Amplifier] [Effect]`  
**Variables:**  
- Cooldown: integer, in ticks, no default  
- Duration: integer, no default, in ticks  
- Amplifier: integer, no default, level of the effect  
- Effect: string, no default, [possible effects](https://github.com/TheCreeperOfRedstone/RPG-Items-2/wiki/Potion-Effects)  

**Effect:**  
Applies potion effect on right click.
## Potion Tick ##
**Command:**  
`/rpgitem [Item] power potiontick [Amplifier] [Effect]`  
**Variables:**  
- Amplifier: integer, no default, level of the effect  
- Effect: string, no default, [possible effects](https://github.com/TheCreeperOfRedstone/RPG-Items-2/wiki/Potion-Effects) 

**Effect:**  
Gives the wielder the specified potion effect.
## Rainbow ##
**Command:**  
`/rpgitem [Item] power rainbow [Cooldown] [Count]`  
**Variables:**  
- Cooldown: integer, in ticks, default 20 ticks  
- Count: integer, number of blocks, default 5  

**Effect:**  
Fires blocks of coloured wool on right click, the wool will remove itself.  
## Rumble ##
**Command:**  
`/rpgitem [Item] power rumble [Cooldown] [Power] [Distance]`  
**Variables:**  
- Cooldown: integer, in ticks, no default   
- Power: integer, no default  
- Distance: integer, no default, how far the wave travels  

**Effect:**  
Sends a shockwave through the ground and sends any hit entities flying.  
## Skyhook ##
**Command**  
`/rpgitem [Item] power skyhook [Material] [Distance]`  
**Variables:**  
- Material: string, name of the material the skyhook will attach to, no default   
- Distance: integer, no default  

**Effect:**  
Hooks onto set material, similar to Bishock's skyhook.  
## Teleport ##
**Command:**  
`/rpgitem [Item] power teleport [Cooldown] [Distance]`  
**Variables:**  
- Cooldown: integer, in ticks, default 20 ticks  
- Distance: integer, how many blocks to teleport, default 5 blocks  

**Effect:**  
Teleports the player in the direction that it's are looking at.  

## Tipped Arrow 
**Command:**  
`/rpgitem [Item] power tippedarrow [Cooldown] [Effect] [Duration] [Amplifier]`  
**Variables:**  
- Cooldown: integer,no default
- Effect: string, no default, [possible effects](https://github.com/TheCreeperOfRedstone/RPG-Items-2/wiki/Potion-Effects)  
- Duration: integer, no default, in ticks  
- Amplifier: integer, no default, level of the effect  

**Effect:**  
Fires an tipped arrow with specified effect on right click.  

## TNT Cannon ##
**Command:**  
`/rpgitem [Item] power tntcannon [Cooldown]`  
**Variables:**  
- Cooldown: integer, in ticks, default 20 ticks 

**Effect:**  
Fires active TNT on right click.
## Torch ##
**Command:**  
`/rpgitem [Item] power torch [Cooldown]`  
**Variables:**  
- Cooldown: integer, in ticks, no default

**Effect:**  
Shoots torches on right click.