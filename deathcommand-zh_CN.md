# 技能：即死命令

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:deathcommand`

来源插件：`RPGItems`

触发：HIT。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

以 1/chance 的几率杀死目标并执行命令
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* chance

  * 类型：int
  * **必填**

  触发几率， 1/n

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* count

  * 类型：int
  * 默认：1

  执行命令的次数

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

* command

  * 类型：String

  执行的命令

* desc

  * 类型：String

  技能的提示文字

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->