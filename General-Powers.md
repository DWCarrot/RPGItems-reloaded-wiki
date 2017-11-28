# 通用技能指令集
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
`/rpgitem {item} power aoe {cooldown} {range} {effect} {duration} {amlifier} [selfapplication]`

**效果：**
为 [Item]添加范围效果，冷却时间为 [Cooldown]ticks 右键使用将应用效果 [Effect] 到 [range]# 范围内的所有实体，时长为 [Duration]ticks，效果等级为 [Amplifier]. 如果 [Self] 没有设置，默认此效果也将应用到释放者

**静态成员变量**
- cooldown
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
- Cooldown
  -类型：long
  -设定状态：可选
  -作用：设定技能冷却时间
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
- Cooldown
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
** 指令：**
`/rpgitem {Item} power consume`

** 效果： **
  设置 [Item]为消耗品. 冷却时间默认为0，可通过setter修改。默认右键消耗该物品，可通过setter更改为左键

** 属性： **
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

## Consume
** 指令：**
`/rpgitem testconsume {Item} power consume`

** 效果： **
  设置 [Item]为消耗品. 冷却时间默认为0，可通过setter修改。默认右键消耗该物品，可通过setter更改为左键

** 属性： **
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

## ConsumeHit(后期期望整合入consume)
**指令：**
`/rpgitem {item} power consumehit`

** 效果： **
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
`/rpgitem {item} power deflect [facing] [initiative] [cooldownTime] [passive] [cooldownTimePassive]`

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
`/rpgitem testdeflect  power deflect`

## Fire
** 指令：**
`/rpgitem {Item} power fire {cooldownTime} {distance} {burnduration} `

** 效果： **
  给 {item} 添加火焰技能，能在右键时候发射火焰，并在接触第一个方块时候造成一条距离为{distance}持续时间为{burnduration}火墙，冷却时间 {cooldownTime}ticks. 

** 属性： **
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
** 指令：**
`/rpgitem {Item} power fireball [cooldownTime] `

** 效果： **
  发射小火球 [cooldownTime]tick冷却时间。

** 属性： **
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
** 指令：**
`/rpgitem {Item} power Flame [burnTime] `

** 效果： **
  对目标造成 [burnTime]tick的点燃时间。

** 属性： **
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
** 指令：**
`/rpgitem {Item} power food {foodpoints} `

** 效果： **
   给 {Item} 添加可食用功能, 吃掉时变化 {foodpoints}点饥饿值.

** 属性： **
- foodpoints
  - 类型：int
  - 默认：无
  - 设定状态：必选
  - 作用：变化的饥饿值

**示例**
`/rpgitem testflame power food 10`

## ForceField
** 指令：**
`/rpgitem {Item} power forcefield {cooldownTime} {radius} {height} {base} {ttl}`

** 效果： **
   在你周围设置可以阻止一切实体进入的一个半径 {radius}，高度 {height}，深度 {base} 并持续 {ttl}秒的力场，冷却时间{cooldownTime}tick的由屏障组成的空心圆柱。

** 属性： **
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
** 指令：**
`/rpgitem {Item} power ice [cooldownTime]`

** 效果： **
   给 {Item} 添加冰块射击技能 冷却时间 [cooldownTime]tick. 右键发射冰块, 制造出大量冰块冲击目标, 冰块会慢慢消失

** 属性： **
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

## Knockup
** 指令：**
`/rpgitem {Item} power ice [cooldownTime]`

** 效果： **
   给 {Item} 添加冰块射击技能 冷却时间 [cooldownTime]tick. 右键发射冰块, 制造出大量冰块冲击目标, 冰块会慢慢消失

** 属性： **
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


//TODO