# 技能：弹反

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:deflect`

来源插件：`RPGItems`

默认触发：`HIT_TAKEN`, `RIGHT_CLICK`。  
可用触发：`ATTACHMENT`, `HIT_TAKEN`, `LEFT_CLICK`, `OFFHAND_CLICK`, `RIGHT_CLICK`, `SNEAK`, `SPRINT`。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

弹反射来的箭矢或火球
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* duration

  * 类型：int
  * 默认：50

  持续时间

* cooldownpassive

  * 类型：int
  * 默认：20

  被动弹反的冷却时间

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* chance

  * 类型：int
  * 默认：50

  被动弹反的百分比几率

* deflectCost

  * 类型：int
  * 默认：0

  每次弹反的耐久消耗量。

* cooldown

  * 类型：int
  * 默认：20

  技能的冷却时间，以游戏刻为单位。

* facing

  * 类型：double
  * 默认：30.0

  最大有效视角，度

* triggers

  * 类型：Set&lt;Trigger&gt;
  * 默认：RIGHT_CLICK

  技能的触发。

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