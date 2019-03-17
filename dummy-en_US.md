# Power: Dummy

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:dummy

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: ATTACHMENT, PROJECTILE_HIT, HURT, SNEAK, HIT_TAKEN, LEFT_CLICK, SWAP_TO_OFFHAND, HIT, SPRINT, PICKUP_OFF_HAND, PLACE_OFF_HAND, TICK, RIGHT_CLICK, OFFHAND_CLICK, SWAP_TO_MAINHAND.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Won't do anything but give you fine control
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* display

  * Type: String

  Display text of this power.

* successResult

  * Type: TriggerResult
  * Default: OK

  Result returned when success

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: RIGHT_CLICK

  Triggers of this power.

* costResult

  * Type: TriggerResult
  * Default: COST

  Result returned when failed to comsume durability

* showCDWarning

  * Type: boolean
  * Default: true

  Show cooldown warning

* checkDurabilityBound

  * Type: boolean
  * Default: true

  If to check durability bound of this item

* cooldownResult

  * Type: TriggerResult
  * Default: COOLDOWN

  Result returned when in cooldown

* cooldown

  * Type: long
  * Default: 20

  Cooldown of the power, in ticks.

* cooldownKey

  * Type: String
  * Default: dummy

  Key for cooldowning

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