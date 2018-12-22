# 技能：计分板

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:scoreboard

来源插件：RPGItems

默认触发：RIGHT_CLICK。 可用触发：HIT, OFFHAND_CLICK, SNEAK, PICKUP_OFF_HAND, SWAP_TO_MAINHAND, PROJECTILE_HIT, HIT_TAKEN, RIGHT_CLICK, TICK, SWAP_TO_OFFHAND, SPRINT, LEFT_CLICK, PLACE_OFF_HAND。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

添加或移除玩家的计分板标签或队伍
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

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

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->