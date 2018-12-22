# Power: AOE Effect

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:aoe

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: HIT, LEFT_CLICK, RIGHT_CLICK

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

* selectors

  * Type: Set<String>

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


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->