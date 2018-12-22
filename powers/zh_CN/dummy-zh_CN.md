# Power: 空

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

Full Name: rpgitems:dummy

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: SPRINT, HIT, PICKUP_OFF_HAND, TICK, SWAP_TO_OFFHAND, SNEAK, LEFT_CLICK, RIGHT_CLICK, PROJECTILE_HIT, HIT_TAKEN, PLACE_OFF_HAND, OFFHAND_CLICK, SWAP_TO_MAINHAND


<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

什么都不做
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* display

  * 类型：String

  技能的提示文字

* successResult

  * 类型：TriggerResult
  * 默认：OK

  成功时的结果

* costResult

  * 类型：TriggerResult
  * 默认：COST

  无法消耗耐久时的结果

* checkDurabilityBound

  * 类型：boolean
  * 默认：true

  暂无说明

* cooldownResult

  * 类型：TriggerResult
  * 默认：COOLDOWN

  冷却时的结果

* cooldown

  * 类型：long
  * 默认：20

  技能的冷却时间，以游戏刻为单位

* cooldownKey

  * 类型：String
  * 默认：dummy

  暂无说明


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->