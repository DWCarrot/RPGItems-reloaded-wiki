Related commit e4b687dc718ada75375d35c24ddd37918effea99  
Related issue #24

# 新命令 /rpgitemupdate
所有存在的RPGItem将会失效  
将失效的物品拿在手中，并执行`/rpgitemupdate`命令，即可更新物品  
会有提示显示更新是否成功  
需要有权限`rpgitemupdate.command`才可执行命令

有三个只有OP可以执行的子命令用于调试：


- /rpgitemupdate inspect
- /rpgitemupdate upgrade
- /rpgitemupdate downgrade

# 可能的问题

- 一些插件可能错误地处理Metadata导致NBT损坏
- 仍有信息存储在Lore中。有权限的玩家依然可以修改。

# New Command /rpgitemupdate
All existed rpgitems will become invalid.  
Taking the item you want to update in hand then type the command.  
A notification about whether the process success or fail will appear.  
Player need permission node `rpgitemupdate.command` to execute this.

There are three sub-command which only OPs can execute, they are for debug purpose only.

- /rpgitemupdate inspect
- /rpgitemupdate upgrade
- /rpgitemupdate downgrade

# Possible Issus

- Some plugins may handle metadata incorrectly thus break the NBT tag
- There are still data stored in lore. Players with permissions can still modify them.