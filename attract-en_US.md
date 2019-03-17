# Power: Attract

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: `rpgitems:attract`

Providing Plugin: `RPGItems`

Default Trigger: RIGHT_CLICK.
All available Trigger: ATTACHMENT, LEFT_CLICK, OFFHAND_CLICK, RIGHT_CLICK, SNEAK, SPRINT, TICK.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Pull around mobs in to player
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* attractingTickCost

  * Type: int
  * Default: 0

  Durability cost per tick when attracting.

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* maxSpeed

  * Type: double
  * Default: 0.4

  Maximum speed when attracting.

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: RIGHT_CLICK

  Triggers of this power.

* selectors

  * Type: Set&lt;String&gt;

  Selectors for this power.

* duration

  * Type: int
  * Default: 5

  Duration of this power when triggered by click in tick.

* attractPlayer

  * Type: boolean
  * Default: false

  Whether allow attracting player.

* attractingEntityTickCost

  * Type: int
  * Default: 0

  Durability cost per entity one tick when attracting.

* cooldown

  * Type: long
  * Default: 20

  Cooldown of the power, in ticks.

* radius

  * Type: int
  * **Required**

  Effective range in blocks.

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