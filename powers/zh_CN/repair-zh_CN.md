# 技能：修理

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:repair

来源插件：RPGItems

默认触发：RIGHT_CLICK。 可用触发：RIGHT_CLICK, LEFT_CLICK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

用指定材料修理物品
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* amount

  * 类型：int
  * 默认：1

  所需材料数量

* display

  * 类型：String
  * **必填**

  技能的提示文字

* durability

  * 类型：int
  * 默认：20

  修复耐久值

* mode

  * 类型：PowerRepair$RepairMode
  * 默认：DEFAULT

  是否允许耐久溢出

* abortOnSuccess

  * 类型：boolean
  * 默认：false

  修理成功后中止后续技能

* abortOnFailure

  * 类型：boolean
  * 默认：false

  修理失败时中止后续技能

* material

  * 类型：ItemStack
  * **必填**

  修理用材料

* cooldown

  * 类型：int
  * 默认：0

  技能的冷却时间，以游戏刻为单位

* customMessage

  * 类型：String

  材料不足时的自定义提示

* isSneak

  * 类型：boolean
  * 默认：false

  修理时是否需要潜行


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->