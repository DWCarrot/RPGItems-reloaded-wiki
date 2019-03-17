# 技能：喷火

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:fire

来源插件：RPGItems

默认触发：RIGHT_CLICK。 可用触发：RIGHT_CLICK, SPRINT, OFFHAND_CLICK, LEFT_CLICK, ATTACHMENT, SNEAK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

发射一个火焰方块，点燃击中的实体
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* distance

  * 类型：int
  * 默认：15

  最远有效距离

* burnduration

  * 类型：int
  * 默认：40

  火焰持续时间

* cooldown

  * 类型：long
  * 默认：20

  技能的冷却时间，以游戏刻为单位。

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