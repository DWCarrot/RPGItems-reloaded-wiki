**instruction:**
`/rpgitem power {Item} torch {cooldownTime}`

**effect:**
 Adds lighting ability to {Item}, cooling time is {cooldownTime}, throws a bunch of torches at the pointed area, and the torch will be thrown on the corresponding square

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set status: Required
  - Role: Cooling time
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testtorch torch 20`