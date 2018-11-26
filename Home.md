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

## Updated to Lore based item identification

Related commit [7604687](https://github.com/NyaaCat/RPGitems-reloaded/commit/7604687e69f43527ba1c043552818aa14ecd61b8)  
Related issue [#24](https://github.com/NyaaCat/RPGitems-reloaded/issues/24)

#### New Command /rpgitemupdate
All existed rpgitems will become invalid.  
Taking the item you want to update in hand then type the command.  
A notification about whether the process success or fail will appear.  
Player need permission node `rpgitemupdate.command` to execute this.

There are three sub-command which only OPs can execute, they are for debug purpose only.

- /rpgitemupdate inspect
- /rpgitemupdate upgrade
- /rpgitemupdate downgrade

#### Possible Issues

- Data are stored in lore. Players with permissions can still modify them.

#### 新命令 /rpgitemupdate
所有存在的RPGItem将会失效  
将失效的物品拿在手中，并执行`/rpgitemupdate`命令，即可更新物品  
会有提示显示更新是否成功  
需要有权限`rpgitemupdate.command`才可执行命令

有三个只有OP可以执行的子命令用于调试：

- /rpgitemupdate inspect
- /rpgitemupdate upgrade
- /rpgitemupdate downgrade

#### 可能的问题

- 信息存储在Lore中。有权限的玩家依然可以修改。

