**instruction:**
`/rpgitem power {Item} teleport [cooldownTime] [distance]`

**effect:**
 Add a transfer skill to {Item}, CooldownTime [cooldownTime] game moment Right-handed transmission distance is [distance] grid. The direction of transmission is the direction you are facing.

**feture**
 This skill is used when the material of the carrier is a bow and arrow, it will become the position where the arrow is sent to the shooter, and if the distance from the player to the ground is greater than [distance], it will prompt too far.

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Setting status: optional
  - Role: Cooling time
- distance
  - Type: int
  - Default: 5
  - Setting status: optional
  - Role: transmission distance
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testteleport teleport 20 10`