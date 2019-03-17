# Power: Potion Self

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:potionself

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: HIT, SPRINT, ATTACHMENT, SNEAK, HIT_TAKEN, RIGHT_CLICK, LEFT_CLICK, OFFHAND_CLICK.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Apply effect to player when used
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* duration

  * Type: int
  * **Required**

  Time of potion effect, in ticks

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* cooldown

  * Type: long
  * **Required**

  Cooldown of the power, in ticks.

* amplifier

  * Type: int
  * **Required**

  Amplifier of potion effect

* type

  * Type: PotionEffectType
  * Default: HEAL

  Type of potion effect

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: RIGHT_CLICK

  Triggers of this power.

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