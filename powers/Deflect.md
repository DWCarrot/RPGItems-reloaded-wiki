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
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
`/rpgitem power testdeflect deflect`
