**Full Name:** rpgitems:airborne

## Description

Do `percentage`% more but less than `cap` damage when gliding.

## Properties

* `percentage`

  * Type: int
  * Default: 50

  Damage increase percentage.

* `cap`

  * Type: double
  * Default: 300

  Maximum damage should this power do.

## Example

`/rpgitem item power rpgitems:airborne percentage:100 cap:20`
Increase your damage by 100% but no more than 20.

## Note

If origin damage already great than `cap`, this power is no-op.