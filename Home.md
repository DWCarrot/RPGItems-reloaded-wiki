Welcome to RPGItems Wiki.

Current stable version - 3.5 for 1.11/1.12

Version 3.6 for 1.13 is on its way but still considered as unstable. Starting from this version you need NyaaCore, LangUtils and Vault to work.

***

## Item auto update from 1.12 to 1.13

Items will be automatically updated on first start of 1.13 version. `items.yml` will be renamed to `items.bak` and each item saved into `items/` separately.

If you need to update command/throw related powers (command format, nbt, item/entity names, etc.), follow these procedure:

1. Install Nodejs (tested working v10.13.0 LTS).
2. Run `git clone https://github.com/Librazy/spu.git && cd spu && git checkout work && npm i && npm run restful`.
3. Edit `RPGItems/config.yml`, add `spu_endpoint: http://127.0.0.1:8080` under `general` section. Change the endpoint URL when necessary.
4. `/rpgitem reload` and then `/rpgitem updatecmdandentity all`

Nearly all vanilla commands will be updated to 1.13 format. Other commands can't be recognized by spu will keep unchanged.

