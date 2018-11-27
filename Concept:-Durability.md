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

If the item have PowerUnbreakable, it won't lost its last 1 durability. When some tried to reduce durability more or equal to current durability, it will cancel the event 
(can't break blocks, can't damage entities or fail to trigger powers, and your armour with its last durability can't protect you from damage). 

