# 技能：吸引

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:attract

来源插件：RPGItems

默认触发：RIGHT_CLICK。 可用触发：TICK, RIGHT_CLICK, SPRINT, OFFHAND_CLICK, LEFT_CLICK, ATTACHMENT, SNEAK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

吸引附近的怪物到玩家
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* attractingTickCost

  * 类型：int
  * 默认：0

  吸引时每刻的耐久消耗。

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* maxSpeed

  * 类型：double
  * 默认：0.4

  最大速度。

* triggers

  * 类型：Set&lt;Trigger&gt;
  * 默认：RIGHT_CLICK

  技能的触发。

* selectors

  * 类型：Set&lt;String&gt;

  应用到本技能的选择器。

* duration

  * 类型：int
  * 默认：5

  主动触发的持续时间。

* attractPlayer

  * 类型：boolean
  * 默认：false

  是否允许吸引玩家。

* attractingEntityTickCost

  * 类型：int
  * 默认：0

  吸引时每个实体每刻的耐久消耗。

* cooldown

  * 类型：long
  * 默认：20

  技能的冷却时间，以游戏刻为单位。

* radius

  * 类型：int
  * **必填**

  有效半径。

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->