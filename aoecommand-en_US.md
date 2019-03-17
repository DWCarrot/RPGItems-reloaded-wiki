# Power: AOE Command

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:aoecommand

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: SPRINT, ATTACHMENT, SNEAK, HURT, RIGHT_CLICK, LEFT_CLICK, OFFHAND_CLICK.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Run command for entities in range. PowerSelector is applicable.
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* c

  * Type: int
  * Default: 100

  Maximum count of entities.

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* display

  * Type: String
  * **Required**

  Display text of this power.

* selfapplication

  * Type: boolean
  * Default: false

  Whether to apply command on triggering player.

* facing

  * Type: double
  * Default: 30.0

  Maximum effective view angle in degrees.

* permission

  * Type: String

  Permission that will be given to user executing command

* type

  * Type: String
  * Default: entity

  Type of entities

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: RIGHT_CLICK

  Triggers of this power.

* selectors

  * Type: Set&lt;String&gt;

  Selectors for this power.

* command

  * Type: String
  * **Required**

  Command to be executed

* r

  * Type: int
  * **Required**

  Maximum range in blocks.

* mustsee

  * Type: boolean
  * Default: false

  Whether only apply to the entities within line of sight

* cooldown

  * Type: long
  * **Required**

  Cooldown of the power, in ticks.

* rm

  * Type: int
  * **Required**

  Minimum range in blocks.

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