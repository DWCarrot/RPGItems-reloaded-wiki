## Update From v3.5

0. Stop the server
1. Download RPGItems 3.6 and its dependencies: NyaaCore, Vault, LangUtils, put them to your plugins directory, and remove old version of them. Leave RPGItems directory on here.
2. Do other upgrades and update your Spigot to latest 1.13.2
3. Start the server
4. Monitor the console and see your upgrade progress  
5. ???  
6. Profit!

The upgrade is automatic and should change any behavior of items (except those with PowerCommand -- if vanilla minecraft break the command they are using). If you come across any stacktrace or misbehavior of items, feel free to open an issue here. Server ops will be notified when any item upgrade fails when they login.

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

## Known Issue

Power Color is not implemented now.
