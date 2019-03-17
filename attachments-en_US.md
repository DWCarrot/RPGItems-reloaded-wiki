# Power: Attachments

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: `rpgitems:attachments`

Providing Plugin: `RPGItems`

Default Trigger: `RIGHT_CLICK`.  
All available Trigger: `ATTACHMENT`, `HIT`, `LEFT_CLICK`, `OFFHAND_CLICK`, `RIGHT_CLICK`, `SNEAK`, `SPRINT`.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Can use other RPGItems as attachments. Firing this power will trigger ATTACHMENT trigger of attachments.
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* allowedSlots

  * Type: List&lt;EquipmentSlot&gt;

  allowed equipment slot

* allowedInvSlots

  * Type: List&lt;Integer&gt;

  allowed inventory slot number. -1 to disable inventory

* limit

  * Type: int
  * Default: 0

  maximum number of attachments

* allowedItems

  * Type: Set&lt;String&gt;

  RPGItems/Groups' id or name that are leagal attachment for this item

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: RIGHT_CLICK

  Triggers of this power.

* selectors

  * Type: Set&lt;String&gt;

  Selectors for this power.

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