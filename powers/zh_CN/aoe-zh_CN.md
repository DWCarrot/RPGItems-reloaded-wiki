# Power: 范围效果

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

Full Name: rpgitems:aoe

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: LEFT_CLICK, RIGHT_CLICK, HIT


<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

对周围实体施放状态效果。可使用选择器。
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* selfapplication

  * 类型：boolean
  * 默认：true

  是否对自身使用

* range

  * 类型：int
  * **必填**

  有效范围，方块

* type

  * 类型：PotionEffectType
  * **必填**

  状态效果

* selectors

  * 类型：Set<String>

  应用到本技能的选择器

* duration

  * 类型：int
  * **必填**

  持续时间，游戏刻

* cooldown

  * 类型：long
  * **必填**

  技能的冷却时间，以游戏刻为单位

* name

  * 类型：String

  技能的提示文字

* amplifier

  * 类型：int
  * 默认：1

  效果倍率


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->