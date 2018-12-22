# 技能：装备条件

<!-- 本文件是通过游戏内 `/rpgitem gen-wiki` 命令生成的。 -->
<!-- 请只在对应的 "beginCustomXXXX" 与 "endCustomXXXX" 间编辑。  -->
<!-- 如果您想修改技能或其属性的描述， -->
<!-- 请修改 "resources/lang/zh_CN.yml" 中对应的项。 -->

全名：rpgitems:equipmentcondition

来源插件：RPGItems

**标识技能**。

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## 说明

要求玩家穿特定装备
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## 属性

* slots

  * 类型：Set<EquipmentSlot>

  暂无说明

* itemStack

  * 类型：ItemStack

  玩家需要装备的物品

* material

  * 类型：Material

  玩家需要装备的材质

* matchAllSlot

  * 类型：boolean
  * 默认：false

  暂无说明

* isCritical

  * 类型：boolean
  * 默认：false

  条件失败时是否中止当前触发

* id

  * 类型：String

  此条件/选择器的ID

* rpgitem

  * 类型：String

  玩家需要装备的 RPGItem


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## 示例

<!-- beginCustomExample -->
<!-- endCustomExample -->

## 说明

<!-- beginCustomNote -->
<!-- endCustomNote -->