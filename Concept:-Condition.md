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

TBD

TBC