**instruction:**
`/rpgitem power {Item} fire {cooldownTime} {distance} {burnduration}`

**effect:**
  Adds a fire ability to {item}, which fires the flame on the right and causes a {distance} duration {burnduration} wall and cooling time {cooldownTime} ticks when touching the first square.

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set status: Required
  - Role: Set skill cooldown
- distance
  - Type: int
  - Type: 15
  - Set status: Required
  - Role: The distance of the fire wall
- burnduration
  - Type: int
  - Type: 40
  - Set status: Required
  - Role: The duration of the wall
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testfire fire 10 10 20`
