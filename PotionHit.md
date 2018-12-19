**instruction:**
`/rpgitem power {Item} potionhit {chance} {dration} {amplifier} {type}`

**effect:**
  There is a 1/{chance}% chance of attack to get a potion effect. {type} is a potion effect {dration} is the duration in gameplay, {amplifier}
      Is an integer. Potions available: See the [Potion Effect](/NyaaCat/RPGitems-reloaded/wiki/en:Potion-Effects) for details.

**Attributes:**
- chance
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Trigger probability
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
  - Role: Potion effect: See [Potion Effects](/NyaaCat/RPGitems-reloaded/wiki/en:Potion-Effects) for details
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpotionhit potionhit 1 100 1 speed `
