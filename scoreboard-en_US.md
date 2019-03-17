# Power: Scoreboard

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:scoreboard

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: ATTACHMENT, PROJECTILE_HIT, SNEAK, HIT_TAKEN, LEFT_CLICK, SWAP_TO_OFFHAND, HIT, SPRINT, PICKUP_OFF_HAND, PLACE_OFF_HAND, TICK, RIGHT_CLICK, OFFHAND_CLICK, SWAP_TO_MAINHAND.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Add/remove tag/team to/from player's scoreboard
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* abortOnSuccess

  * Type: boolean
  * Default: false

  Abort subsequence execution of powers when success

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* cooldown

  * Type: long
  * Default: 20

  Cooldown of the power, in ticks.

* tag

  * Type: String

  Tag(s) to add and remove, `TO_ADD,!TO_REMOVE`

* team

  * Type: String

  Team(s) to join and leave, `JOIN,!LEAVE`

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