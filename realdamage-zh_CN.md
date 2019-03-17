# 技能：真实伤害

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:realdamage`

来源插件：`RPGItems`

触发：HIT。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

对目标造成真实伤害但不会杀死它
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* realDamage

  * 类型：double
  * 默认：0.0

  真实伤害量

* cooldown

  * 类型：long
  * **必填**

  技能的冷却时间，以游戏刻为单位。

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

* minDamage

  * 类型：double
  * 默认：0.0

  触发该技能的最小伤害

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->