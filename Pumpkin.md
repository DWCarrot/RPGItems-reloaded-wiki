**instruction:**
`/rpgitem power {Item} pumpkin {chance} {drop}`

**effect:**
   1/{chance}% Chance to put the enemy on a pumpkin head, with a 1/{drop}% chance to drop the pumpkin head

**Attributes:**
- chance
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Trigger probability
- drop
  - Type: double
  - Default: 0
  - Set Status: Required
  - Role: Pumpkin Drop Chance
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpumpkin pumpkin 1 1`