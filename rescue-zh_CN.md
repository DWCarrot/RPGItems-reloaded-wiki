# 技能：拯救

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:rescue`

来源插件：`RPGItems`

触发：HIT_TAKEN, HURT。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

受到过量伤害或者血量即将低于指定值时拯救玩家
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* healthTrigger

  * 类型：int
  * 默认：4

  血量触发

* useBed

  * 类型：boolean
  * 默认：true

  是否回床（而非出生点）

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* damageTrigger

  * 类型：double
  * 默认：1024.0

  伤害触发

* cooldown

  * 类型：long
  * 默认：20

  技能的冷却时间，以游戏刻为单位。

* conditions

  * 类型：Set&lt;String&gt;

  技能的条件。

* inPlace

  * 类型：boolean
  * 默认：false

  是否原地拯救

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->