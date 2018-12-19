**instruction:**
`/rpgitem power {Item} fireball [cooldownTime] `

**effect:**
  Fire small fireball [cooldownTime]tick cooling time.

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set status: Required
  - Role: Set skill cooldown
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testfire fireball`