# 技能：投掷实体

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:throw

来源插件：RPGItems

默认触发：RIGHT_CLICK。 可用触发：RIGHT_CLICK, LEFT_CLICK。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

生成并投掷实体
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* cost

  * 类型：int
  * 默认：0

  技能的耐久消耗量

* entityName

  * 类型：String
  * **必填**

  实体名称

* display

  * 类型：String
  * **必填**

  技能的提示文字

* isPersistent

  * 类型：boolean
  * 默认：false

  实体是否保留在世界存档

* cooldown

  * 类型：long
  * **必填**

  技能的冷却时间，以游戏刻为单位

* speed

  * 类型：double
  * **必填**

  投掷速度

* entityData

  * 类型：String

  实体 NBT 数据


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->