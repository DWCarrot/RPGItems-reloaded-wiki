**instruction:**
`/rpgitem power {Item} ice [cooldownTime]`

**effect:**
   Add ice cube shooting skills to {Item} CooldownTime tick. Right-click on the ice cube to create a mass of ice cubes that impact the target and the ice will slowly disappear.

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Setting status: optional
  - Role: Skill cooldown
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testice ice 10`