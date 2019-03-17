# 技能：粒子屏障

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:particlebarrier`

来源插件：`RPGItems`

默认触发：RIGHT_CLICK, TICK。
可用触发：ATTACHMENT, LEFT_CLICK, OFFHAND_CLICK, RIGHT_CLICK, SNEAK, SPRINT, TICK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

将受到的攻击转化为效果
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* energyDecay

  * 类型：double
  * 默认：1.5

  能量每秒的衰减

* triggers

  * 类型：Set&lt;Trigger&gt;
  * 默认：RIGHT_CLICK,TICK

  技能的触发。

* projected

  * 类型：boolean
  * 默认：false

  是否为投射屏障

* energyPerBarrier

  * 类型：double
  * 默认：40.0

  满盾能提供的能量

* energyPerLevel

  * 类型：double
  * 默认：10.0

  每级力量效果所需要的能量

* effect

  * 类型：PotionEffectType
  * 默认：INCREASE_DAMAGE

  屏障的效果

* cooldown

  * 类型：int
  * 默认：20

  技能的冷却时间，以游戏刻为单位。

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

* barrierHealth

  * 类型：double
  * 默认：40.0

  满盾的生命值

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->