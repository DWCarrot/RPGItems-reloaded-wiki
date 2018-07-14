# 技能(Power)指令集

`/rpgitem {item} power {power} [properties……]`
**属性**
- item：道具id e.g.： testitem->一个id为testitem的道具
- power：技能id  e.g.： potionself->给自己一个buff
- properties
  - 分类：
    - 必选：必须在创建power的时候就指定，用`{}`表示
    - 可选：可以在创建power的时候指定，用`[]`表示
    - 附加：只能通过set设置,不会显示在指令设定的属性中，使用`<>`表示
  - 作用：技能初始化可配参数 e.g.：以上面potionself为例 可配参数有[cooldown] [duration] [amplifier] [effect],整条指令类似这样：`/rpgitem testpotionself power 20 100 1 speed` 右键使用之后给玩家一个持续5秒的等级2的速度buff（cd：1s）。各个参数单位请看下方详细power变量设定。

# 普通技能
## AOE
**指令：**
`/rpgitem {Item} power aoe {cooldown} {range} {effect} {duration} {amlifier} [selfapplication]`

**效果：**
为 [Item]添加范围效果，冷却时间为 [Cooldown]ticks 右键使用将应用效果 [Effect] 到 [range]# 范围内的所有实体，时长为 [Duration]ticks，效果等级为 [Amplifier]. 如果 [Self] 没有设置，默认此效果也将应用到释放者

**属性**
- cooldownTime
  - 类型：long
  - 设定状态：必选
  - 作用：设定技能冷却时间
- range
  - 类型：int
  - 设定状态：必选
  - 作用：设定范围
- effect
  - 类型：String
  - 设定状态：必选
  - 作用：设定效果字符，字符详见 [药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节
- duration
  - 类型：int
  - 设定状态：必选
  - 作用：设定持续时间
- amlifier
  - 类型：int
  - 设定状态：必选
  - 作用：设定技能效果等级，等级=amlifier+1
- selfapplication
  - 类型：boolean
  - 设定状态：可选
  - 作用：是否设定效果作用于自身
- name
  - 类型：String
  - 设定状态：附加
  - 作用: 设定显示名称
- consumption
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
- cooldownTime
  - 类型：long
  - 设定状态：可选
  - 作用：设定技能冷却时间
- consumption
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testarrow power arrow 20`

## Attract
**指令：**  
`/rpgitem {Item} power attract {radius} {maxspeed}`  

**效果：**
为 {Item} 添加技能。拿在手上时将生物拉扯到玩家附近。半径 {radius} 格子，最大速度 {maxspeed}

**属性**  
- radius
  - 类型：int
  - 设定状态：必选
  - 作用：设定技能拉扯最大半径
- maxSpeed
  - 类型：double
  - 设定状态：必选
  - 作用：设定技能最大拉扯速度
**示例**
`/rpgitem testarrow power attract 20 0.1`

## Color 
**指令：**  
`/rpgitem {Item} power color [Cooldown] [glass] [clay] [wool]`  

**效果：**
 改变粘土，玻璃和羊毛的颜色 ([Cooldown] 秒冷却)

**属性**  
- cooldownTime
  - 类型：long
  - 设定状态：可选
  - 作用：设定技能冷却时间
- glass
  - 类型：boolean
  - 设定状态：可选
  - 作用：设定是否作用于玻璃
- clay
  - 类型：boolean
  - 设定状态：可选
  - 作用：设定是否作用于黏土
- wool
  - 类型：boolean
  - 设定状态：可选
  - 作用：设定是否作用于羊毛
- consumption
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testarrow power color 100 true false true`

## Consume
**指令：**
`/rpgitem {Item} power consume`

**效果：**
  设置 [Item]为消耗品. 按键按下后消耗该物品

**属性：**
- cooldownTime
  - 类型：int
  - 设定状态：附加
  - 作用：设定技能冷却时间
- isRight
  - 类型：boolean
  - 设定状态：附加
  - 作用：是否应用为左键
- consumption
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testconsume power consume`

## ConsumeHit
**指令：**
`/rpgitem {Item} power consumehit`

**效果：**
  设置 [Item]为攻击时的消耗品. 冷却时间默认为0，可通过setter修改。

**属性**
- cooldownTime
  - 类型：int
  - 设定状态:附加
  - 作用：设定技能冷却时间

**示例**
`/rpgitem testconsumehit power consumehit`

## Deflect
**指令：**
`/rpgitem {Item} power deflect [facing] [initiative] [cooldownTime] [passive] [cooldownTimePassive]`

**效果：**
  反弹射来的箭与火球（弹反）！

  当参数设定[initiative]为true，[passive]为false并且在技能已经冷却（[cooldownTime]归零）状态下可以根据<isRight>设定左右键触发在[duration]时间内将飞行道具反射到当前玩家正在朝向的方向上

  当参数设定[initiative]为false，[passive]为true的状态下可以在技能触发间隔时间[cooldownTimePassive]归零的状态下有<chance>%的概率将飞行道具反射到当前玩家正在朝向的方向上
  

**属性：**
- facing
  - 类型：double
  - 默认：30
  - 设定状态：可选
  - 作用：最大捕获角度（当前视线与飞行道具之间的夹角）
- initiative
  - 类型：initiative
  - 默认：true
  - 设定状态：可选
  - 作用：主动模式（是否需要主动触发）
- cooldownTime
  - 类型：int
  - 默认：20刻
  - 设定状态：可选
  - 作用：技能冷却时间(当主动模式为true的时候)
- passive
  - 类型：boolean
  - 默认：false
  - 设定状态：可选
  - 作用：是否启用被动模式
- cooldownTimePassive 
  - 类型：int
  - 默认：20刻
  - 设定状态：可选
  - 作用：技能触发间隔时间（被动模式下即passive为true的情况下的触发间隔）
- chance
  - 类型：int
  - 默认：50
  - 设定状态：附加
  - 作用：设定技能在被动模式下触发的几率（<chance>%）
- isRight
  - 类型：boolean
  - 默认：true
  - 设定状态：附加
  - 作用：主动模式下为左键还是右键触发，true为右键
- duration
  - 类型：int
  - 默认：50刻
  - 设定状态：附加
  - 作用：设定主动模式下的弹反有效时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testdeflect power deflect`

## Fire
**指令：**
`/rpgitem {Item} power fire {cooldownTime} {distance} {burnduration} `

**效果：**
  给 {item} 添加火焰技能，能在右键时候发射火焰，并在接触第一个方块时候造成一条距离为{distance}持续时间为{burnduration}火墙，冷却时间 {cooldownTime}ticks. 

**属性：**
- cooldownTime
  - 类型：long
  - 默认：20
  - 设定状态：必选
  - 作用：设定技能冷却时间
- distance
  - 类型：int
  - 类型：15
  - 设定状态：必选
  - 作用：火墙的距离
- burnduration
  - 类型：int
  - 类型：40
  - 设定状态：必选
  - 作用：火墙的持续时间
- consumption
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testfire power fire 10 10 20`


## Fireball
**指令：**
`/rpgitem {Item} power fireball [cooldownTime] `

**效果：**
  发射小火球 [cooldownTime]tick冷却时间。

**属性：**
- cooldownTime
  - 类型：long
  - 默认：20
  - 设定状态：必选
  - 作用：设定技能冷却时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testfire power fireball`

## Flame
**指令：**
`/rpgitem {Item} power Flame [burnTime] `

**效果：**
  对目标造成 [burnTime]tick的点燃时间。

**属性：**
- burnTime
  - 类型：int
  - 默认：20
  - 设定状态：可选
  - 作用：点燃时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testflame power Flame`

## Food
**指令：**
`/rpgitem {Item} power food {foodpoints} `

**效果：**
   给 {Item} 添加可食用功能, 吃掉时变化 {foodpoints}点饥饿值.

**属性：**
- foodpoints
  - 类型：int
  - 默认：无
  - 设定状态：必选
  - 作用：变化的饥饿值

**示例**
`/rpgitem testflame power food 10`

## ForceField
**指令：**
`/rpgitem {Item} power forcefield {cooldownTime} {radius} {height} {base} {ttl}`

**效果：**
   在你周围设置可以阻止一切实体进入的一个半径 {radius}，高度 {height}，深度 {base} 并持续 {ttl}秒的力场，冷却时间{cooldownTime}tick的由屏障组成的空心圆柱。

**属性：**
- cooldownTime
  - 类型：int
  - 默认：200
  - 设定状态：必选
  - 作用：技能冷却时间
- radius
  - 类型：int
  - 默认：5
  - 设定状态：必选
  - 作用：设定圆柱半径
- height
  - 类型:int
  - 默认：30
  - 设定状态：必选
  - 作用：设定圆柱高度
- base
  - 类型：int
  - 默认：-15
  - 设定状态：必选
  - 作用：设定圆柱的深度偏移
- ttl
  - 类型：int
  - 默认：100
  - 设定状态：必选
  - 作用：设定持续时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节


**示例**
`/rpgitem testforcefield power forcefield 10 10 10 0 40`

## Ice
**指令：**
`/rpgitem {Item} power ice [cooldownTime]`

**效果：**
   给 {Item} 添加冰块射击技能 冷却时间 [cooldownTime]tick. 右键发射冰块, 制造出大量冰块冲击目标, 冰块会慢慢消失

**属性：**
- cooldownTime
  - 类型：long
  - 默认：20
  - 设定状态：可选
  - 作用：技能冷却时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节


**示例**
`/rpgitem testice power knockup 10`

## Knockup（失效待修复）
**指令：**
`/rpgitem {Item} power knockup [chance] [power]`

**效果：**
   给 {Item} 添加击飞技能, 几率为 1/[chance] 威力为[power]. 击飞技能会把目标击飞

**属性：**
- chance 
  - 类型：int 
  - 默认：20
  - 设定状态：可选
  - 作用：技能几率
- power
  - 类型：double 
  - 默认：2
  - 设定状态：可选
  - 作用：技能威力
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节


**示例**
`/rpgitem testknockup power knockup`

## LifeSteal
** 指令：**
`/rpgitem {Item} power lifesteal [chance]`

**效果：**
   给 {Item} 添加生命偷取技能, 偷取几率为 [chance]

**属性：**
- chance 
  - 类型：int 
  - 默认：20
  - 设定状态：可选
  - 作用：技能几率
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节


**示例**
`/rpgitem testlifesteal power lifesteal`

## Lightning
**指令：**
`/rpgitem {Item} power lightning [chance]`

**效果：**
   给 {Item} 添加闪电技能, 默认几率为1/[chance]. 攻击目标时一定几率生成闪电

**属性：**
- chance 
  - 类型：int 
  - 默认：20
  - 设定状态：可选
  - 作用：技能几率
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节


**示例**
`/rpgitem testlightning power lifesteal`

## Particle
**指令：**
`/rpgitem {Item} power particle {effect}`

**效果：**
   向 {Item}添加粒子效果. 当右键时，在玩家周围产生粒子。 {effect} 可以是 SMOKE/ENDER_SIGNAL/MOBSPAWNER_FLAMES 之一

**属性：**
- effect 
  - 类型：String
  - 默认：FLAME
  - 设定状态：必填
  - 作用：粒子类型
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节


**示例**
`/rpgitem testparticle power particle FLAME`

## ParticleTick
**指令：**
`/rpgitem {Item} power particletick {effect} [interval]`

**效果：**
  向 {Item} 添加粒子效果. 当持有时，在玩家周围产生粒子。  间隔为[interval]tick。{effect} 可以是 SMOKE/ENDER_SIGNAL/MOBSPAWNER_FLAMES 之一。

**属性：**
- effect 
  - 类型：String
  - 默认：FLAME
  - 设定状态：必填
  - 作用：粒子类型
- interval
  - 类型：int 
  - 默认：15
  - 设定状态：可选
  - 作用：触发间隔时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节


**示例**
`/rpgitem testparticletick power particletick FLAME 20`

## PotionHit
**指令：**
`/rpgitem {Item} power potionhit {chance} {dration} {amplifier} {type}`

**效果：**
  '攻击时有 1/{chance}% 的几率使目标获得药水效果. {type} 为药水效果  {dration}为持续时间单位为游戏刻, {amplifier}
      为整数。 可用药水效果:详见[药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节

**属性：**
- chance 
  - 类型：int
  - 默认：20
  - 设定状态：必填
  - 作用：触发几率
- dration
  - 类型：int
  - 默认：20
  - 设定状态：必填
  - 作用：持续时间
- amplifier
  - 类型：int
  - 默认：1
  - 设定状态：必填
  - 作用：药水效果等级
- type 
  - 类型：String
  - 默认：HARM
  - 设定状态：必填
  - 作用：药水效果：详见[药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testpotionhit power potionhit 1 100 1 speed `

## PotionSelf
**指令：**
`/rpgitem {Item} power potionself {cooldownTime} {duration} {amplifier} {type}`

**效果：**
  右键获得等级{amplifier}的{type}药水效果持续{duration}游戏刻{cooldownTime}游戏刻，冷却时间。 可用药水效果:详见[药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节

**属性：**
- cooldownTime 
  - 类型：long
  - 默认：20
  - 设定状态：必填
  - 作用：冷却时间
- dration
  - 类型：int
  - 默认：20
  - 设定状态：必填
  - 作用：持续时间
- amplifier
  - 类型：int
  - 默认：1
  - 设定状态：必填
  - 作用：药水效果等级
- type 
  - 类型：String
  - 默认：HARM
  - 设定状态：必填
  - 作用：药水效果：详见[药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testpotionself power potionself 100 100 1 speed `

## PotionTick
**指令：**
`/rpgitem {Item} power potiontick {amplifier} {effect} [interval] [duration]`

**效果：**
  持有/穿戴时获得时长为[duration]游戏刻的等级为{amplifier}的{effect}效果并每次经过[interval]游戏刻再次赋予。 可用药水效果:详见[药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节

**属性：**
- amplifier
  - 类型：int
  - 默认：1
  - 设定状态：必填
  - 作用：药水效果等级
- effect
  - 类型：String
  - 默认：SPEED
  - 设定状态：必填
  - 作用：药水效果：详见[药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节
- interval
  - 类型：int
  - 默认：0
  - 设定状态：可选
  - 作用：药水效果循环触发间隔
- duration
  - 类型：int
  - 默认：60
  - 设定状态：可选
  - 作用：药水效果持续时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testpotiontick power potiontick 1 speed `

## Projectile
**指令：**
`/rpgitem {Item} power projectile {cooldownTime} {cone} {projectileType} [range] [amount] [speed]`

**效果：**
{cone}为true： 为 {Item} 添加发射实体技能，冷却时间为{cooldownTime} 游戏刻。右键发射[amount] 个以[speed]速度飞行的 {projectileType}类型的实体。以玩家方向为中心，角度 [range] 呈圆锥形随机分散。可接受的类型：skull, fireball, snowball, smallfireball, arrow, llamaspit

{cone}为false:为 {Item} 添加发射实体技能,冷却时间为{cooldownTime} 游戏刻。右键发射[amount] 个以[speed]速度飞行的 {projectileType}类型的实体。可接受的类型：skull, fireball, snowball, smallfireball, arrow, llamaspit

**属性：**
- cooldownTime
  - 类型：long
  - 默认：20
  - 设定状态：必填
  - 作用：冷却时间
- cone
  - 类型：boolean
  - 默认：false
  - 设定状态：必填
  - 作用：发射区间是否为圆锥型
- projectileType
  - 类型：String
  - 默认：Snowball
  - 设定状态：必填
  - 作用：发射物类型
- range
  - 类型：int
  - 默认：15
  - 设定状态：可选
  - 作用：发射区间角度范围
- amount
  - 类型：int
  - 默认：5
  - 设定状态：可选
  - 作用：发射物数量
- speed
  - 类型：double
  - 默认：1
  - 设定状态：可选
  - 作用：发射物速度
- gravity
  - 类型：boolean
  - 默认：true
  - 设定状态：附加
  - 作用：是否受重力影响
- burstCount
  - 类型：int
  - 默认：1
  - 设定状态：附加
  - 作用：一次释放连续触发的技能次数
- burstInterval
  - 类型：int
  - 默认：1
  - 设定状态：附加
  - 作用：一次释放连续触发的技能时间间隔
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testprojectile power projectile 1 true arrow 10 10 2 `

## Pumpkin
**指令：**
`/rpgitem {Item} power pumpkin {chance} {drop}`

**效果：**
   1/{chance}% 几率使敌人戴上南瓜头，南瓜头有1/{drop}%几率掉落

**属性：**
- chance
  - 类型：int 
  - 默认：20
  - 设定状态：必填
  - 作用：触发几率
- drop
  - 类型：double
  - 默认：0
  - 设定状态：必填
  - 作用：南瓜掉落几率
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testpumpkin power pumpkin 1 1`

## Rainbow
**指令：**
`/rpgitem power {Item} rainbow [cooldownTime] [count] [isFire]`

**效果：**
  给 {Item} 添加彩虹技能,[cooldownTime]为游戏刻. [count]为发射彩色羊毛方块数量. [isFire]为是否发射火焰方块替代羊毛

**属性：**
- cooldownTime
  - 类型：int 
  - 默认：20
  - 设定状态：可选
  - 作用：冷却时间
- count
  - 类型：int
  - 默认：5
  - 设定状态：可选
  - 作用：发射数量
- isFire
  - 类型：boolean
  - 默认：false
  - 设定状态：可选
  - 作用：是否替换发射物为火焰
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testpumpkin power rainbow`

## RealDamage
**指令：**
`/rpgitem{Item}  power realdamage {cooldownTime} {realDamage}`

**效果：**
  给 {Item} 添加真实伤害技能, {cooldownTime}为游戏刻. 被击中的生物将受到{realDamage}真实伤害但至少会剩<minDamage>点生命值.

**属性：**
- cooldownTime
  - 类型：int 
  - 默认：20
  - 设定状态：必填
  - 作用：冷却时间
- realDamage
  - 类型：double
  - 默认：0
  - 设定状态：必填
  - 作用：真实伤害数值
- minDamage
  - 类型：double
  - 默认：0
  - 设定状态：附加
  - 作用：目标最小残留血量
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testrealdamage power realdamage 1 10`

## Rescue
**指令：**
`/rpgitem {Item} power rescue [cooldownTime] [healthTrigger] [useBed] [inPlace]`

**效果：**
  给 {Item} 添加拯救技能，冷却时间为[cooldownTime]游戏刻，在玩家血量低于[healthTrigger]触发，[useBed]为true的时候拯救传送回出身点，[inPlace]为true的时候原地复活并无敌。优先级[inPlace]>[useBed]

**属性：**
- cooldownTime
  - 类型：int 
  - 默认：20
  - 设定状态：可选
  - 作用：冷却时间
- healthTrigger
  - 类型：int
  - 默认：4
  - 设定状态：可选
  - 作用：拯救触发最小血量
- useBed
  - 类型：boolean
  - 默认：true
  - 设定状态：可选
  - 作用：是否传送回出身点
- inPlace
  - 类型：boolean
  - 默认：false
  - 设定状态：可选
  - 作用：是否原地复活
- damageTrigger
  - 类型：double
  - 默认：1024
  - 设定状态：附加
  - 作用：多少伤害以上触发
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testrescue power rescue`

## Rumble
**指令：**
`/rpgitem {Item} power rumble {cooldownTime} {power} {distance}`

**效果：**
  给 {Item} 添加添加土遁技能，冷却时间为{cooldownTime},有效推进范围为{distance}，将土遁推进范围内触碰到的第一个实体周围产生爆炸并将周围小范围内的相同实体以{power}的击飞等级击飞上天

**属性：**
- cooldownTime
  - 类型：int 
  - 默认：20
  - 设定状态：必填
  - 作用：冷却时间
- power
  - 类型：int
  - 默认：2
  - 设定状态：必填
  - 作用：击飞等级
- distance
  - 类型：int
  - 默认：15
  - 设定状态：必填
  - 作用：推进距离
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testrumble power rumble 100 4 10`

##Repair
**指令：**
`/rpgitem {item} power repair {durability} {material} {display} {isRight} {isSneak}`

**效果：**
 给{item}添加修复技能，携带对应的{material}的时候可以在设定是否左右键{isRight}之后点击对应的按键并是否需要点击shift（{isSneak}）情况下进行消耗/增加{durability}数值的耐久

**属性：**
- durability
  - 类型：int
  - 默认：20
  - 设定状态：必填
  - 作用：设定耐久值
- material
  - 类型：Srting
  - 默认：无
  - 设定状态：必填
  - 作用：设定消费物品
- display
  - 类型：String
  - 默认：无
  - 设定状态：必填
  - 作用：设定技能显示名字
- isRight
  - 类型：Boolean
  - 默认：true
  - 设定状态：必填
  - 作用：是否要使用右键
- isSneak
  - 类型：Boolean
  - 默认：false
  -设定状态：必填
  -作用：是否要按shift

**示例**
`/rpgitem testrepair power repair 10 DIAMOND repair right false`


## SkyHook
**指令：**
`/rpgitem {Item} power skyhook {railMaterial} {hookDistance}`

**效果：**
 给 {Item}添加天钩技能. 天钩技能允许使用者钩到{hookDistance}距离以内的指定{railMaterial}材质方块并向那个方向突进

**属性：**
- railMaterial
  - 类型：String 
  - 默认：无
  - 设定状态：必填
  - 作用：可以指向的材质id
- hookDistance
  - 类型：int 
  - 默认：10
  - 设定状态：必填
  - 作用：改材质方块距离玩家的最小距离
- cooldownTime
  - 类型：int 
  - 默认：20
  - 设定状态：必填
  - 作用：冷却时间
- hookingTickCost
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：每次勾取过程中飞行1游戏刻的消耗量
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testskyhook power  skyhook 1 10`

## TNTCannon
**指令：**
`/rpgitem {Item} power tntcannon [cooldownTime]`

**效果：**
 给 {Item}添加发射tnt的功能，冷却时间为[cooldownTime]

**属性：**
- cooldownTime
  - 类型：long 
  - 默认：20
  - 设定状态：可选
  - 作用：冷却时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testtntcannon power tntcannon`

## Teleport
**指令：**
`/rpgitem {Item} power teleport [cooldownTime] [distance]`

**效果：**
 给{Item}添加传送技能, 冷却时间[cooldownTime]游戏刻 右键传送距离为[distance]格. 传送方向为你所面向的方向

**feture**
 这个技能当载体的材质为弓箭的时候，会变成传送到射出去的箭矢落地的位置，并且若弓箭落地的位置和玩家的距离大于[distance]会提示太远了

**属性：**
- cooldownTime
  - 类型：long 
  - 默认：20
  - 设定状态：可选
  - 作用：冷却时间
- distance
  - 类型：int 
  - 默认：5
  - 设定状态：可选
  - 作用：传送距离
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testteleport power teleport 20 10`

## TippedArrow
**指令：**
`/rpgitem {Item} power tippedarrow {cooldownTime} {type} {duration} {amplifier} `

**效果：**
 给 {Item} 添加药箭技能, 效果{type}时长{duration}为游戏刻, 等级为{amplifier},冷却时间{cooldownTime}游戏刻. 右键发射. 有效的药水效果：详见[药水系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C)章节

**属性：**
- cooldownTime
  - 类型：long 
  - 默认：20
  - 设定状态：必选
  - 作用：冷却时间
- type
  - 类型：String 
  - 默认：null
  - 设定状态：必选
  - 作用：药水效果类型
- duration
  - 类型：int 
  - 默认：15
  - 设定状态：必选
  - 作用：持续时间
- amplifier
  - 类型：int 
  - 默认：1
  - 设定状态：必选
  - 作用：效果等级
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testtippedarrow power tippedarrow 20 speed 40 1`

## Torch
**指令：**
`/rpgitem {Item} power torch {cooldownTime}`

**效果：**
 给 {Item} 添加照亮技能，冷却时间为{cooldownTime}，对着指向的区域扔一堆火把，火把会投掷到对应的方块上

**属性：**
- cooldownTime
  - 类型：long 
  - 默认：20
  - 设定状态：必选
  - 作用：冷却时间
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testtorch power torch 20`

## Throw
**指令：**
`/rpgitem {Item} power throw {display} {cooldownTime} {left/right} {speed} {entity} [entityData]`

**效果：**
为 {Item} 添加发射实体技能，冷却时间为{cooldownTime} 游戏刻。{left/right}键发射以{speed}速度飞行的 {entity}，并付带 [entityData]

**属性：**
- display
  - 类型：string
  - 默认: 空
  - 设定状态：必填
  - 作用： power 在 lore 中的展示字符
- cooldownTime
  - 类型：long
  - 默认：20
  - 设定状态：必填
  - 作用：冷却时间
- left/right
  - 类型：String
  - 默认：right
  - 设定状态：必填
  - 作用：左右键触发
- speed
  - 类型：double
  - 默认：1
  - 设定状态：必填
  - 作用：发射物速度
- entity
  - 类型：string
  - 默认：空
  - 设定状态：必填
  - 作用：设置发射的实体
- entityData
  - 类型：string (json)
  - 默认：空 `{}`
  - 设定状态：必填
  - 作用：设置发射的实体 entityData
- consumption
  - 类型：int
  - 默认：0
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
`/rpgitem testthrow power throw ThrowCreeper 20 right 2 creeper {ignited:1,Fuse:5}`

# 特殊技能（command系列）

## aoecommand

**指令：**
`/rpgitem {Item} power aoecommand {cooldown} {isRight} {display} {command} {rm} {r} {facing} [permission]`

**效果：**
给 {Item}添加AOE指令技能, 冷却时间为 {cooldown}. 若{isRight}为right则右键触发否则为left左键触发，工具提示为 {display}. {command}会在{isRight}后对范围({rm} ~ {r} 在 {facing} 视角)内的实体运行 并需要给对应角色运行此{command}的 {permission}

**属性**
- cooldownTime
  - 类型：long
  - 设定状态：必选
  - 作用：设定技能冷却时间
- isRight
  - 类型：left/right
  - 设定状态：必选
  - 作用：设定左键或者右键
- display
  - 类型：string
  - 设定状态：必选
  - 作用：设定技能描述字符
- command
  - 类型：string
  - 设定状态：必选
  - 作用：设定技能触发时的指令（可为任何minecraft指令方块或者聊天框中输入的可执行指令）
  - 特殊转换：可在指令中替换成某些特殊数值的固定字符串
    - 使用者：
      - `{player}` : 可转换为当前使用者名字
      - `{player.x}`: 可转换为当前使用者的x坐标
      - `{player.y}`: 可转换为当前使用者的y坐标
      - `{player.z}`: 可转换为当前使用者的z坐标
      - `{player.yaw}`: 可转换为当前使用者视线水平转角
      - `{player.pitch}`: 可转换喂当前使用者的视线仰角
    - 被执行者：
      - `{entity}`: 每个被执行者的名字（注意是名字例如是僵尸，那就叫`僵尸`）
      - `{entity.x}` : 每个被执行者的x坐标
      - `{entity.y}` : 每个被执行者的y坐标
      - `{entity.z}` : 每个被执行者的z坐标
      - `{entity.yaw}` : 每个被执行者的视线水平转角
      - `{entity.pitch}` : 每个被执行者的视线仰角
      - `{entity.uuid}` : 每个被执行者的uuid
    - #### 转换不支持运算，例如`{player.yaw}+90`不可行
- rm
  - 类型：int
  - 默认：0
  - 设定状态：必选
  - 作用：索敌范围的最小半径
- r
  - 类型：int
  - 默认：10
  - 设定状态：必选
  - 作用：索敌范围的最大半径
- facing
  - 类型：int
  - 默认：30
  - 设定状态：必选
  - 作用:使用者当前视线偏转角度（圆锥型范围）
- permission
  - 类型：string
  - 设定状态：可选
  - 作用：使用者执行{command}时候需要的权限节点（仅支持单节点，多节点不支持，为`*`的话就是赋予op权限）
- c
  - 类型：int
  - 设定状态：附加
  - 默认：100
  - 作用：设定最大捕获的被执行者数量
- mustsee
  - 类型：boolean
  - 设定状态：附加
  - 默认：false
  - 作用：只适用于被玩家视线看到的实体
- selfapplication
  - 类型：boolean
  - 设定状态：附加
  - 默认：false
  - 作用：指令是否作用于使用者本身
- type
  - 类型：entity/player/mobs
  - 设定状态：附加
  - 默认：entity
  - 作用：指令作用者类型
- consumption
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
```
/rpgitem testaoecommand power aoecommand 20 right `say hello` `/say {entity} hello` 0 20 360 minecraft.command.say
```
**效果**：让使用者为中心0-20范围内的所有LivingEntity类型的实体说一声：(实体名字) hello。

**注释1**：注意这个指令的使用者是使用者本人，如果使用相对位置 `~` 符号的话也只是根据使用者当前位置进行计算而非每个被执行者的位置。并且执行指令的次数为当前技能捕获到的被执行者的个数相同。

**注释2**：有些指令（例如`execute`）拥有可以越权的权限，需要特别注意。


## command

**指令：**
`/rpgitem {Item} power command {cooldown} {isRight} {display} {command} [permission]`

**效果：**
给 {Item} 添加指令技能, 冷却时间为 {cooldown}. 工具提示为{display}. {command}  会在 {isRight}（left/right）后运行, 并给予运行此  {command} 的 [permission]. ***注意***: 如果你想在 {display} 或 {command} 或 [permission] 打空格, 那么要在字符串周围加 `符号. 例如: `/say Hello`'

- cooldownTime
  - 类型：long
  - 设定状态：必选
  - 作用：设定技能冷却时间
- isRight
  - 类型：left/right
  - 设定状态：必选
  - 作用：设定左键或者右键
- display
  - 类型：string
  - 设定状态：必选
  - 作用：设定技能描述字符
- command
  - 类型：string
  - 设定状态：必选
  - 作用：设定技能触发时的指令（可为任何minecraft指令方块或者聊天框中输入的可执行指令）
  - 特殊转换：可在指令中替换成某些特殊数值的固定字符串
    - 使用者：
      - `{player}` : 可转换为当前使用者名字
      - `{yaw}`: 可转换为当前使用者视线水平转角
      - `{pitch}`: 可转换喂当前使用者的视线仰角
    - #### 转换不支持运算，例如`{yaw}+90`不可行
- consumption
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
```
/rpgitem testcommand power command 20 right `say hello` `/say hello` minecraft.command.say
```
**效果**：让使用者在聊天频道打出hello。

**注释**：有些指令（例如`execute`）拥有可以越权的权限，需要特别注意。

## commandhit

**指令：**
`/rpgitem {Item} power commandhit {cooldown} {display} {command} [permission]`

**效果：**
给 {Item} 添加击中指令技能. 冷却时间为 {cooldown}. 工具提示为 {display} . {command} 会在击中目标后执行,并给予运行{command} 的 [permission]. 
***注意***: 如果你想在 {display} 或 {command} 或 [permission] 输入空格, 那么要在字符串周围加`符号. 例如: `/say Hello`'
- cooldownTime
  - 类型：long
  - 设定状态：必选
  - 作用：设定技能冷却时间
- isRight
  - 类型：left/right
  - 设定状态：必选
  - 作用：设定左键或者右键
- display
  - 类型：string
  - 设定状态：必选
  - 作用：设定技能描述字符
- command
  - 类型：string
  - 设定状态：必选
  - 作用：设定技能触发时的指令（可为任何minecraft指令方块或者聊天框中输入的可执行指令）
  - 特殊转换：可在指令中替换成某些特殊数值的固定字符串
    - 使用者：
      - `{player}` : 可转换为当前使用者名字
      - `{player.x}`: 可转换为当前使用者的x坐标
      - `{player.y}`: 可转换为当前使用者的y坐标
      - `{player.z}`: 可转换为当前使用者的z坐标
      - `{player.yaw}`: 可转换为当前使用者视线水平转角
      - `{player.pitch}`: 可转换喂当前使用者的视线仰角
    - 被执行者：
      - `{entity}`: 每个被执行者的名字（注意是名字例如是僵尸，那就叫`僵尸`）
      - `{entity.x}` : 每个被执行者的x坐标
      - `{entity.y}` : 每个被执行者的y坐标
      - `{entity.z}` : 每个被执行者的z坐标
      - `{entity.yaw}` : 每个被执行者的视线水平转角
      - `{entity.pitch}` : 每个被执行者的视线仰角
      - `{entity.uuid}` : 每个被执行者的uuid
    - #### 转换不支持运算，例如`{player.yaw}+90`不可行
- minDamage
  - 类型:int
  - 设定状态：附加
  - 默认：0
  - 作用：最小触发伤害
- consumption
  - 类型：int
  - 设定状态：附加
  - 作用：消耗量，详见 [新消耗系统](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system)章节

**示例**
```
/rpgitem testcommandhit power commandhit 20 `say hello` `/say {entity} hello` minecraft.command.say
```
**效果**：让使用者在聊天频道里向被攻击者打出hello。

**注释**：有些指令（例如`execute`）拥有可以越权的权限，需要特别注意。
