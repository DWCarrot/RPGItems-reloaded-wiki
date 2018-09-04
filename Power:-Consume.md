**instruction:**
`/rpgitem power {Item} consume`

**effect:**
  Set [Item] as a consumable item. Press this button to consume the item

**Attributes:**
- cooldownTime
  - Type: int
  - Set status: additional
  - Role: Set skill cooldown
- isRight
  - Type: boolean
  - Set status: additional
  - Effect: Whether to apply as left button
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testconsume consume`