# Skill instruction set

`/rpgitem power {item} {power} [properties......]`
**Attributes**
- item: item id e.g.: testitem-> an item with id testitem
- power: skill id e.g.: potionself-> give yourself a buff
- properties
  - Category:
    - Required: Must be specified when power is created, denoted by `{}`
    - Optional: Can be specified when power is created, denoted by `[]`
    - Additional: Can only be set by set, not displayed in the properties set by the instruction, using `<>`
  - Function: The skill can be initialized with the parameters eg: Take potionself as an example. Available parameters are [cooldown] [duration] [amplifier] [effect]. The entire command is similar to this: `/rpgitem power testpotionself 20 100 1 speed` The player is then given a level 2 speed buff (cd:1s) for 5 seconds. See the detailed power variable settings below for each parameter unit.

# Ordinary skills
## AOE
**instruction:**
`/rpgitem power {Item} aoe {cooldown} {range} {effect} {duration} {amlifier} [selfapplication]`

**effect:**
Add a range effect to [Item] with a cooldown of [Cooldown] ticks. Right-click on all entities in the range [Effect] to [range]# that will apply [Duration] ticks and the effect level is [Amplifier]. If [ Self] is not set, this effect is also applied to the release by default

**Attributes**
- cooldownTime
  - Type: long
  - Set status: Required
  - Role: Set skill cooldown
- range
  - Type: int
  - Set status: Required
  - Role: Setting range
- effect
  - Type: String
  - Set status: Required
  - Role: Sets the effect character. Please refer to [Potion System] for details (https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88 %E6%9E%9C) chapter
- duration
  - Type: int
  - Set status: Required
  - Role: Set duration
- amlifier
  - Type: int
  - Set status: Required
  - Role: Set skill level, level = amlifier +1
- selfapplication
  - Type: boolean
  - Setting status: optional
  - Role: whether to set effect on itself
- name
  - Type: String
  - Set status: additional
  - Function: Set display name
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testaoe aoe 10 10 speed 100 0 true`



## Arrow
**Instructions:**
`/rpgitem power {Item} arrow [Cooldown]`

**effect:**
Add Rocket ability to [Item], cooldown [Cooldown] ticks.

**Attributes** 
- cooldownTime
  - Type: long
  - Setting status: optional
  - Role: Set skill cooldown
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testarrow arrow 20`

## Attract
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

## Color
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testarrow color 100 true false true`

## Consume
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testconsume consume`

## ConsumeHit
**instruction:**
`/rpgitem power {Item} consumehit`

**effect:**
  Set [Item] as the consumable when attacking. Cooling time defaults to 0, which can be modified via setter.

**Attributes**
- cooldownTime
  - Type: int
  - Set status: additional
  - Role: Set skill cooldown

**Example**
`/rpgitem power testconsumehit consumehit`

## Deflect
**instruction:**
`/rpgitem power {Item} deflect [facing] [initiative] [cooldownTime] [passive] [cooldownTimePassive]`

**effect:**
  Bounced arrows and fireballs (rebound)!

  When the parameter setting [initiative] is true and [passive] is false and the skill has been cooled ([cooldownTime] is zero), you can set the left and right keys to trigger reflection of the flying prop in [duration] time. The current player is heading

  When the parameter setting [initiative] is false and [passive] is true, there is a probability of <chance>% when the skill trigger interval [cooldownTimePassive] returns to zero. The flight prop is reflected to the direction the current player is facing. on
  

**Attributes:**
- facing
  - Type: double
  - Default: 30
  - Setting status: optional
  - Effect: Maximum capture angle (angle between current sight and flight prop)
- initiative
  - Type:initiative
  - Default: true
  - Setting status: optional
  - Role: Active mode (need to trigger actively)
- cooldownTime
  - Type: int
  - Default: 20 moments
  - Setting status: optional
  - Role: skill cooldown (when active mode is true)
- passive
  - Type: boolean
  - Default: false
  - Setting status: optional
  - Role: whether to enable passive mode
- cooldownTimePassive
  - Type: int
  - Default: 20 moments
  - Setting status: optional
  - Effect: Interval for triggering the skill (in case of passive mode, if the passive is true)
- chance
  - Type: int
  - Default: 50
  - Set status: additional
  - Role: Sets the chance for the skill to trigger in passive mode (<chance>%)
- isRight
  - Type: boolean
  - Default: true
  - Set status: additional
  - Role: active mode is left or right trigger, true is the right
- duration
  - Type: int
  - Default: 50 moments
  - Set status: additional
  - Function: setting the anti-active time in active mode
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testdeflect deflect`

## Fire
**instruction:**
`/rpgitem power {Item} fire {cooldownTime} {distance} {burnduration}`

**effect:**
  Adds a fire ability to {item}, which fires the flame on the right and causes a {distance} duration {burnduration} wall and cooling time {cooldownTime} ticks when touching the first square.

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set status: Required
  - Role: Set skill cooldown
- distance
  - Type: int
  - Type: 15
  - Set status: Required
  - Role: The distance of the fire wall
- burnduration
  - Type: int
  - Type: 40
  - Set status: Required
  - Role: The duration of the wall
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testfire fire 10 10 20`


## Fireball
**instruction:**
`/rpgitem power {Item} fireball [cooldownTime] `

**effect:**
  Fire small fireball [cooldownTime]tick cooling time.

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set status: Required
  - Role: Set skill cooldown
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testfire fireball`

## Flame
**instruction:**
`/rpgitem power {Item} Flame [burnTime]`

**effect:**
  Inflicts [burnTime]tick ignition time on the target.

**Attributes:**
- burnTime
  - Type: int
  - Default: 20
  - Setting status: optional
  - Role: Ignite time
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testflame Flame`

## Food
**instruction:**
`/rpgitem power {Item} food {foodpoints} `

**effect:**
   Add edible features to {Item} and change {foodpoints} to hunger when eaten.

**Attributes:**
- foodpoints
  - Type: int
  - Default: None
  - Set status: Required
  - Role: Changing hunger

**Example**
`/rpgitem power testflame food 10`

## ForceField
**instruction:**
`/rpgitem power {Item} forcefield {cooldownTime} {radius} {height} {base} {ttl}`

**effect:**
   Set around you a circle {radius} that prevents all entities from entering, a height of {height}, a depth of {base} and a field of force of {ttl} seconds, and a cool cylinder of the cooldown time {cooldownTime}tick.

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 200
  - Set status: Required
  - Role: Skill cooldown
- radius
  - Type: int
  - Default: 5
  - Set status: Required
  - Function: Set the cylinder radius
- height
  - Type: int
  - Default: 30
  - Set status: Required
  - Function: Set the cylinder height
- base
  - Type: int
  - Default: -15
  - Set status: Required
  - Function: Set the cylinder depth offset
- ttl
  - Type: int
  - Default: 100
  - Set status: Required
  - Role: Set duration
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testforcefield forcefield 10 10 10 0 40`

## Ice
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testice knockup 10`

## Knockup (failed to be repaired)
**instruction:**
`/rpgitem power {Item} knockup [chance] [power]`

**effect:**
   Add a flying skill to {Item} with a probability of 1/[chance] and a power of [power]. Flying a skill will fly the target.

**Attributes:**
- chance
  - Type: int
  - Default: 20
  - Setting status: optional
  - Role: Ability chance
- power
  - Type: double
  - Default: 2
  - Setting status: optional
  - Role: The power of skills
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testknockup knockup`

## LifeSteal
** Instruction: **
`/rpgitem power {Item} lifesteal [chance]`

**effect:**
   Add life stealing skills to {Item}, steal chance [chance]

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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testlifesteal lifesteal`

## Lightning
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testlightning lifesteal`

## Particle
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testparticle particle FLAME`

## ParticleTick
**instruction:**
`/rpgitem power {Item} particletick {effect} [interval]`

**effect:**
  Add particle effects to {Item}. When held, creates particles around the player. The interval is [interval]tick. {effect} can be one of SMOKE/ENDER_SIGNAL/MOBSPAWNER_FLAMES.

**Attributes:**
- effect
  - Type: String
  - Default: FLAME
  - Set Status: Required
  - Role: Particle type
- interval
  - Type: int
  - Default: 15
  - Setting status: optional
  - Effect: Trigger interval
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter


**Example**
`/rpgitem power testparticletick particletick FLAME 20`

## PotionHit
**instruction:**
`/rpgitem power {Item} potionhit {chance} {dration} {amplifier} {type}`

**effect:**
  There is a 1/{chance}% chance of attack to get a potion effect. {type} is a potion effect {dration} is the duration in gameplay, {amplifier}
      Is an integer. Potions available: See the [Pharmacy System] for details (https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E% 9C) Chapter

**Attributes:**
- chance
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Trigger probability
- dration
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Duration
- amplifier
  - Type: int
  - Default: 1
  - Set Status: Required
  - Role: Potion effect level
- type
  - Type: String
  - Default: HARM
  - Set Status: Required
  - Role: Potion effect: See [Potion System] for details (https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6% 9E%9C) chapter
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpotionhit potionhit 1 100 1 speed `

## PotionSelf
**instruction:**
`/rpgitem power {Item} potionself {cooldownTime} {duration} {amplifier} {type}`

**effect:**
  Right-click on the {type} potion effect of level {amplifier} for {duration} game moments, and cooldown time. Potions available: See the [Pharmacy System] for details (https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E% 9C) Chapter

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- dration
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Duration
- amplifier
  - Type: int
  - Default: 1
  - Set Status: Required
  - Role: Potion effect level
- type
  - Type: String
  - Default: HARM
  - Set Status: Required
  - Role: Potion effect: See [Potion System] for details (https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6% 9E%9C) chapter
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpotionself potionself 100 100 1 speed `

## PotionTick
**instruction:**
`/rpgitem power {Item} potiontick {amplifier} {effect} [interval] [duration]`

**effect:**
  When the player holds/wears, the {effect} effect with the duration of [duration] game engraved with {amplifier} is given again each time [interval] game is engraved. Potions available: See the [Pharmacy System] for details (https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E% 9C) Chapter

**Attributes:**
- amplifier
  - Type: int
  - Default: 1
  - Set Status: Required
  - Role: Potion effect level
- effect
  - Type: String
  - Default: SPEED
  - Set Status: Required
  - Role: Potion effect: See [Potion System] for details (https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6% 9E%9C) chapter
- interval
  - Type: int
  - Default: 0
  - Setting status: optional
  - Role: potion effect cycle trigger interval
- duration
  - Type: int
  - Default: 60
  - Setting status: optional
  - Role: potency effect duration
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpotiontick potiontick 1 speed `

## Projectile
**instruction:**
`/rpgitem power {Item} projectile {cooldownTime} {cone} {projectileType} [range] [amount] [speed]`

**effect:**
{cone} is true: Adds a spelling entity skill to {Item} with cooldown time of {cooldownTime}. Right-click to [amount] {projectileType} type entities flying at [speed] speed. Centered on the player's direction, the angle [range] is randomly distributed in a conical shape. Acceptable types: skull, fireball, snowball, smallfireball, arrow, llamaspit

{cone} is false: Add launch entity skills for {Item} with cooldown time of {cooldownTime}. Right-click to [amount] {projectileType} type entities flying at [speed] speed. Acceptable types: skull, fireball, snowball, smallfireball, arrow, llamaspit

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- cone
  - Type: boolean
  - Default: false
  - Set Status: Required
  - Role: Is the transmission range cone-shaped?
- projectileType
  - Type: String
  - Default: Snowball
  - Set Status: Required
  - Role: Type of Launcher
- range
  - Type: int
  - Default: 15
  - Setting status: optional
  - Role: Range of emission range angle
- amount
  - Type: int
  - Default: 5
  - Setting status: optional
  - Role: The number of launches
- speed
  - Type: double
  - Default: 1
  - Setting status: optional
  - Role: Launch speed
- Gravity
  - Type: boolean
  - Default: true
  - Set status: additional
  - Role: whether it is affected by gravity
- burstCount
  - Type: int
  - Default: 1
  - Set status: additional
  - Role: Number of consecutive triggered skills
- burstInterval
  - Type: int
  - Default: 1
  - Set status: additional
  - Role: Releases consecutive triggered skill intervals at once
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testprojectile projectile 1 true arrow 10 10 2 `

## Pumpkin
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpumpkin pumpkin 1 1`

## Rainbow
**instruction:**
`/rpgitem power {Item} rainbow [cooldownTime] [count] [isFire]`

**effect:**
  Add Rainbow skill to {Item}, [cooldownTime] for game engrave. [count] is the number of colored squares to be fired. [IsFire] is whether fire box is fired in place of wool

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 20
  - Setting status: optional
  - Role: Cooling time
- count
  - Type: int
  - Default: 5
  - Setting status: optional
  - Role: Number of shots
- isFire
  - Type: boolean
  - Default: false
  - Setting status: optional
  - Role: whether to replace the fire as a flame
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testpumpkin rainbow`

## RealDamage
**instruction:**
`/rpgitem power {Item} realdamage {cooldownTime} {realDamage}`

**effect:**
  Adds real damage ability to {Item}, {cooldownTime} is engraved for the game. Creatures that are hit will have real damage from {realDamage} but at least <minDamage> points remaining.

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- realDamage
  - Type: double
  - Default: 0
  - Set Status: Required
  - Role: Real damage value
- minDamage
  - Type: double
  - Default: 0
  - Set status: additional
  - Role: Target minimum residual blood volume
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testrealdamage realdamage 1 10`

## Rescue
**instruction:**
`/rpgitem power {Item} rescue [cooldownTime] [healthTrigger] [useBed] [inPlace]`

**effect:**
  Adds salvation skills to {Item}, cooling time is [cooldownTime] game moments, saves when the player's blood volume is lower than the [healthTrigger] trigger, [useBed] is true, and returns to the origin when [inPlace] is true. Resurrection is invincible. Priority [inPlace]> [useBed]

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 20
  - Setting status: optional
  - Role: Cooling time
- healthTrigger
  - Type: int
  - Default: 4
  - Setting status: optional
  - Role: Rescue triggers minimum blood volume
- useBed
  - Type: boolean
  - Default: true
  - Setting status: optional
  - Role: whether to send back to the body
- inPlace
  - Type: boolean
  - Default: false
  - Setting status: optional
  - Role: whether to revive in situ
- damageTrigger
  - Type: double
  - Default: 1024
  - Set status: additional
  - Effect: How much damage is triggered above
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testrescue rescue`

## Rumble
**instruction:**
`/rpgitem power {Item} rumble {cooldownTime} {power} {distance}`

**effect:**
  Adds bandit ability to {Item}, cooldown time is {cooldownTime}, effective range is {distance}, explosion around the first entity touched by the bandit advances and will be the same around small area The entity hits the sky with a {power} strike level.

**Attributes:**
- cooldownTime
  - Type: int
  - Default: 20
  - Set Status: Required
  - Role: Cooling time
- power
  - Type: int
  - Default: 2
  - Set Status: Required
  - Role: Hit level
- distance
  - Type: int
  - Default: 15
  - Set Status: Required
  - Role: advance distance
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testrumble rumble 100 4 10`

## SkyHook
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testskyhook skyhook 1 10`

## TNTCannon
**instruction:**
`/rpgitem power {Item} tntcannon [cooldownTime]`

**effect:**
 Adding tnt to {Item} with cooldown [cooldownTime]

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Setting status: optional
  - Role: Cooling time
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testtntcannon tntcannon`

## Teleport
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testteleport teleport 20 10`

## TippedArrow
**instruction:**
`/rpgitem power {Item} tippedarrow {cooldownTime} {type} {duration} {amplifier} `

**effect:**
 Adds drug arrow skill to {Item}, effect {type} duration{duration} is game engraved, level is {amplifier}, cooldown time is {cooldownTime} game moment. Right shot launch. Effective potion effect: see [Potion system] for details ( https://github.com/NyaaCat/RPGitems-reloaded/wiki/%E8%8D%AF%E6%B0%B4%E6%95%88%E6%9E%9C) Chapter

**Attributes:**
- cooldownTime
  - Type: long
  - Default: 20
  - Set status: Required
  - Role: Cooling time
- type
  - Type: String
  - Default: null
  - Set status: Required
  - Role: potion effect type
- duration
  - Type: int
  - Default: 15
  - Set status: Required
  - Role: Duration
- amplifier
  - Type: int
  - Default: 1
  - Set status: Required
  - Role: Effect Level
- consumption
  - Type: int
  - Default: 0
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testtippedarrow tippedarrow 20 speed 40 1`

## Torch
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
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testtorch torch 20`

# Special skills (command series)

## aoecommand

**instruction:**
`/rpgitem power {Item} aoecommand {cooldown} {isRight} {display} {command} {rm} {r} {facing} [permission]`

**effect:**
Add AOE command skill to {Item}. Cooling time is {cooldown}. If {isRight} is right, right-click trigger otherwise left click. Tooltip is {display}. {command} will be after {isRight} ({rm} ~ {r} entities running within the {facing} perspective) need to run {permission} for this {command} for the corresponding role

**Attributes**
- cooldownTime
  - Type: long
  - Set status: Required
  - Role: Set skill cooldown
- isRight
  - Type: left/right
  - Set status: Required
  - Role: Set left or right
- display
  - Type: string
  - Set status: Required
  - Function: Set skill description characters
- command
  - Type: string
  - Set status: Required
  - Role: Sets the command when the skill is triggered (can be any minecraft command box or executable command entered in the chat box)
  - Special conversions: fixed strings that can be replaced with certain special values ​​in instructions
    - User:
      - `{player}` : Can be converted to current user name
      - `{player.x}`: convertible to the current user's x coordinate
      - `{player.y}`: Can be converted to the current user's y-coordinate
      - `{player.z}`: can be converted to the current user's z coordinate
      - `{player.yaw}`: Can be converted to the current user's horizon
      - `{player.pitch}`: Can be converted to feed the current user's line of sight elevation
    - Performed by:
      - `{entity}`: the name of each executed person (note that the name is, for example, a zombie, it is called `zombie`)
      - `{entity.x}` : the x coordinate of each performee
      - `{entity.y}` : the y coordinate of each performee
      - `{entity.z}` : the z coordinate of each performee
      - `{entity.yaw}` : horizontal angle of view of each subject’s gaze
      - `{entity.pitch}` : The elevation of the gaze of each subject
      - `{entity.uuid}` : uuid of each performer
    - #### conversion does not support operations, eg `{player.yaw}+90` is not feasible
- rm
  - Type: int
  - Default: 0
  - Set status: Required
  - Role: The minimum radius of the enemy's range
- r
  - Type: int
  - Default: 10
  - Set status: Required
  - Function: The maximum radius of the enemy enemy range
- facing
  - Type: int
  - Default: 30
  - Set status: Required
  - Function: User's current line of sight deflection angle (cone range)
- permission
  - Type: string
  - Setting status: optional
  - Role: Permissions node required by the user when executing {command} (only single node is supported, multiple nodes are not supported, `*` is assigned op permission)
- c
  - Type: int
  - Set status: additional
  - Default: 100
  - Role: Set the maximum number of trapped performers
- mustsee
  - Type: boolean
  - Set status: additional
  - Default: false
  - Role: Applies only to entities that are viewed by the player
- selfapplication
  - Type: boolean
  - Set status: additional
  - Default: false
  - Role: whether the instruction acts on the user itself
- type
  - Type: entity/player/mobs
  - Set status: additional
  - Default: entity
  - Role: Command Action Type
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
```
/rpgitem testaoecommand power aoecommand 20 right `say hello` `/say {entity} hello` 0 20 360 minecraft.command.say
```
**Effective**: Let the user speak for all entities of type LivingEntity in the 0-20 range: (entity name) hello.

**Note 1**: Note that the user of this instruction is the user himself. If the relative position `~` symbol is used, it is calculated based on the user's current position rather than the position of each executed person. And the number of times the instruction is executed is the same as the number of executed persons captured by the current skill.

**Note 2**: Some instructions (such as ʻexecute`) have permissions that can be overridden and require special attention.


## command

**instruction:**
`/rpgitem power {Item} command {cooldown} {isRight} {display} {command} [permission]`

**effect:**
Adds a command skill to {Item} with a cooldown of {cooldown}. The tooltip is {display}. {command} will be run after {isRight}(left/right) and given the [permission] to run this {command}. ***Note ***: If you want to use spaces in {display} or {command} or [permission], then add the ` symbol around the string. For example: `/say Hello`

- cooldownTime
  - Type: long
  - Set status: Required
  - Role: Set skill cooldown
- isRight
  - Type: left/right
  - Set status: Required
  - Role: Set left or right
- display
  - Type: string
  - Set status: Required
  - Function: Set skill description characters
- command
  - Type: string
  - Set status: Required
  - Role: Sets the command when the skill is triggered (can be any minecraft command box or executable command entered in the chat box)
  - Special conversions: fixed strings that can be replaced with certain special values ​​in instructions
    - User:
      - `{player}` : Can be converted to current user name
      - `{yaw}`: Can be converted to the current user's horizontal line of sight
      - `{pitch}`: Can be converted to feed the current user's line of sight elevation
    - #### conversion does not support operations, eg `{yaw}+90` is not feasible
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
```
/rpgitem testcommand power command 20 right `say hello` `/say hello` minecraft.command.say
```
**Effective**: Let users play hello on the chat channel.

**Notes**: Some instructions (such as `execute`) have permissions that can be overridden and require special attention.

## commandhit

**instruction:**
`/rpgitem power {Item} commandhit {cooldown} {display} {command} [permission]`

**effect:**
Add a hit command skill to {Item}. The cooldown is {cooldown}. The tooltip is {display} . {command} will be executed after hitting the target and given the {permission} of {command}.
***Note ***: If you want to enter spaces in {display} or {command} or [permission], then add the ` symbol around the string. For example: `/say Hello`
- cooldownTime
  - Type: long
  - Set status: Required
  - Role: Set skill cooldown
- isRight
  - Type: left/right
  - Set status: Required
  - Role: Set left or right
- display
  - Type: string
  - Set status: Required
  - Function: Set skill description characters
- command
  - Type: string
  - Set status: Required
  - Role: Sets the command when the skill is triggered (can be any minecraft command box or executable command entered in the chat box)
  - Special conversions: fixed strings that can be replaced with certain special values ​​in instructions
    - User:
      - `{player}` : Can be converted to current user name
      - `{player.x}`: convertible to the current user's x coordinate
      - `{player.y}`: Can be converted to the current user's y-coordinate
      - `{player.z}`: can be converted to the current user's z coordinate
      - `{player.yaw}`: Can be converted to the current user's horizon
      - `{player.pitch}`: Can be converted to feed the current user's line of sight elevation
    - Performed by:
      - `{entity}`: the name of each executed person (note that the name is, for example, a zombie, it is called `zombie`)
      - `{entity.x}` : the x coordinate of each performee
      - `{entity.y}` : the y coordinate of each performee
      - `{entity.z}` : the z coordinate of each performee
      - `{entity.yaw}` : horizontal angle of view of each subject’s gaze
      - `{entity.pitch}` : The elevation of the gaze of each subject
      - `{entity.uuid}` : uuid of each performer
    - #### conversion does not support operations, eg `{player.yaw}+90` is not feasible
- minDamage
  - Type: int
  - Set status: additional
  - Default: 0
  - Role: Minimal trigger damage
- consumption
  - Type: int
  - Set status: additional
  - Role: Consumption, see the [New Consumption System] (https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
```
/rpgitem testcommandhit power commandhit 20 `say hello` `/say {entity} hello` minecraft.command.say
```
**Effect**: Let users play hello to the attacked person in the chat channel.

**Notes**: Some instructions (such as `execute`) have permissions that can be overridden and require special attention.