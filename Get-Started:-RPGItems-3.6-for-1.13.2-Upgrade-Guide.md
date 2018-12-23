# Update From v3.5

1. Stop the server
2. Download RPGItems 3.6 and its dependencies: NyaaCore, Vault, LangUtils, put them to your plugins directory, and remove old version of them. Leave RPGItems directory on here.
3. Do other upgrades and update your Spigot to latest 1.13.2
4. Start the server
5. Monitor the console and see your upgrade progress
6. ???
7. Profit!

Items will be automatically updated on first start of 1.13 version. `items.yml` will be renamed to `items.bak` and each item saved into `items/` separately.

The upgrade is automatic and should change any behavior of items (except those with PowerCommand -- if vanilla minecraft break the command they are using). If you come across any stacktrace or misbehavior of items, feel free to open an issue here. Server ops will be notified when any item upgrade fails when they login.

## Item auto update from 1.12 to 1.13

If you need to update command/throw related powers (command format, nbt, item/entity names, etc.), follow these procedure:

1. Install Nodejs (tested working v10.13.0 LTS).
2. Run `git clone https://github.com/Librazy/spu.git && cd spu && git checkout work && npm i && npm run restful`.
3. Edit `RPGItems/config.yml`, add `spu_endpoint: http://127.0.0.1:8080` under general section. Change the endpoint URL when necessary.
4. `/rpgitem reload` and then `/rpgitem updatecmdandentity all` (replace `all` with item name if you want to update single item)
Nearly all vanilla commands will be updated to 1.13 format. Other commands can't be recognized will keep unchanged.

These update is provided by [SPU](https://github.com/CommandBlockLogic/spu), very appreciated for their effort.

## New Features

* Trigger system
* Condition system
* Extension system
* New command interface
* Smart tab completion
* Separated item config
* New powers
* New properties for existing powers

## Changes From v3.5

TBD

## Things removed since v3.5

* Item quality is removed. Color of display name is preserved. The item quality has no impact to gameplay in 3.5.
* Item lore is migrated to item description. It will become beginning lines of lore and will be auto wrapped.
* Known Issue
* Power Color is not implemented now.