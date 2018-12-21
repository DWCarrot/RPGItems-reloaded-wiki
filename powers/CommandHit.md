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
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
```
/rpgitem testcommandhit power commandhit 20 `say hello` `/say {entity} hello` minecraft.command.say
```
**Effect**: Let users play hello to the attacked person in the chat channel.

**Notes**: Some instructions (such as `execute`) have permissions that can be overridden and require extra attention.
