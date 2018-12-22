# 技能：击中效果

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:potionhit

来源插件：RPGItems

触发：HIT, LIVINGENTITY。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

击中后对目标施放状态效果
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* duration

  * 类型：int
  * **必填**

  持续时间，游戏刻

* chance

  * 类型：int
  * 默认：20

  触发几率，1/n

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* amplifier

  * 类型：int
  * **必填**

  效果倍率

* type

  * 类型：PotionEffectType
  * 默认：HARM

  状态效果


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->