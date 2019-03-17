# 技能：击中命令

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:commandhit

来源插件：RPGItems

默认触发：HIT。 可用触发：HIT, RIGHT_CLICK, HURT, LIVINGENTITY, SPRINT, OFFHAND_CLICK, LEFT_CLICK, ATTACHMENT, SNEAK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

击中目标时执行一条命令。
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* display

  * 类型：String
  * **必填**

  技能的提示文字。

* cooldown

  * 类型：long
  * **必填**

  技能的冷却时间，以游戏刻为单位。

* permission

  * 类型：String

  执行指令所需的临时权限

* triggers

  * 类型：Set&lt;Trigger&gt;
  * 默认：HIT

  技能的触发。

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

* command

  * 类型：String

  执行的命令

* minDamage

  * 类型：double
  * 默认：0.0

  触发最小的伤害

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->