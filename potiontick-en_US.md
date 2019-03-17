# Power: Potion Tick

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:potiontick

Providing Plugin: RPGItems

Trigger: TICK.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Apply effect to player when equipped
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* duration

  * Type: int
  * Default: 60

  Time of potion effect, in ticks

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* effect

  * Type: PotionEffectType
  * Default: SPEED

  Type of potion effect

* clear

  * Type: boolean
  * Default: false

  Whether to remove the effect instead of adding it

* amplifier

  * Type: int
  * **Required**

  Amplifier of potion effect

* interval

  * Type: int
  * Default: 0

  Interval of this power

* conditions

  * Type: Set&lt;String&gt;

  Conditions of this power.

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->