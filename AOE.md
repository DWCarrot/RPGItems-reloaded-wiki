<!-- --- title: Powers: AOE -->

**Full Name:** rpgitems:aoe

## Description

Add a range effect to item with a cooldown of `cooldown ` ticks. Apply `effect` effect to entities in `range` with `duration` ticks duration and `amplifier`+1 level. If `selfapplication` is true, the effect will also apply to the player.

## Properties

* cooldown

  * Type: long
  * **Required**

  Cooldown of power.

* range

  * Type: int
  * **Required**

  Maximum effective range in blocks.

* type

  * Type: PotionEffectType
  * **Required**
  
  Effect to be applied. See https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/potion/PotionEffectType.html for full list

* duration

  * Type: int
  * **Required**
  
  Duration of effect

* amplifier

  * Type: int
  * **Required**
  
  Amplifier of effect. level = amplifier +1

* selfapplication

  * Type: boolean

  Whether to apply effect to the player

* name

  * Type: String

  Display text of this power. Will use default text in case of null

* cost

  * Type: int

  Durability cost of this power.

## Example

`/rpgitem power item aoe cooldown:10 range:10 type:speed duration:100 amplifier:0 selfapplication:true`

## Note

You can use power selector to filter which entities will be affect by this power.
