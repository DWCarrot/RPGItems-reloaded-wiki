# Power: Delayed Command

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: `rpgitems:delayedcommand`

Providing Plugin: `RPGItems`

Default Trigger: RIGHT_CLICK.
All available Trigger: ATTACHMENT, HURT, LEFT_CLICK, OFFHAND_CLICK, RIGHT_CLICK, SNEAK, SPRINT.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Run command on click with a delay
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* delay

  * Type: int
  * **Required**

  Delay before executing command

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* display

  * Type: String
  * **Required**

  Display text of this power.

* cooldown

  * Type: long
  * **Required**

  Cooldown of the power, in ticks.

* permission

  * Type: String

  Permission that will be given to user executing command

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: RIGHT_CLICK

  Triggers of this power.

* conditions

  * Type: Set&lt;String&gt;

  Conditions of this power.

* command

  * Type: String

  Command to be executed

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->