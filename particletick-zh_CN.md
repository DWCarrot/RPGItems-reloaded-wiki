# 技能：佩戴粒子效果

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：`rpgitems:particletick`

来源插件：`RPGItems`

触发：TICK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

佩戴后按照一定间隔生成粒子效果
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量。

* dustSize

  * 类型：double
  * 默认：0.0

  尘埃粒子效果的大小

* particleCount

  * 类型：int
  * 默认：1

  粒子效果的数量

* offsetX

  * 类型：double
  * 默认：0.0

  X 偏移

* offsetZ

  * 类型：double
  * 默认：0.0

  Z 偏移

* offsetY

  * 类型：double
  * 默认：0.0

  Y 偏移

* material

  * 类型：Material

  粒子效果的材质

* dustColor

  * 类型：int
  * 默认：0

  尘埃粒子效果的颜色

* effect

  * 类型：Effect
  * 默认：MOBSPAWNER_FLAMES

  视觉效果

* extra

  * 类型：double
  * 默认：1.0

  附加数据

* interval

  * 类型：int
  * 默认：15

  间隔时间，游戏刻

* particle

  * 类型：Particle

  粒子效果

* force

  * 类型：boolean
  * 默认：false

  强制显示粒子

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