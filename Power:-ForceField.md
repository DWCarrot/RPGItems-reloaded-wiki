**instruction:**
`/rpgitem power {Item} forcefield {cooldownTime} {radius} {height} {base} {ttl}`

**effect:**
   Set around you a circle {radius} that prevents all entities from entering, a height of {height}, a depth of {base} and a field of force of {ttl} seconds, and a cool cylinder of the cooldown time {cooldownTime}tick.

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 200
  - Set status: Required
  - Role: Skill cooldown
- radius
  - Type: int
  - Default: 5
  - Set status: Required
  - Function: Set the cylinder radius
- height
  - Type: int
  - Default: 30
  - Set status: Required
  - Function: Set the cylinder height
- base
  - Type: int
  - Default: -15
  - Set status: Required
  - Function: Set the cylinder depth offset
- ttl
  - Type: int
  - Default: 100
  - Set status: Required
  - Role: Set duration
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testforcefield forcefield 10 10 10 0 40`
