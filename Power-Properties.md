Getter and Setter is the tool to view/modify power properties.

Each power has its own configurable properties. For details, please refer to [en:Powers](/NyaaCat/RPGitems-reloaded/wiki/en:Powers) page.

## Basic usage

```
/rpgitem [item] get [power] [index] [properties]
```

```
/rpgitem [item] set [power] [index] [properties] [value]
```

E.g, check `test_item` first `potionhit` power's duration property:
```
/rpgitem test_item get potionhit 1 duration
```

And set the second `aoecommand` power `command` property, to spawn a ignited creeper at each entity location:

```
/rpgitem test_item set aoecommand 2 command summon creeper {entity.x} {entity.y} {entity.y} {ignited:1,Fuse:5}
```

Note: you may need command block or console access if the command is too long.
