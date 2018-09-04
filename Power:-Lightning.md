**instruction:**
`/rpgitem power {Item} lightning [chance]`

**effect:**
   Lightning ability added to {Item}, the default chance is 1/[chance]. A chance to generate lightning when attacking a target.

**Attributes:**
- chance
  - Type: int
  - Default: 20
  - Setting status: optional
  - Role: Ability chance
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testlightning lightning`