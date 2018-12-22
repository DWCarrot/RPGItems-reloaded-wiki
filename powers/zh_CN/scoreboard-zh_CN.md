# Power: 计分板

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

Full Name: rpgitems:scoreboard

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: SPRINT, HIT, PICKUP_OFF_HAND, TICK, SWAP_TO_OFFHAND, SNEAK, LEFT_CLICK, RIGHT_CLICK, PROJECTILE_HIT, HIT_TAKEN, PLACE_OFF_HAND, OFFHAND_CLICK, SWAP_TO_MAINHAND


<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

添加或移除玩家的计分板标签或队伍
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* abortOnSuccess

  * 类型：boolean
  * 默认：false

  成功后中止后续技能

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* cooldown

  * 类型：long
  * 默认：20

  技能的冷却时间，以游戏刻为单位

* tag

  * 类型：String

  需要添加或移除的标签，`TO_ADD,!TO_REMOVE`

* team

  * 类型：String

  需要加入或离开的队伍，`JOIN,!LEAVE`


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->