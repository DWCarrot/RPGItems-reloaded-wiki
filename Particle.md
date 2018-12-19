**instruction:**
`/rpgitem power {Item} particle {effect}`

**effect:**
   Add particle effects to {Item}. When right-clicking, particles are created around the player. {effect} can be one of SMOKE/ENDER_SIGNAL/MOBSPAWNER_FLAMES

**Attributes:**
- effect
  - Type: String
  - Default: FLAME
  - Set Status: Required
  - Role: Particle type
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testparticle particle FLAME`