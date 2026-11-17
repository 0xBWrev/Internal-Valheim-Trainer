Valheim Trainer

This is my trainer for Valheim, with a menu you open inside the game. You copy one file into the Valheim folder and the game loads the trainer by itself. You don't need BepInEx, Jötunn or devcommands.

I made it for a dedicated server I play on with two friends. We play PvE, so I set one rule: the trainer only changes my own character and leaves everyone else alone. Where it can't keep that rule, I explain it in On a server.

It started as a Cheat Engine table. It has the same cheats and a lot more, and I don't need a second window open while I play.

Download

Get the zip from Releases. The changes for each version are in CHANGELOG.md.

The source code is here too. If you'd rather build it yourself, it's explained in Building.

Install

Copy version.dll into the Valheim folder, next to valheim.exe. To find the folder in Steam, right-click Valheim and go to Manage > Browse local files.

Start Valheim as usual. The trainer loads with the game, and Insert or F1 opens the menu.

If you need everything off right away, press End. It turns every feature off and closes every window. Unload trainer, at the bottom of the menu, takes the trainer out until you start the game again.

To uninstall it, delete version.dll from the Valheim folder.

The menu

There are six tabs: Player, Combat, Inventory, World, Build and Travel. Every feature is a checkbox, and the ones with settings have a + next to them. The buttons at the bottom of each tab do something once. The search box above the tabs is the fastest way to find something now that the list is this long.

You can move the window anywhere. In Settings... you can change the text size, pick a dark or light theme, set how transparent the windows are and change every hotkey. Your settings are saved in ValheimTrainer.cfg, next to the game's saves in %USERPROFILE%\AppData\LocalLow\IronGate\Valheim. The features you had on are not saved. I did that on purpose, so every session starts with everything off.

After a Valheim update, press Check compatibility first. It checks everything the trainer needs from the game without turning anything on, and tells you what broke. If a feature breaks while it's on, the trainer turns that one off and the rest keeps working.

What's in it

Player. Reverse Damage is the one I use the most. You take less damage, the attacker gets part of it back, you heal over time, and your health never goes below the minimum you set. There's also god mode, ghost mode, no debuffs and keeping everything when you die. Then the stats: higher base health and stamina, three stamina modes, infinite eitr, food that doesn't run out, always rested and no cooldown on the Forsaken power. For moving around there's movement speed, a higher jump without fall damage, flying, no weight limit, armor without the speed penalty, a longer auto-pickup range and faster skill gain. And there's a party aura that heals and buffs the players near you, plus Share my features for friends who also run the trainer.

Combat. More damage to creatures. Faster chopping and mining, or one hit if you just want the forest gone. Infinite ammo and a bow aimbot. More loot, with an option to always drop the trophy. ESP for enemies, friends, ore, treasure, pickables, dropped items and dungeons. I turn off the ones I don't need, because each one costs frames.

Inventory. I made this tab because I was lazy. Infinite durability, bigger stacks, extra rows, teleport with any item, food and potions that don't get used up, crafting and building from nearby chests, and a filter so auto-pickup leaves the junk on the ground. The buttons add items, clean the inventory, repair everything, stack into nearby chests, sort the backpack and edit an item.

World. Fixed time of day, fixed weather and no fog, Mistlands mist included. Faster production, plants that grow instantly and give more, no fuel needed and instant taming. A HUD with coordinates, biome, day, time and FPS, a free camera, more camera zoom and a bigger map reveal radius. The buttons reveal bosses and traders, tame the animals around you, spawn creatures or explore the whole map. Game speed is here too. Read what I say about it in On a server before you use it.

Build. Free building and crafting, longer reach, bigger terrain leveling, infinite support, no rain damage and planting anywhere. One button repairs every structure around you, and terraform (raise, lower, level, smooth) has an undo. You'll probably need it.

Travel. Tailwind and a faster boat, because sailing gets slow after a while. Teleport to the last pin, any pin, the map cursor, your bed, where you died, another player, or a position you saved.

On a server

My friends don't need the trainer, and most of it never touches them.

Combat features never affect players or tamed animals. That includes the extra damage, kill nearby, the aimbot, enemy ESP and the damage Reverse Damage sends back.
Reverse Damage ignores hits from other players, so it doesn't help you in PvP.
The only things the trainer does to other players are the heal button and the party aura. Both use what the game already lets players do to each other. The aura skips anyone with PvP on, but the heal button heals everyone in range.
Share my features only reaches friends who also run the trainer. They can refuse it by unticking Accept features shared by others, and nothing is applied to a player with PvP on.
Apart from that, nothing reaches a player who doesn't run the trainer. Damage, stamina and inventory are worked out on each player's own PC.
It doesn't start raids or events, doesn't touch the server's global keys and doesn't delete structures.
Crafting from chests skips other players' private chests, chests in a ward you can't open, chests someone has open, and tombstones.

Some things can't be only mine, and you should know about them:

God mode and ghost mode are the game's own switches. They protect you from everyone, players too, so I turn them off before any PvP.
World features (production, fuel, plants, fire, support, rain damage, taming) only work in zones your game owns, which is usually whoever got there first. In a friend's zone they do nothing.
Game speed only runs on your side. Day and night follow the server's clock, but creatures in your zones move at your speed, and friends nearby will see it.
Spawned creatures, terraforming and anything you take from shared chests change the world for everyone. Terraforming also ignores wards. Ask your group first.
If you kill things in god or ghost mode, the loot is marked as cheated. That only matters for Steam achievements and stats, but Valheim does remember that the character cheated.

Three buttons change your character for good: Raise skills, Unlock everything and Explore the whole map. The last two ask first.

Bigger stacks and More inventory rows only work while the trainer is loaded. Stacks go back to normal when you leave or turn the feature off. Before you unload the trainer or delete version.dll, empty the extra rows, or the game drops what's in them the next time it loads your character.

If something goes wrong
It doesn't load. Check that version.dll is right next to valheim.exe, not in a subfolder. If it loads but something fails, a message tells you why, and ValheimTrainer.log next to version.dll has the details.
The trainer says it's loaded but Insert does nothing. Try F1. A lot of laptops don't have an Insert key.
High CPU or temperatures. Check Game speed first. Above x1 the game simulates more every second, and that costs CPU whatever else is on. A big ESP range with pickables and dropped items also costs frames. End turns everything off, so you can compare.
A feature doesn't work. Press Check compatibility and read the list. Trainer lines in Player.log, in the same folder as the settings, start with [ValheimTrainer].
It doesn't load on Linux or Steam Deck. Add WINEDLLOVERRIDES="version=n,b" %command% to Valheim's launch options in Steam, so Proton uses the version.dll in the game folder.
Your antivirus complains. A DLL that a game loads from its own folder is also a trick malware uses, so some antivirus programs can flag it. All the code is here, so you can check it or build it yourself.

If none of that helps, open an issue and attach ValheimTrainer.log.
