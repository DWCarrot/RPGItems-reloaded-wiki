**instruction:**
`/rpgitem power {Item} tntcannon [cooldownTime]`

**effect:**
 Adding tnt to {Item} with cooldown [cooldownTime]

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Setting status: optional
  - Role: Cooling time
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testtntcannon tntcannon`