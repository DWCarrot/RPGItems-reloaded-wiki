# 指令集
`/rpgitem {item} power {power} [attributes……]`
**属性**
- item：道具id e.g.： testitem->一个id为testitem的道具
- power：技能id  e.g.： potionself->给自己一个buff
- attributes：
  - 分类：
    - 必选：必须在创建power的时候就指定，用`{}`表示
    - 可选：可以在创建power的时候指定，用`[]`表示
    - 附加：只能通过set设置,不会显示在指令设定的属性中
  - 作用：技能初始化可配参数 e.g.：以上面potionself为例 可配参数有[cooldown] [duration] [amplifier] [effect],整条指令类似这样：`/rpgitem testpotionself power 20 100 1 speed` 右键使用之后给玩家一个持续5秒的等级2的速度buff（cd：1s）。各个参数单位请看下方详细power变量设定。

# 普通技能
## AOE
**指令：**
`/rpgitem {item} power aoe {cooldown} {range} {effect} {duration} {amlifier} [selfapplication]`

**效果：**
为 [Item]添加范围效果，冷却时间为 [Cooldown]ticks 右键使用将应用效果 [Effect] 到 [range]# 范围内的所有实体，时长为 [Duration]ticks，效果等级为 [Amplifier]. 如果 [Self] 没有设置，默认此效果也将应用到释放者

**静态成员变量**
- cooldown：
  - 类型：long
  - 设定状态：必选
  - 作用：设定技能冷却时间
- range：
  - 类型：int
  - 设定状态：必选
  - 作用：设定范围
- effect：
  - 类型：String
  - 设定状态：必选
  - 作用：设定效果字符，字符详见 [药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节
- duration:
  - 类型：int
  - 设定状态：必选
  - 作用：设定持续时间
- amlifier：
  - 类型：int
  - 设定状态：必选
  - 作用：设定技能效果等级，等级=amlifier+1
- selfapplication：
  - 类型：boolean
  - 设定状态：可选
  - 作用：是否设定效果作用于自身
- name：
  - 类型：String
  - 设定状态：附加
  - 作用: 设定显示名称
- consumption：
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testaoe power aoe 10 10 speed 100 0 true`



## Arrow 
**指令：**  
`/rpgitem {Item} power arrow [Cooldown]`  

**效果：**
给 [Item] 添加火箭技能, 冷却时间 [Cooldown]ticks. 右键发射

**属性**  
- Cooldown: 
  -类型：long
  -设定状态：可选
  -作用：设定技能冷却时间
- consumption：
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testarrow power arrow 20`

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