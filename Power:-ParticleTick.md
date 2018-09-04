**instruction:**
`/rpgitem power {Item} particletick {effect} [interval]`

**effect:**
  Add particle effects to {Item}. When held, creates particles around the player. The interval is [interval]tick. {effect} can be one of SMOKE/ENDER_SIGNAL/MOBSPAWNER_FLAMES.

**Attributes:**
- effect
  - Type: String
  - Default: FLAME
  - Set Status: Required
  - Role: Particle type
- interval
  - Type: int
  - Default: 15
  - Setting status: optional
  - Effect: Trigger interval
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testparticletick particletick FLAME 20`