# 技能：经济

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:economy`

来源插件：`RPGItems`

默认触发：ATTACHMENT, HIT, LEFT_CLICK, OFFHAND_CLICK, RIGHT_CLICK, SNEAK, SPRINT。
可用触发：ATTACHMENT, HIT, LEFT_CLICK, OFFHAND_CLICK, RIGHT_CLICK, SNEAK, SPRINT。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

向玩家付款或扣款
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* abortOnFailure

  * 类型：boolean
  * 默认：true

  失败时中止

* showFailMessage

  * 类型：boolean
  * 默认：false

  失败时显示经济插件的消息

* cooldown

  * 类型：int
  * 默认：20

  技能的冷却时间，以游戏刻为单位。

* triggers

  * 类型：Set&lt;Trigger&gt;
  * 默认：SNEAK,RIGHT_CLICK,HIT,LEFT_CLICK,ATTACHMENT,SPRINT,OFFHAND_CLICK

  技能的触发。

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

* amountToPlayer

  * 类型：double
  * 默认：0.0

  向玩家支付的数量（可为负）

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->