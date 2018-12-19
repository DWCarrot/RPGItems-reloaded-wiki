#### `/rpgitem [ITEM] create`

Creates the `[ITEM]`.

#### `/rpgitem [ITEM]`

Preview the item.

#### `/rpgitem [ITEM] give` | `/rpgitem [ITEM] give [player] [amount]`

Give you the item or give specified player an amount of such items.

#### `/rpgitem [ITEM] armour` | `/rpgitem [ITEM] armour [armour value|int[0-100]]`

Show/set item armour value. The armour reduce a percent of damage taken.

Note: Multiple armor with such attributes calculates as "times". E.g., helmet armour 10%, leggings armour 15%, total damage taken = damage amount x 0.9 x 0.85.

#### `/rpgitem [ITEM] clone [ITEM2]`

Clone `ITEM` as `ITEM2`, use to quickly create a bunch of similar items or a series items.

#### `/rpgitem [ITEM] cost [options]`

Set item cost values. See [Durability Mechanism](./Commands:-Durability-Mechanism).

Available options:

* `breaking` | `breaking [value|integer]` - Show/set durability cost when breaking block using this item.
* `hit` | `hit [value|integer]` - Show/set durability cost when being hit with this item.
* `hit toggle` - Toggle cost status of being hit with this item.
* `hitting` | `hitting [value|integer]` - Show/set durability cost when hit other entities with this item.

Note: values can be negative, thus hit/hitting/breaking will increase item durability.

E.g., hit someone with `blade_item` to gain 2 durability each time:

```
/rpgitem blade_item cost hitting -2
```

#### `/rpgitem [ITEM] customItemModel`

Use custom item mode.

#### `/rpgitem [ITEM] damage` | `/rpgitem [ITEM] damage [option]`

Show/set item damage value. Available options:

* `[value]` - Set damage to a fixed value. `/rpgitem test_item damage 15`
* `[min] [max]` - Set damage to a random value in a range. `/rpgitem test_item damage 10 20`

#### `/rpgitem [ITEM] damageMode`

Toggle item damage mode. Use this command to change item damage mode to next option. Available options:

* Fixed (default) - Fixed RPGItem damage, enchants will not work, but status/potion effects will apply
* Vanilla - Use minecraft vanilla damage calculation w/ enchants
* Additional - Use minecraft vanilla damage plus RPGItem damage calculation. Enchants/effects will apply

#### `/rpgitem [ITEM] durability [options]`

Set item durability to `value`. Available options:

* `[value]` - Set durability to `value` - `/rpgitem test_item durability 100`
* `infinite` - Set durability to infinite - `/rpgitem test_item durability infinite`
* `togglebar` - Set durability bar to force show/hide

#### `/rpgitem [ITEM] durabilitybound [minimum] [maximum]`

Set item durability lower and upper bounds. This controls whether and how a power will be executed.

```
/rpgitem test_item durabilitybound 10 100
```

* When item durability is 9, powers with positive `consumption` attribute value will not be executed.
* When item durability is 101, powers with negative `consumption` attribute value will not be executed.
* When item durability is 50, all powers will/can be executed.

#### `/rpgitem [ITEM] durabilityinfo`

Show the item durability information.

#### `/rpgitem [ITEM] description add [text]`

Add `text` to item description/lore. Formatting codes are supported with `&` symbol.

#### `/rpgitem [ITEM] description set [line|int[0~]] [text]`

Set item description to `text` on a specified line. Line number starts from 0.

#### `/rpgitem [ITEM] description remove [line|int[0~]]`

Remove item description of specified line. Line number starts from 0.

#### `/rpgitem [ITEM] display` | `/rpgitem [ITEM] [value]`

Set item name to `value`. Formatting code supported with `&` symbol.

```
/rpgitem test_item display &bHidden Blade
```

#### `/rpgitem [ITEM] drop [EntityType]` | `/rpgitem [ITEM] [EntityType] [chance]`

Set item to be dropped from a specified entity, or with an optional chance.

#### `/rpgitem [ITEM] enchantment` | `/rpgitem [ITEM] enchantment [clone|clear]`

Clone or clear enchantments in hand to item.

E.g., hold a sword with `SHARP II` and execute `/rpgitem test_item enchantment clone` will add `SHARP II` enchant to `text_item`.

#### `/rpgitem [ITEM] hand [text]`

Set hand text for item. Hand text is displayed at left under item name.

#### `/rpgitem [ITEM] type [text]`

Set type text for item. Type text is displayed at right under item name.

#### `/rpgitem [ITEM] item` | `/rpgitem [ITEM] item [options|value]`

Set `ITEM` material to `item` or with additional options.

Available options:

* `[item id]` - Set to an item as material.
* `[item id] hex [string]` - Set to item material with specified color.
* `[item id] [damage value]` - Set to item material with specified damage value.

#### `/rpgitem [ITEM] [additemflag|removeitemflag] [flag]`

Add or remove item flags.

#### `/rpgitem [ITEM] permission [permission node] [enabled|boolean]`

Set item permission node. If `enabled` is `true`, only players with corresponding permission node can use this item.

#### `/rpgitem [ITEM] quality` | `/rpgitem [ITEM] quality [value]`

Set item quality. Currently no actual usage in plugin.

Possible values:

* `trash`
* `common`
* `uncommon`
* `rare`
* `epic`
* `legendary`

#### `/rpgitem [ITEM] recipe [chance|int]`

Set the item has a chance of `1/[chance]` to be crafted via craft table.

#### `/rpgitem [ITEM] remove`

Remove the item from plugin.

#### `/rpgitem [ITEM] removepower [power]`

Remove the power from item. If the item have multiple specified power, the first match (pit fall) will be removed.

#### `/rpgitem [ITEM] toggleArmorLore`

Toggle item armor information and hand/type text to be shown/hidden.

#### `/rpgitem [ITEM] togglePowerLore`

Toggle item power description to be shown/hidden. Hide power lore can make item description looks cleaner.

#### `/rpgitem [ITEM] worldguard`

Set item to work with worldguard.
