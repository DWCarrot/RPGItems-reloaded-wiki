**instruction:**
`/rpgitem power {Item} rainbow [cooldownTime] [count] [isFire]`

**effect:**
  Add Rainbow skill to {Item}, [cooldownTime] for game engrave. [count] is the number of colored squares to be fired. [IsFire] is whether fire box is fired in place of wool

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 20
  - Setting status: optional
  - Role: Cooling time
- count
  - Type: int
  - Default: 5
  - Setting status: optional
  - Role: Number of shots
- isFire
  - Type: boolean
  - Default: false
  - Setting status: optional
  - Role: whether to replace the fire as a flame
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpumpkin rainbow`
