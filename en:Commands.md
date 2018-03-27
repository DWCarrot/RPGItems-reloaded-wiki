This is general commands to use the plugin, or customize an item.

## Plugin Commands

#### `/rpgitem list [page|optional]`

List all items, with item identical name (in plugin) and item details (item itself). Like this:

```
RPGItems: 1/41
hidden_blade - Ezio's hidden blade
...
```

With mouse hover onto item name (the later name `Ezio's hidden blade`), an item tooltip will show details of this item.

`/rpgitem list` simply list all items, `/rpgitem list 3` will list items in page 3.

#### `/rpgitem help [keyword]`

Search help messages for `keyword`. It can be a power or any description in message file.

E.g., `/rpgitem help left` will display all information related with `left`, possibly all the powers that supports to use with left click.

#### `/rpgitem version`

Check version string.

#### `/rpgitem reload`

Reload all the config.

## Item Commands

#### `/rpgitem [ITEM] create`

Creates the `[ITEM]`.

#### `/rpgitem [ITEM]`

Preview the item.

#### `/rpgitem [ITEM] give` | `/rpgitem [ITEM] give [player] [amount]`

Give you the item or give specified player an amount of such items.

#### `/rpgitem [ITEM] armour` | `/rpgitem [ITEM] armour [armour value|int[0-100]]`

Show/set item armour value. The armour reduce a percent of damage taken.

#### `/rpgitem [ITEM] clone [ITEM2]`

Clone `ITEM` as `ITEM2`, use to quickly create a bunch of similar items or a series items.

#### `/rpgitem [ITEM] cost [options]`

Set item cost values. See [New Durability System](/NyaaCat/RPGitems-reloaded/wiki/New-durability-system).

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

#### `/rpgitem [ITEM] quality` | `/rpgitem [ITEM] quality [value]`

#### `/rpgitem [ITEM] recipe [chance|int]`

#### `/rpgitem [ITEM] remove`

#### `/rpgitem [ITEM] removepower [power]`

#### `/rpgitem [ITEM] toggleArmorLore`

#### `/rpgitem [ITEM] togglePowerLore`

#### `/rpgitem [ITEM] worldguard`