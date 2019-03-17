# 技能：弹射物

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:projectile`

来源插件：`RPGItems`

默认触发：RIGHT_CLICK。
可用触发：ATTACHMENT, HIT, HIT_TAKEN, LEFT_CLICK, LIVINGENTITY, OFFHAND_CLICK, RIGHT_CLICK, SNEAK, SPRINT。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

发射弹射物
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* projectileType

  * 类型：Class&lt;? extends Projectile&gt;
  * 默认：snowball

  弹射物类型

* amount

  * 类型：int
  * 默认：5

  弹射物的数量

* burstCount

  * 类型：int
  * 默认：1

  发射次数

* cost

  * 类型：int
  * 默认：1

  技能的耐久消耗量。

* isIncendiary

  * 类型：Boolean

  爆炸物是否会点火

* range

  * 类型：int
  * 默认：15

  弹射物的散射角

* isCone

  * 类型：boolean
  * **必填**

  是否以锥形发射弹射物

* setFireballDirection

  * 类型：boolean
  * 默认：false

  是否设置火球的方向使其不偏离

* triggers

  * 类型：Set&lt;Trigger&gt;
  * 默认：RIGHT_CLICK

  技能的触发。

* speed

  * 类型：double
  * 默认：1.0

  弹射物速度

* burstInterval

  * 类型：int
  * 默认：1

  每次发射之间的间隔

* gravity

  * 类型：boolean
  * 默认：true

  弹射物是否受到重力影响

* yield

  * 类型：Double

  爆炸物的爆炸半径

* cooldown

  * 类型：long
  * **必填**

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