# Command

`/rpgitem {item} power {power} [properties……]`

* `item`：the item id e.g. testitem -> an item with id `testitem`
* `power`：the power id e.g. potionself -> issue an potion effect for yourself when use with right click
* properties
  * types
    * required: The required arguments when adding the power, quotes with `{}` marks.
    * optional: Optional arguments available when adding the power, quotes with `[]` marks.
    * addition: Only available via `set` command and will not be shown when adding powers, quotes with `<>` marks.
  * usage: initialize the power added to the item. For example, power `potionself` comes with the following optional arguments `[cooldown] [duration] [amplifier] [effect]`. The full command looks like this: `/rpgitem testpotionself power 20 100 1 speed`, when right click with this item (use), the user will be applied 'speed 2' potion effect, keep for 5 seconds and it need 1 second to cool down.
