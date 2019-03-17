# 技能：自身效果

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:potionself`

来源插件：`RPGItems`

默认触发：RIGHT_CLICK。
可用触发：ATTACHMENT, HIT, HIT_TAKEN, LEFT_CLICK, OFFHAND_CLICK, RIGHT_CLICK, SNEAK, SPRINT。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

对自身施放状态效果
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* duration

  * 类型：int
  * **必填**

  持续时间，游戏刻

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* cooldown

  * 类型：long
  * **必填**

  技能的冷却时间，以游戏刻为单位。

* amplifier

  * 类型：int
  * **必填**

  效果倍率

* type

  * 类型：PotionEffectType
  * 默认：HEAL

  状态效果

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