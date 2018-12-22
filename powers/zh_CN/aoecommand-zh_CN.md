# Power: 范围命令

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

Full Name: rpgitems:aoecommand

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: SNEAK, LEFT_CLICK, RIGHT_CLICK, SPRINT, HURT


<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

对周围实体执行命令。可使用选择器。
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* c

  * 类型：int
  * 默认：100

  实体的最大数量

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* display

  * 类型：String
  * **必填**

  技能的提示文字

* selfapplication

  * 类型：boolean
  * 默认：false

  Whether to apply command on triggering player.

* facing

  * 类型：double
  * 默认：30.0

  有效视角，度

* permission

  * 类型：String

  执行指令所需的临时权限

* type

  * 类型：String
  * 默认：entity

  实体的类型

* selectors

  * 类型：Set<String>

  应用到本技能的选择器

* command

  * 类型：String
  * **必填**

  要执行的命令

* r

  * 类型：int
  * **必填**

  最大距离，方块

* mustsee

  * 类型：boolean
  * 默认：false

  是否必须要看见实体

* cooldown

  * 类型：long
  * **必填**

  技能的冷却时间，以游戏刻为单位

* rm

  * 类型：int
  * **必填**

  最小距离，方块


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->