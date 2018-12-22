# Power: 佩戴状态效果

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

Full Name: rpgitems:potiontick

Providing Plugin: RPGItems

Trigger: TICK


<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

佩戴后按照一定间隔施放状态效果
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* duration

  * 类型：int
  * 默认：60

  持续时间，游戏刻

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* effect

  * 类型：PotionEffectType
  * 默认：SPEED

  状态效果

* clear

  * 类型：boolean
  * 默认：false

  清除状态效果而非施放

* amplifier

  * 类型：int
  * **必填**

  效果倍率

* interval

  * 类型：int
  * 默认：0

  间隔时间，游戏刻


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->