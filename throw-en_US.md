# Power: Throw

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: `rpgitems:throw`

Providing Plugin: `RPGItems`

Default Trigger: RIGHT_CLICK.
All available Trigger: ATTACHMENT, LEFT_CLICK, OFFHAND_CLICK, RIGHT_CLICK, SNEAK, SPRINT.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Spawn and throw a entity
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* entityName

  * Type: String
  * **Required**

  Name of entity thrown

* display

  * Type: String
  * **Required**

  Display text of this power.

* isPersistent

  * Type: boolean
  * Default: false

  Whether to make entity persistent

* cooldown

  * Type: long
  * **Required**

  Cooldown of the power, in ticks.

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: RIGHT_CLICK

  Triggers of this power.

* conditions

  * Type: Set&lt;String&gt;

  Conditions of this power.

* speed

  * Type: double
  * **Required**

  Speed of entity thrown

* entityData

  * Type: String

  NBT data of entity

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->