**Instructions:**
`/rpgitem power {Item} attract {radius} {maxspeed}`

**effect:**
Add skills for {Item}. When you hold it in your hand, pull the creature near the player. Radius {radius} grid, max speed {maxspeed}

**Attributes** 
- radius
  - Type: int
  - Set status: Required
  - Role: Set the maximum radius of skill pull
- maxSpeed
  - Type: double
  - Set status: Required
  - Role: Set the maximum pulling speed of the skill
**Example**
`/rpgitem power testarrow attract 20 0.1