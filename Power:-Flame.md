**instruction:**
`/rpgitem power {Item} Flame [burnTime]`

**effect:**
  Inflicts [burnTime]tick ignition time on the target.

**Attributes:**
- burnTime
  - Type: int
  - Default: 20
  - Setting status: optional
  - Role: Ignite time
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testflame Flame`