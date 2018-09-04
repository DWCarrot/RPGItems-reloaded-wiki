**instruction:**
`/rpgitem power {Item} aoe {cooldown} {range} {effect} {duration} {amlifier} [selfapplication]`

**effect:**
Add a range effect to [Item] with a cooldown of [Cooldown] ticks. Right-click on all entities in the range [Effect] to [range]# that will apply [Duration] ticks and the effect level is [Amplifier]. If [ Self] is not set, this effect is also applied to the release by default

**Attributes**
- cooldownTime
  - Type: long
  - Set status: Required
  - Role: Set skill cooldown
- range
  - Type: int
  - Set status: Required
  - Role: Setting range
- effect
  - Type: String
  - Set status: Required
  - Role: Sets the effect character. Please refer to [Potion Effects](/NyaaCat/RPGitems-reloaded/wiki/en:Potion-Effects) for details
- duration
  - Type: int
  - Set status: Required
  - Role: Set duration
- amlifier
  - Type: int
  - Set status: Required
  - Role: Set skill level, level = amplifier +1
- selfapplication
  - Type: boolean
  - Setting status: optional
  - Role: whether to set effect on itself
- name
  - Type: String
  - Set status: additional
  - Function: Set display name
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testaoe aoe 10 10 speed 100 0 true`
