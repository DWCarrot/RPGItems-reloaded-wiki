"Condition" is a new concept introduced in RPGItems 3.6. Power won't fire until all of its conditions are met. Each condition has a id. By adding an id to a power's `conditions` property, you add that condition to the power.

If a condition is static, it'll evaluate its result once, before all powers' execution. Else the condition will evaluate its result each time before firing the power that depends on it.

If a condition is critical, it'll abort the trigger if it fails. That is, a non-critical condition prevent powers that depend on it, and a critical condition cancel all the powers after its failure.

There are two types of conditions: primitive and complex.

## Primitive conditions

Primitive conditions don't depend of other conditions. 

### Chance Condition

* Name: `rpgitems:chancecondition`
* Can be static: Yes
* Can be critical: Yes

This is a condition that "meet by chance". Each evaluate of this condition have a `chancePercentage` chance of returning true. You can use this condition to make powers fire randomly.

`chancePercentage` may be a decimal (technically it is a `double`).

### Durability Condition

* Name: `rpgitems:durabilitycondition`
* Can be static: Yes
* Can be critical: Yes

Durability condition checks if an items RPGItem durability is in given range. That is, greater than `durabilityMin` and if `durabilityMax` greater than zero, less than `durabilityMax`.

### Equipment Condition

* Name: `rpgitems:equipmentcondition`
* Can be static: Must
* Can be critical: Yes

This condition checks whether the player is wearing the required material, item stack, rpgitem or (to be added) rpgitem group. If any/all (controlled by `matchAllSlot`) of `slots` match the `material` `itemStack` `rpgitem` and (to be added) rpgitem group, it returns true. All of `material` `itemStack` `rpgitem` will be checked if set, and match empty slot only if none of them are set.

Available `material`s are listed here <https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html>.  
Besides the above mentioned Materials, `itemStack` also accepts `HAND` as value (the item in main hand).  
`rpgitem` accepts name or uid of a RPGItem.

### Last Result Condition

* Name: `rpgitems:lastresultcondition`
* Can be static: No
* Can be critical: Yes

Checks whether result of last power is in `okResults`. If no power has been fired before, it fails if `failOnNoResult`.

### Scoreboard Condition

* Name: `rpgitems:lastresultcondition`
* Can be static: Yes
* Can be critical: Yes

It is a scoreboard-based condition, return true if the player's `score`, `tag`, and `team` meet it. 

`score` uses a syntax like `score_name:min,max another_score_name:min,max`.  
`tag` uses a syntax like `MUST_HAVE,!MUST_NOT_HAVE`.  
`team` uses a syntax like `MUST_ON,!MUST_NOT_ON`. Only the first `MUST_ON` spec takes effect.  

## Complex Conditions

TBD