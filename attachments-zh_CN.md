# 技能：配件

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:attachments

来源插件：RPGItems

默认触发：RIGHT_CLICK。 可用触发：HIT, RIGHT_CLICK, SPRINT, OFFHAND_CLICK, LEFT_CLICK, ATTACHMENT, SNEAK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

可以使用其他 RPGItem 作为配件。将会触发配件上的 ATTACHMENT 触发
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* allowedSlots

  * 类型：List&lt;EquipmentSlot&gt;

  可以使用的装备栏

* allowedInvSlots

  * 类型：List&lt;Integer&gt;

  可以使用的背包格，-1为禁用背包

* limit

  * 类型：int
  * 默认：0

  配件数量

* allowedItems

  * 类型：Set&lt;String&gt;

  可以使用的 RPGItem

* triggers

  * 类型：Set&lt;Trigger&gt;
  * 默认：RIGHT_CLICK

  技能的触发。

* selectors

  * 类型：Set&lt;String&gt;

  应用到本技能的选择器。

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->