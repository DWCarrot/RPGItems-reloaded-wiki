**instruction:**
`/rpgitem power {Item} rumble {cooldownTime} {power} {distance}`

**effect:**
  Adds bandit ability to {Item}, cooldown time is {cooldownTime}, effective range is {distance}, explosion around the first entity touched by the bandit advances and will be the same around small area The entity hits the sky with a {power} strike level.

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- power
  - Type: int
  - Default: 2
  - Set Status: Required
  - Role: Hit level
- distance
  - Type: int
  - Default: 15
  - Set Status: Required
  - Role: advance distance
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testrumble rumble 100 4 10`