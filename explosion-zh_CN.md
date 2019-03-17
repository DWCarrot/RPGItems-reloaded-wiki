# 技能：爆炸

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:explosion`

来源插件：`RPGItems`

默认触发：`PROJECTILE_HIT`。  
可用触发：`ATTACHMENT`, `HIT`, `LEFT_CLICK`, `LOCATION`, `OFFHAND_CLICK`, `PROJECTILE_HIT`, `RIGHT_CLICK`, `SNEAK`, `SPRINT`。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

制造一个玩家产生的爆炸
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* chance

  * 类型：double
  * 默认：20.0

  触发几率，百分比

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* distance

  * 类型：int
  * 默认：20

  最远距离

* power

  * 类型：float
  * 默认：4.0

  爆炸威力。 4 为 TNT 的爆炸威力

* triggers

  * 类型：Set&lt;Trigger&gt;
  * 默认：PROJECTILE_HIT

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