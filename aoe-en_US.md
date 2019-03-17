# Power: AOE Effect

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: `rpgitems:aoe`

Providing Plugin: `RPGItems`

Default Trigger: `RIGHT_CLICK`.  
All available Trigger: `ATTACHMENT`, `HIT`, `LEFT_CLICK`, `OFFHAND_CLICK`, `RIGHT_CLICK`, `SNEAK`, `SPRINT`.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Apply effect to entities in range. PowerSelector is applicable.
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* selfapplication

  * Type: boolean
  * Default: true

  Whether to apply effect on triggering player.

* range

  * Type: int
  * **Required**

  Effective range in blocks.

* type

  * Type: PotionEffectType
  * **Required**

  Type of applied effect.

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: RIGHT_CLICK

  Triggers of this power.

* selectors

  * Type: Set&lt;String&gt;

  Selectors for this power.

* duration

  * Type: int
  * **Required**

  Duration of applied effect, in ticks.

* cooldown

  * Type: long
  * **Required**

  Cooldown of the power, in ticks.

* name

  * Type: String

  Display text of the power.

* amplifier

  * Type: int
  * Default: 1

  Amplifier of applied effect.

* conditions

  * Type: Set&lt;String&gt;

  Conditions of this power.

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
```/rpgitem power item aoe cooldown:10 range:10 type:speed duration:100 amplifier:0 selfapplication:true```
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
You can use power selector to filter which entities will be affect by this power.
<!-- endCustomNote -->