**instruction:**
`/rpgitem power {Item} rescue [cooldownTime] [healthTrigger] [useBed] [inPlace]`

**effect:**
  Adds salvation skills to {Item}, cooling time is [cooldownTime] game moments, saves when the player's blood volume is lower than the [healthTrigger] trigger, [useBed] is true, and returns to the origin when [inPlace] is true. Resurrection is invincible. Priority [inPlace]> [useBed]

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 20
  - Setting status: optional
  - Role: Cooling time
- healthTrigger
  - Type: int
  - Default: 4
  - Setting status: optional
  - Role: Rescue triggers minimum blood volume
- useBed
  - Type: boolean
  - Default: true
  - Setting status: optional
  - Role: whether to send back to the body
- inPlace
  - Type: boolean
  - Default: false
  - Setting status: optional
  - Role: whether to revive in situ
- damageTrigger
  - Type: double
  - Default: 1024
  - Set status: additional
  - Effect: How much damage is triggered above
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testrescue rescue`