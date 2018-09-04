**instruction:**
`/rpgitem power {Item} skyhook {railMaterial} {hookDistance}`

**effect:**
 Adds a hook skill to {Item}. The hook ability allows the user to hook into a specified {railMaterial} material square within a distance of {hookDistance} and advance in that direction.

**Attributes:**
- railMaterial
  - Type: String
  - Default: None
  - Set Status: Required
  - Role: Material ID that can be pointed to
- hookDistance
  - Type: int
  - Default: 10
  - Set Status: Required
  - Role: Change the minimum distance from the material block to the player
- cooldownTime
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- hookingTickCost
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: The consumption of flying 1 game in each tick
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testskyhook skyhook 1 10`