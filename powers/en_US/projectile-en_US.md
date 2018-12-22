# Power: Projectile

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:projectile

Providing Plugin: RPGItems

Default Trigger: RIGHT_CLICK. All available Trigger: SPRINT, HIT, LEFT_CLICK, SNEAK, LIVINGENTITY, HIT_TAKEN, RIGHT_CLICK

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Launches projectile
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* projectileType

  * Type: Class<? extends Projectile>
  * Default: snowball

  Type of projectiles

* amount

  * Type: int
  * Default: 5

  Amount of projectiles

* burstCount

  * Type: int
  * Default: 1

  Burst count

* cost

  * Type: int
  * Default: 1

  Durability cost of the power.

* isIncendiary

  * Type: Boolean

  Whether this Explosive's explosion causes fire

* range

  * Type: int
  * Default: 15

  Range will projectiles spread, in degree

* isCone

  * Type: boolean
  * **Required**

  Whether launch projectiles in cone

* setFireballDirection

  * Type: boolean
  * Default: false

  Whether to set Fireball' direction so it won't curve

* speed

  * Type: double
  * Default: 1.0

  Speed of projectiles

* burstInterval

  * Type: int
  * Default: 1

  Interval between bursts

* gravity

  * Type: boolean
  * Default: true

  Whether the projectile have gravity

* yield

  * Type: Double

  Radius affected by this Explosive's explosion

* cooldown

  * Type: long
  * **Required**

  Cooldown of the power, in ticks.


<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->