**instruction:**
`/rpgitem power {Item} realdamage {cooldownTime} {realDamage}`

**effect:**
  Adds real damage ability to {Item}, {cooldownTime} is engraved for the game. Creatures that are hit will have real damage from {realDamage} but at least <minDamage> points remaining.

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- realDamage
  - Type: double
  - Default: 0
  - Set Status: Required
  - Role: Real damage value
- minDamage
  - Type: double
  - Default: 0
  - Set status: additional
  - Role: Target minimum residual blood volume
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testrealdamage realdamage 1 10`
