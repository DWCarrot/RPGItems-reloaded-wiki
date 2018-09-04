**instruction:**
`/rpgitem power {Item} projectile {cooldownTime} {cone} {projectileType} [range] [amount] [speed]`

**effect:**
{cone} is true: Adds a spelling entity skill to {Item} with cooldown time of {cooldownTime}. Right-click to [amount] {projectileType} type entities flying at [speed] speed. Centered on the player's direction, the angle [range] is randomly distributed in a conical shape. Acceptable types: skull, fireball, snowball, smallfireball, arrow, llamaspit

{cone} is false: Add launch entity skills for {Item} with cooldown time of {cooldownTime}. Right-click to [amount] {projectileType} type entities flying at [speed] speed. Acceptable types: skull, fireball, snowball, smallfireball, arrow, llamaspit

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- cone
  - Type: boolean
  - Default: false
  - Set Status: Required
  - Role: Is the transmission range cone-shaped?
- projectileType
  - Type: String
  - Default: Snowball
  - Set Status: Required
  - Role: Type of Launcher
- range
  - Type: int
  - Default: 15
  - Setting status: optional
  - Role: Range of emission range angle
- amount
  - Type: int
  - Default: 5
  - Setting status: optional
  - Role: The number of launches
- speed
  - Type: double
  - Default: 1
  - Setting status: optional
  - Role: Launch speed
- Gravity
  - Type: boolean
  - Default: true
  - Set status: additional
  - Role: whether it is affected by gravity
- burstCount
  - Type: int
  - Default: 1
  - Set status: additional
  - Role: Number of consecutive triggered skills
- burstInterval
  - Type: int
  - Default: 1
  - Set status: additional
  - Role: Releases consecutive triggered skill intervals at once
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testprojectile projectile 1 true arrow 10 10 2 `
