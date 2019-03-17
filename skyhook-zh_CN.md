# 技能：钩爪

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:skyhook`

来源插件：`RPGItems`

触发：RIGHT_CLICK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

发射钩爪钩住指定方块
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* railMaterial

  * 类型：Material
  * **必填**

  可以钩的材质

* cooldown

  * 类型：long
  * 默认：20

  技能的冷却时间，以游戏刻为单位。

* hookDistance

  * 类型：int
  * 默认：10

  可以钩的距离

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

* hookingTickCost

  * 类型：int
  * 默认：0

  钩子每 tick 的消耗

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->