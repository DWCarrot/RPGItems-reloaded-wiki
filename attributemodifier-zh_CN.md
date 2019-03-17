# 技能：属性修改

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:attributemodifier`

来源插件：`RPGItems`

**标识技能**。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

修改玩家/物品属性
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* amount

  * 类型：double
  * **必填**

  数值

* name

  * 类型：String
  * **必填**

  属性名称

* attribute

  * 类型：Attribute
  * **必填**

  属性

* slot

  * 类型：EquipmentSlot

  物品栏位

* uuidMost

  * 类型：int
  * 默认：-1562882519

  UUID 前半部分

* operation

  * 类型：AttributeModifier$Operation
  * 默认：ADD_NUMBER

  操作

* uuidLeast

  * 类型：int
  * 默认：-1935899162

  UUID 后半部分

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->