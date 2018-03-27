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

#### `/rpgitem [ITEM] give`

Give you the item.

Use `/rpgitem [ITEM] give [player] [amount]` to give specified player an amount of such items.

#### `/rpgitem [ITEM] armour` | `/rpgitem [ITEM] armour [armour value|int[0-100]]`

#### `/rpgitem [ITEM] clone [ITEM2]`

#### `/rpgitem [ITEM] cost [options]`

options: breaking|breaking [value]|hit|hit [value]|hit toggle|hitting [value]

#### `/rpgitem [ITEM] customItemModel`

#### `/rpgitem [ITEM] damage` | `/rpgitem [ITEM] damage [option]`

#### `/rpgitem [ITEM] damageMode`

value: fixed|vanilla|additional

#### `/rpgitem [ITEM] durability [value|options]`

value: int
options: infinite|togglebar

#### `/rpgitem [ITEM] durabilitybound [minimum] [maximum]`

#### `/rpgitem [ITEM] durabilityinfo`

#### `/rpgitem [ITEM] description add [text]`

#### `/rpgitem [ITEM] description set [line|int[0~]] [text]`

#### `/rpgitem [ITEM] description remove [line|int[0~]]`

#### `/rpgitem [ITEM] display` | `/rpgitem [ITEM] [value]`

#### `/rpgitem [ITEM] drop [EntityType]` | `/rpgitem [ITEM] [EntityType] [chance]`

#### `/rpgitem [ITEM] enchantment` | `/rpgitem [ITEM] enchantment [clone|clear]`

#### `/rpgitem [ITEM] hand [text]`

#### `/rpgitem [ITEM] type [text]`

#### `/rpgitem [ITEM] item` | `/rpgitem [ITEM] item [options|value]`

value: item id
options: item id hex string | item id damagevalue | item id

#### `/rpgitem [ITEM] [additemflag|removeitemflag] [flag]`

#### `/rpgitem [ITEM] permission [permission node] [enabled|boolean]`

#### `/rpgitem [ITEM] quality` | `/rpgitem [ITEM] quality [value]`

#### `/rpgitem [ITEM] recipe [chance|int]`

#### `/rpgitem [ITEM] remove`

#### `/rpgitem [ITEM] removepower [power]`

#### `/rpgitem [ITEM] toggleArmorLore`

#### `/rpgitem [ITEM] togglePowerLore`

#### `/rpgitem [ITEM] worldguard`