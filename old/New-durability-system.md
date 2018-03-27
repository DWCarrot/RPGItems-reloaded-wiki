**To set durability like the old way:**

```
/rpgitem some_item durability 100
/rpgitem some_item durabilitybound 0 100
/rpgitem some_item defaultdurability 100
```
-------

An item will lose durability when:
* break a block will reduce item.blockBreakingCost(default 1) durability 
* damage a entity will reduce item.hittingCost(default 1) durability 
* some power will reduce durability according to power.consumption (or some power specified way)
* armor be hit will reduce item.hit(default 1) or item.hit*damage/100(when item.hitCostByDamage is set) durability

Consumption can be negative, so that item will increase durability after triggered some power with negative consumption .

Default value of power.consumption is 0 (1 for projectile-related power for compatibility), you can set it using
 `/rpgitem item set somepower number consumption value` 
e.g.
 `/rpgitem imba_item set arrow 1 consumption 1` set consumption of "imba_item"'s first PowerArrow to 1

After some event be handled, if item's durability is below or equal 0, it will consume itself.

If the item have PowerUnbreakable, it won't lost its last 1 durability. When some tried to reduce durability more or equal to current durability, it will cancel the event (can't break blocks, can't damage entities or fail to trigger powers, and your armour with its last durability can't protect you from damage). 

物品会在以下时候丢失耐久：
* 破坏方块，降低item.blockBreakingCost(默认1)耐久
* 伤害实体，降低item.hittingCost（默认1）耐久
* 触发某些技能，按照技能的consumption属性降低耐久（或者技能自身的设定）
* 护甲受到攻击，降低item.hitCost（默认1）耐久

耐久消耗可以为负数，也就是触发技能后增长耐久。

耐久消耗默认值为0（弹射物相关的消耗为1以保持兼容）。可以通过 `/rpgitem item set somepower number consumption value` 设置。
如：
`/rpgitem imba_item set arrow 1 consumption 1`设置“imba_item”的第一个PowerArrow的耐久消耗为1。

触发事件后，若物品的耐久等于低于0，物品就会消耗掉。

如果物品有PowerUnbreakable，物品将不会消耗自己的最后一点耐久。当试图消耗的耐久大于等于当前耐久，事件将被取消（无法破坏方块、伤害实体或触发技能，以及仅有最后一点耐久的护甲无法减伤）。
