**instruction:**
`/rpgitem power {Item} tippedarrow {cooldownTime} {type} {duration} {amplifier} `

**effect:**
 Adds drug arrow skill to {Item}, effect {type} duration{duration} is game engraved, level is {amplifier}, cooldown time is {cooldownTime} game moment. Right shot launch. Effective potion effect: see [Potion Effect](/NyaaCat/RPGitems-reloaded/wiki/en:Potion-Effects) for details

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set status: Required
  - Role: Cooling time
- type
  - Type: String
  - Default: null
  - Set status: Required
  - Role: potion effect type
- duration
  - Type: int
  - Default: 15
  - Set status: Required
  - Role: Duration
- amplifier
  - Type: int
  - Default: 1
  - Set status: Required
  - Role: Effect Level
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testtippedarrow tippedarrow 20 speed 40 1`