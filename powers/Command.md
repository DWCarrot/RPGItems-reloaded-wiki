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
  - Role: Consumption, see the [New Consumption System](https://github.com/NyaaCat/RPGitems-reloaded/wiki/New-durability-system) chapter

**Example**
```
/rpgitem testcommand power command 20 right `say hello` `/say hello` minecraft.command.say
```
**Effective**: Let users play hello on the chat channel.

**Notes**: Some instructions (such as `execute`) have permissions that can be overridden and require extra attention.
