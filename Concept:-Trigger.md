# Trigger

## About Trigger

"Trigger" is a new concept introduced in RPGItems 3.6. Actually, the idea of trigger dates back to earlier version of RPGItems (like `isRight` property of power `command`), and it becomes more powerful in RPGItems 3.6.

When a player holding RPGItem fires some event (e.g. right clicks / attacks another entity / projectile hits), RPGItem will execute powers added to the item, this process is called "Trigger". In earlier version of RPGItems there are set triggers for a power and can't change. In 3.6, you can set a list of available triggers for a power. One trigger can fire multiple powers at a time, and a power of an item can be fired by multiple trigger.

For triggers of each power, you can consult the wiki for the power [WIP], or help yourself by tab-completing in game.

For example, you can create a item that launch ice right-clicking and launch fire left-clicking
 
```
/rpgitem create fireandice
/rpgitem power fireandice rpgitems:fire triggers:LEFT_CLICK
/rpgitem power fireandice rpgitems:ice
```

Here we set power `fire`'s trigger to `LEFT_CLICK` for left-clicking, and default trigger of `ice` is right-clicking.

We can modify triggers of item, e.g. left-clicking for `ice` and both for `fire`

```
/rpgitem set fireandice rpgitems:fire 1 triggers LEFT_CLICK,RIGHT_CLICK
/rpgitem set fireandice rpgitems:ice 1 triggers LEFT_CLICK
```

Powers that fired by a trigger executes sequentially, and some power can break the execution of current trigger. We call it `abort`s the trigger. For example, power `repair` and power `economy` has a property `abortOnFailure`. If `abortOnFailure` is set on those powers, powers after them won't fire if it fails to repair/withdraw.

Say, we can pay 10$ to fire a fireball with 0.5s (10tick) cooldown

```
/rpgitem create tendollarfireball
/rpgitem power tendollarfireball rpgitems:economy amountToPlayer:-10 abortOnFailure:true cooldown:10
/rpgitem power tendollarfireball rpgitems:fireball cooldown:0
```

## List of Built-in Triggers

Built-in triggers:

* `HIT`  
  Triggers when player hit entity by melee/projectile with RPGItem
* `PROJECTILE_HIT`  
  Triggers when projectile fired by RPGItem hits block/entity
* `HIT_TAKEN`  
  Triggers when player is to take damage with RPGItem in hand/inventory. Note: the player is not hurt yet and the damage may be altered or cancelled.
* `HURT`  
  Triggers when player is hurt with RPGItem in hand/inventory. Note: the player is hurt and the damage can't be altered or cancelled.
* `LEFT_CLICK`  
  Triggers when player left clicks with RPGItem in main hand
* `RIGHT_CLICK`  
  Triggers when player right clicks with RPGItem in main hand
* `OFFHAND_CLICK`  
  Triggers when player right clicks with RPGItem in offhand
* `SNEAK`  
  Triggers when player sneaks with RPGItem in main hand
* `SPRINT`  
  Triggers when player sprints with RPGItem in main hand
* `SWAP_TO_OFFHAND`  
  Triggers when player swap RPGItem to offhand from main hand
* `SWAP_TO_MAINHAND`  
  Triggers when player swap RPGItem to main hand from offhand
* `PLACE_OFF_HAND`  
  Triggers when player place RPGItem to offhand slot in inventory
* `PICKUP_OFF_HAND`  
  Triggers when player pickup RPGItem from offhand slot in inventory
* `TICK`  
  Triggers every tick for RPGItem player holds/equips

Extensions may add new triggers to RPGItems, you can consult their document for detail. Unknown trigger on item will be ignored and removed with a warning.

## Extension Development: Add Triggers

TBD