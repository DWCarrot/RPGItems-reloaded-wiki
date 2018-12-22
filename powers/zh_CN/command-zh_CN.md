# Power: 命令

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

Full Name: rpgitems:command

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: SNEAK, LEFT_CLICK, RIGHT_CLICK, SPRINT, HURT


<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

执行一条命令
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* display

  * 类型：String
  * **必填**

  技能的提示文字

* cooldown

  * 类型：long
  * **必填**

  技能的冷却时间，以游戏刻为单位

* permission

  * 类型：String

  执行指令所需的临时权限

* command

  * 类型：String

  执行的命令


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->