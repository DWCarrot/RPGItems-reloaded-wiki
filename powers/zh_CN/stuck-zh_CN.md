# 技能：定身

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:stuck

来源插件：RPGItems

默认触发：HIT。 可用触发：RIGHT_CLICK, HIT。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

定身目标
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* chance

  * 类型：int
  * 默认：3

  触发几率，1/n

* cost

  * 类型：int
  * 默认：0

  击中实体定身的消耗

* range

  * 类型：int
  * 默认：10

  范围定身的范围

* facing

  * 类型：double
  * 默认：30.0

  定身最大视角

* costPerEntity

  * 类型：int
  * 默认：0

  范围定身每个实体的消耗

* selectors

  * 类型：Set<String>

  应用到本技能的选择器

* duration

  * 类型：int
  * 默认：100

  持续时间

* costAoe

  * 类型：int
  * 默认：0

  范围定身触发消耗

* cooldown

  * 类型：long
  * 默认：200

  技能的冷却时间，以游戏刻为单位


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->