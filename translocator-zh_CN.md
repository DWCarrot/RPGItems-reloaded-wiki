# 技能：传送信标

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:translocator`

来源插件：`RPGItems`

触发：PICKUP_OFF_HAND, PLACE_OFF_HAND, SWAP_TO_MAINHAND, SWAP_TO_OFFHAND。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

投掷信标，之后传送到信标位置
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* setupCost

  * 类型：int
  * 默认：0

  建立信标所需消耗

* tpCost

  * 类型：int
  * 默认：0

  传送所需消耗

* cooldown

  * 类型：long
  * 默认：80

  技能的冷却时间，以游戏刻为单位。

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