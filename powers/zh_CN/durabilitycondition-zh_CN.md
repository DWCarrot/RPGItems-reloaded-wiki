# 技能：耐久条件

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:durabilitycondition

来源插件：RPGItems

**标识技能**。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

要求耐久在一定范围内
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* isStatic

  * 类型：boolean
  * 默认：false

  是否仅在触发开始时测试条件

* durabilityMin

  * 类型：int
  * 默认：-2147483648

  耐久需大于该值

* isCritical

  * 类型：boolean
  * 默认：false

  条件失败时是否中止当前触发

* durabilityMax

  * 类型：int
  * 默认：2147483647

  耐久需小于该值

* id

  * 类型：String

  此条件/选择器的ID


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->