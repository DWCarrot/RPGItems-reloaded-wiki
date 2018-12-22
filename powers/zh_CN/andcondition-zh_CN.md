# Power: And Condition

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

Full Name: rpgitems:andcondition

Providing Plugin: RPGItems

**Is a marker power**.


<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Condition that requires all its Conditions are met
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* isStatic

  * 类型：boolean
  * 默认：true

  是否仅在触发开始时测试条件

* isCritical

  * 类型：boolean
  * 默认：false

  条件失败时是否中止当前触发

* id

  * 类型：String

  此条件/选择器的ID

* conditions

  * 类型：Set<String>

  技能的条件


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->