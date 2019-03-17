# Power: Particle Barrier

<!-- This file is generated ingame by `/rpgitem gen-wiki`. -->
<!-- Please only edit between "beginCustomXXXX" and "endCustomXXXX".  -->
<!-- If you want to edit description of this power or property, -->
<!-- please edit corresponding section in "resources/lang/en_US.yml" -->

Full Name: rpgitems:particlebarrier

Providing Plugin: RPGItems

Default Trigger: TICK, RIGHT_CLICK. All available Trigger: SPRINT, ATTACHMENT, TICK, SNEAK, RIGHT_CLICK, LEFT_CLICK, OFFHAND_CLICK.

<!-- beginCustomHeader -->
<!-- endCustomHeader -->

## Description

Spawn a barrier that redirecting energy of incoming attacks to strength
<!-- beginCustomDescription -->
<!-- endCustomDescription -->

## Properties

* cost

  * Type: int
  * Default: 0

  Durability cost of the power.

* energyDecay

  * Type: double
  * Default: 1.5

  Decay of energy per second

* triggers

  * Type: Set&lt;Trigger&gt;
  * Default: TICK,RIGHT_CLICK

  Triggers of this power.

* projected

  * Type: boolean
  * Default: false

  Whether this barrier can be projected

* energyPerBarrier

  * Type: double
  * Default: 40.0

  Total energy gained when a barrier was broken

* energyPerLevel

  * Type: double
  * Default: 10.0

  Energy required per level of strength effect

* effect

  * Type: PotionEffectType
  * Default: INCREASE_DAMAGE

  Effect of particle barrier

* cooldown

  * Type: int
  * Default: 20

  Cooldown of the power, in ticks.

* conditions

  * Type: Set&lt;String&gt;

  Conditions of this power.

* barrierHealth

  * Type: double
  * Default: 40.0

  Health of a new barrier

<!-- beginCustomProperties -->
<!-- endCustomProperties -->

## Example

<!-- beginCustomExample -->
<!-- endCustomExample -->

## Note

<!-- beginCustomNote -->
<!-- endCustomNote -->