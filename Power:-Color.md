**Instructions:**
`/rpgitem power {Item} color [Cooldown] [glass] [clay] [wool]`

**effect:**
 Change the color of clay, glass and wool ([Cooldown] seconds cool)

**Attributes** 
- cooldownTime
  - Type: long
  - Setting status: optional
  - Role: Set skill cooldown
- glass
  - Type: boolean
  - Setting status: optional
  - Function: setting whether to act on glass
- clay
  - Type: boolean
  - Setting status: optional
  - Role: Set whether to act on clay
- wool
  - Type: boolean
  - Setting status: optional
  - Role: setting whether to act on wool
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testarrow color 100 true false true`