# Power: Repair

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:repair

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: LEFT_CLICK, RIGHT_CLICK.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Repair the item with some material
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* amount

  * Type: int
  * Default: 1

  Amount of material required

* display

  * Type: String
  * **Required**

  Display text of this power.

* durability

  * Type: int
  * Default: 20

  Durability to be repaired

* mode

  * Type: PowerRepair$RepairMode
  * Default: DEFAULT

  Whether allow repairing when durability would overflow

* abortOnSuccess

  * Type: boolean
  * Default: false

  Abort subsequence execution of powers when success

* abortOnFailure

  * Type: boolean
  * Default: false

  Abort subsequence execution of powers when fail

* material

  * Type: ItemStack
  * **Required**

  Material to be consumed

* cooldown

  * Type: int
  * Default: 0

  Cooldown of the power, in ticks.

* customMessage

  * Type: String

  Custom message when not enought material

* isSneak

  * Type: boolean
  * Default: false

  Whether require sneaking to trigger this power


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->