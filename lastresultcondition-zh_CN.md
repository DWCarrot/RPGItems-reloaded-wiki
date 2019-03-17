# 技能：结果条件

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:lastresultcondition`

来源插件：`RPGItems`

**标识技能**。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

要求上一个执行的技能返回特定的结果
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* failOnNoResult

  * 类型：boolean
  * 默认：true

  是否在不存在上一个执行的技能时失败

* okResults

  * 类型：Set&lt;TriggerResult&gt;
  * 默认：OK

  允许的结果

* isCritical

  * 类型：boolean
  * 默认：false

  条件失败时是否中止当前触发。

* id

  * 类型：String

  此条件/选择器的ID。

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->