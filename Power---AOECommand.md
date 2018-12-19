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
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
```
/rpgitem testaoecommand power aoecommand 20 right `say hello` `/say {entity} hello` 0 20 360 minecraft.command.say
```
**Effective**: Let the user speak for all entities of type LivingEntity in the 0-20 range: (entity name) hello.

**Note 1**: Note that the user of this instruction is the user himself. If the relative position `~` symbol is used, it is calculated based on the user's current position rather than the position of each executed person. And the number of times the instruction is executed is the same as the number of executed persons captured by the current skill.

**Note 2**: Some instructions (such as ʻexecute`) have permissions that can be overridden and require extra attention.
