`/rpgitem help [String]`
------------------------

Shows commands and help for commands that contain `[String]`.  

`/rpgitem [Item]`
-----------------

Prints item `[Item]`’s tool-tip to chat.  

`/rpgitem [String] create`
--------------------------

Create an item with the name `[String]`. The name is what you use to identify the item for later commands e.g: Give. It is not the name of the item on the tool-tip, that is set with `display` instead.  

`/rpgitem [Item] armor [Integer(0-100)]`
----------------------------------------

Sets the item `[Item]`’s armor to `[Integer]`.  


`/rpgitem [Item] armor`
----

Shows the item `[Item]`’s current armor.  


`/rpgitem [Item] damage [Min-Integer] [Max-Integer]`
----

Sets the item `[Item]`’s damage to do random damage between `[Min]` and `[Max]`.  


`/rpgitem [Item] damage [Integer]`
----

Sets the item `[Item]`’s damage to `[Damage]`.  


`/rpgitem [Item] damage`
----

Shows the item `[Item]`’s current damage.  


`/rpgitem [Item] description set [Integer] [String]`
----

Sets the line `[Integer]` to `[String]` on the item `[Item]`.  


`/rpgitem [Item] description remove [Integer]`
----

Removes the line `[Integer]` on the item `[Item]`.  


`/rpgitem [Item] description add [String]`
----

Adds the line `[String]` to the item `[Item]`.  
.  


`/rpgitem [Item] display`
----

Shows the item `[Item]`’s current display name.  
.  
  
`/rpgitem [Item] display [String]  `
----

Sets the item `[Item]`’s display name to `[String]`.  
.  


`/rpgitem [Item] drop [EntityType] [Double]`
----

Sets the chance that `[Item]` will drop from `[EntityType]` to `[Double]`%. 0% prevents it from dropping.  


`/rpgitem [Item] drop [EntityType]`
----

Gets the chance that `[Item]` will drop from `[EntityType]`. 0% means it doesn’t drop.  


`/rpgitem [Item] durability infinite`
----

Sets the durability to infinite. This means the item should never break.  


`/rpgitem [Item] durability togglebar`
----

Toggles the display of the tooltip based durability bar.  


`/rpgitem [Item] durability [Integer]`
----

Sets the durability for the item. The durability is the number of times the item can be used to attack, block damage(armor) or mine.  
.  


`/rpgitem [Item] enchantment`
----

Listing attached enchantments for `[Item]`. 


`/rpgitem [Item] enchantment clone`
----

Clone the enchantments of the item in hand to `[Item]`.  


`/rpgitem [Item] enchantment clear`
----

Remove all attached enchantments from `[Item]`.  
.  


`/rpgitem [Item] give`
----

Gives the item `[Item]` to the user of the command.  


`/rpgitem [Item] give [Player]`
----

Gives the item `[Item]` to the player `[Player]`.  


`/rpgitem [Item] give [Player] [Integer]`
----

Gives `[Integer]` of the item `[Item]` to the player `[Player]`.  
.  

`/rpgitem [Item] hand [String]`
----

Sets the item `[Item]`’s hand text to `[String]`. 
. 

`/rpgitem [Item] hand`
----

Shows the `[Item]`’s current hand.  


`/rpgitem [Item] item`
----

Shows the `[Item]`’s current item.  


`/rpgitem [Item] item [Material] hex [HexColour]`
----

Sets the `[Item]`’s item to `[Material] : [HexColour]`.  


`/rpgitem [Item] item [ItemID] [Integer]`
----

Sets the  `[Item]`’s item to `[ItemID] : [Integer]`.  


`/rpgitem [Item] item [ItemID]`
----

Sets the `[Item]`’s item to `[ItemID]`.  


----
`/rpgitem [Item] item [Material] [Integer]`
----

Sets the `[Item]`’s item to `[Material]` : `[Integer]`.  


`/rpgitem [Item] item [Material]`
----

Sets the item [Item]’s item to [Material].  


`/rpgitem [Item] lore [String]`
----

Sets the item [Item]’s lore to [String].  


----
`/rpgitem [Item] lore`
----

Shows the item [Item]’s current lore.  


`/rpgitem [Item] power arrow`
----

Adds the arrow power to `[Item]` with a default cooldown of 20 ticks (1 second). The arrow power will fire an arrow on right click.  


`/rpgitem [Item] power arrow [Integer]`
----

Adds the arrow power to `[Item]` with a cooldown of `[Integer]` ticks. The arrow power will fire an arrow on right click.  


`/rpgitem [Item] power command [Integer] [left/right] [Display-String] [Command-String] [Permission-String]`
----

Adds the command power to `[Item]` with a cooldown of `[Integer]` ticks. The tooltip will display `[Display]`. The item will run `[Command]` on `[left/right]` click giving the permission `[Permission]` just for the use of the command. Note: If you want spaces in `[Display]`, `[Command]` or `[Permission]` then surround the string with \` e.g: \`/say Hello`.  


`/rpgitem [Item] power command [Integer] [left/right] [Display-String] [Command-String]`
----

Adds the command power to `[Item]` with a cooldown of `[Integer]` ticks. The tooltip will display `[Display]`. The item will run `[Command]` on `[left/right]` click.  



`/rpgitem [Item] power command [Integer] [left/right] [String]`
----

Runs the command on `[left/right]` click. `[String]` is a `|` seperated list of `[display] | [command] | [permission]`. The tool-tip displays `[display]`. `display` and `command` must be separated a `|` symbol. If permission is provided the player will be given the permission just for the use of the item and then it will be removed.  


`/rpgitem [Item] power consume`
----

Adds the consume power to `[Item]`. The consume power will remove the item on right click.  



`/rpgitem [Item] power fireball`
----

Adds the fireball power to `[Item]` with a default cooldown of 20 ticks (1 second). The fireball power will fire an fireball on right click.  


`/rpgitem [Item] power fireball [Integer]`
----

Adds the fireball power to `[Item]` with a cooldown of `[Integer]` ticks. The fireball power will fire an fireball on right click.  


`/rpgitem [Item] power flame`
----

Adds the flame power to `[Item]` with a default burntime of 20 ticks (1 second). The flame power will set the target on fire on hit.  


`/rpgitem [Item] power flame [Integer]`
----

Adds the flame power to `[Item]` with a burntime of `[Integer]` ticks. The flame power will set the target on fire on hit.  
.  

`/rpgitem [Item] power food [Integer]`
----

Adds the food power to `[Item]` that restore `[Integer]` foodpoints when eated. The food power works as if we ate food.
.  

`/rpgitem [Item] power ice [Integer]`
----

Adds the ice power to `[Item]` with a cooldown of `[Iteger]` ticks. The ice power will fire an ice block on right click which will then create a box of ice on impact, the ice will slowly remove itself.  


`/rpgitem [Item] power ice`
----

Adds the ice power to `[Item]` with a default cooldown of 20 ticks (1 second). The ice power will fire an ice block on right click which will then create a box of ice on impact, the ice will slowly remove itself.  


`/rpgitem [Item] power knockup [Integer] [Double]`
----

Adds the knockup power to `[Item]` with a chance of 1/`[Integer]` and a power of `[Double]`. The knockup power will send the hit target flying.  


`/rpgitem [Item] power knockup`
----

Adds the knockup power to `[Item]` with a default chance of 1/20 and a power of 2. The knockup power will send the hit target flying.  


`/rpgitem [Item] power lightning`
----

Adds the lightning power to `[Item]` with a default chance of 1/20. The lightning power will strike the hit target with lightning.  


`/rpgitem [Item] power lightning [Integer]`
----

Adds the lightning power to `[Item]` with a chance of 1/`[Integer]`. The lightning power will strike the hit target with lightning.  


`/rpgitem [Item] power potionhit [Chance-Integer] [Duration-Integer] [Amplifier-Integer] [Effect-String]`
----
 
Adds the potionhit power to `[Item]` with a chance of hitting 1/`[Chance]`. On hit it will apply `[Effect]` for `[Duration]` ticks at power `[Amplifier]`. The list of valid effects can be found [[here|https://github.com/TheCreeperOfRedstone/RPG-Items-2/wiki/Potion-Effects]]


`/rpgitem [Item] power potionself [Cooldown-Integer] [Duration-Integer] [Amplifier-Integer] [Effect-String]`
----

Adds the potionself power to `[Item]` with a cooldown of `[Cooldown]`. On right click it will apply `[Effect]` for `[Duration]` ticks at power `[Amplifier]`.  


`/rpgitem [Item] power potiontick [Integer] [String]`
----

Adds the potiontick power to `[Item]`. The potiontick power will give the wielder of the `[Item]` the `[String]` effect with level `[Integer]` while held/worn.  


`/rpgitem [Item] power rainbow [Cooldown-Integer] [Count-Integer]`
----

Adds the rainbow power to `[Item]` with a cooldown of `[Cooldown]` ticks and a block count of `[Count]`. The rainbow power will fire blocks of coloured wool on right click, the wool will remove itself.  


`/rpgitem [Item] power rainbow`
----

Adds the rainbow power to [Item] with a default cooldown of 20 ticks (1 second) and a block count of 5. The rainbow power will fire blocks of coloured wool on right click, the wool will remove itself.  


`/rpgitem [Item] power rumble [Cooldown-Integer] [Power-Integer] [Distance-Integer]`
----

Adds the runble power to `[Item]` with a cooldown of `[Cooldown]` ticks and a power of `[Power]`, the wave will travel `[Distance]` blocks. The rumble power sends a shockwave through the ground and sends any hit entities flying.  


`/rpgitem [Item] power skyhook [Material] [Integer]`
----

Adds the skyhook power to `[Item]`. The skyhook power will allow the user to hook on to `[Material]` up to `[Integer]` blocks away

`/rpgitem [Item] power teleport [Cooldown-Integer] [Distanc-[Integer]`
----

Adds the teleport power to `[Item]` with a cooldown of `[Cooldown]` ticks (1 second) and teleport distance of `[Distance]` blocks. The teleport will teleport you in the direction you’re looking in.  


`/rpgitem [Item] power teleport`
----

Adds the teleport power to `[Item]` with a default cooldown of 20 ticks (1 second) and teleport distance of 5 blocks. The teleport will teleport you in the direction you’re looking in.  


`/rpgitem [Item] power tntcannon`
----

Adds the tntcannon power to `[Item]` with a default cooldown of 20 ticks (1 second). The tntcannon power will fire active tnt on right click.  


`/rpgitem [Item] power tntcannon [Integer]`
----

Adds the tntcannon power to `[Item]` with a cooldown of `[Integer]` ticks. The tntcannon power will fire active tnt on right click.

`/rpgitem [Item] quality [Quality]`
----

Sets the item `[Item]`’s quality to `[Quality]`.  


`/rpgitem [Item] quality`
----

Shows the item `[Item]`’s current quality.  


`/rpgitem [Item] recipe`
----

Sets the `[Item]`’s recipe.  


`/rpgitem [Item] removerecipe`
----

Removes the `[Item]`’s recipe.  


`/rpgitem [Item] remove`
----

Remove the `[Item]` from the system. This does not currently remove the item from players’ inventories but all powers and damage will stop working on them.  


`/rpgitem [Item] removepower [String]`
----

Removes power `[String]` from `[Item]`.

`/rpgitem [Item] type`
----

Shows the `[Item]`’s current type.  


`/rpgitem [Item] type [String]`
----

Sets the item `[Item]`’s type to `[String]`.  


`/rpgitem [Item] worldguard`
----

Toggles worldguard override on the `[Item]`.  


`/rpgitem list`
----

Shows a list of all created items.  


`/rpgitem option giveperms`
----

Toggles give requiring permissions.  


`/rpgitem option worldguard`
----

Toggles worldguard support. Currently if enabled it prevents RPG Items from being used in non-pvp area.
