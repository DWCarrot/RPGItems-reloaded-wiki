# Power: 传送

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

Full Name: rpgitems:teleport

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK, PROJECTILE_HIT. All available Trigger: RIGHT_CLICK, PROJECTILE_HIT


<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

传送到视线方向或者弹射物击中位置
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* distance

  * 类型：int
  * 默认：5

  最大距离

* cooldown

  * 类型：long
  * 默认：20

  技能的冷却时间，以游戏刻为单位

* targetMode

  * 类型：PowerTeleport$TargetMode
  * 默认：DEFAULT

  寻找传送点的模式


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->