# Power: Selector

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:selector

Providing Plugin: RPGItems

**Is a marker power**.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Provide a selector for some AOE power
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* display

  * Type: String

  Display text of this power.

* count

  * Type: Integer

  Count of target entities

* team

  * Type: String

  Selecting targets by team(s), `MUST_ON,!MUST_NOT_ON`

* type

  * Type: String

  Type(s) of target entities

* score

  * Type: String

  Selecting targets by score(s), `score_name:min,max another_score_name:min,max`

* r

  * Type: Integer

  Selects only targets less than r blocks from reference position

* dx

  * Type: Integer

  Selects only targets less than dx blocks in X-axis from reference position

* dy

  * Type: Integer

  Selects only targets less than dx blocks in Y-axis from reference position

* dz

  * Type: Integer

  Selects only targets less than dx blocks in Z-axis from reference position

* x

  * Type: String

  X-coordinate of reference position, tilde notation is available. Use player's current position if empty

* y

  * Type: String

  Y-coordinate of reference position, tilde notation is available. Use player's current position if empty

* z

  * Type: String

  Z-coordinate of reference position, tilde notation is available. Use player's current position if empty

* id

  * Type: String

  ID of this power, should be unique on this item

* rm

  * Type: Integer

  Selects only targets more than rm blocks from reference position

* tag

  * Type: String

  Selecting targets by tag(s), `MUST_HAVE,!MUST_NOT_HAVE`


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->