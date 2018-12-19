**instruction:**
`/rpgitem power {Item} potionself {cooldownTime} {duration} {amplifier} {type}`

**effect:**
  Right-click on the {type} potion effect of level {amplifier} for {duration} game moments, and cooldown time. Potions available: See the [Potion Effects](/NyaaCat/RPGitems-reloaded/wiki/en:Potion-Effects) for details

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- dration
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Duration
- amplifier
  - Type: int
  - Default: 1
  - Set Status: Required
  - Role: Potion effect level
- type
  - Type: String
  - Default: HARM
  - Set Status: Required
  - Role: Potion effect: See [Potion System](/NyaaCat/RPGitems-reloaded/wiki/en:Potion-Effects) for details
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpotionself potionself 100 100 1 speed `
