**instruction:**
`/rpgitem power {Item} potiontick {amplifier} {effect} [interval] [duration]`

**effect:**
  When the player holds/wears, the {effect} effect with the duration of [duration] game engraved with {amplifier} is given again each time [interval] game is engraved. Potions available: See the [Potion Effect](/NyaaCat/RPGitems-reloaded/wiki/en:Potion-Effects) for details

**Attributes:**
- amplifier
  - Type: int
  - Default: 1
  - Set Status: Required
  - Role: Potion effect level
- effect
  - Type: String
  - Default: SPEED
  - Set Status: Required
  - Role: Potion effect: See [Potion System](/NyaaCat/RPGitems-reloaded/wiki/en:Potion-Effects) for details
- interval
  - Type: int
  - Default: 0
  - Setting status: optional
  - Role: potion effect cycle trigger interval
- duration
  - Type: int
  - Default: 60
  - Setting status: optional
  - Role: potency effect duration
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpotiontick potiontick 1 speed `