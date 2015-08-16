### Installation

* Download the latest release from [here](https://github.com/NyaaCat/RPGitems-reloaded/releases)
* Drop the jar into `plugins` folder
* Restart the server

### Get started

#### EXAMPLE: Ice spell card

We are now going to create a spell card, on player use it shoots ice and then consumes itself.

Commands:

1. `/rpgitem icecard create`
2. `/rpgitem icecard item paper`
3. `/rpgitem icecard display &bICE &dSPELL CARD`
4. `/rpgitem icecard type &bICE`
5. `/rpgitem icecard hand &dSpell Card`
6. `/rpgitem icecard description add &fFreeze them all!`
7. `/rpgitem icecard power ice 20`
8. `/rpgitem icecard power consume`

That's it. Now use `/rpgitem icecard give` to get one and test its power.

Explaination:

1. Create the RPGitem and save into config file.
2. Change the item texture to paper (show as paper)
3. Change the item name to `&bICE &dSPELL CARD`
4. Change the item first line left to `&bICE`
5. Change the item first line right to `&dSpell Card`
6. Add a line of description `&fFreeze them all!`
7. Give the item power `ice`, with cooldown 20 ticks (1 sec)
8. Give the item power `consume`, so that it consumes itself after use.

For more information, consult [commands](https://github.com/NyaaCat/RPGitems-reloaded/wiki/Commands), [powers](https://github.com/NyaaCat/RPGitems-reloaded/wiki/Powers) and [potions](https://github.com/NyaaCat/RPGitems-reloaded/wiki/Potion-Effects) page