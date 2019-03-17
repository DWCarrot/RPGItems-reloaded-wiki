# 技能：计分板条件

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:scoreboardcondition`

来源插件：`RPGItems`

**标识技能**。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

玩家的计分板需满足的条件
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* score

  * 类型：String

  计分板分数范围，`score_name:min,max another_score_name:min,max`

* isStatic

  * 类型：boolean
  * 默认：false

  是否仅在触发开始时测试条件。

* isCritical

  * 类型：boolean
  * 默认：false

  条件失败时是否中止当前触发。

* id

  * 类型：String

  此条件/选择器的ID。

* tag

  * 类型：String

  计分板标签，`MUST_HAVE,!MUST_NOT_HAVE`

* team

  * 类型：String

  计分板队伍，`MUST_ON,!MUST_NOT_ON`

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->