# Valheim Trainer

A trainer for Valheim with a menu you open inside the game. You run `ValheimTrainer.exe` and it gets the trainer into Valheim for you. Nothing else needed: no BepInEx, no Jötunn, no devcommands.

I wrote it for a dedicated server I share with two friends. We play PvE, so I gave myself one rule: whatever the trainer does, it does to my own character, and everyone else is left alone. That rule shaped most of it, and where it doesn't hold, the [On a server](#on-a-server) section says so.

It started out as a Cheat Engine table. Same cheats, quite a few more on top, and no second window to keep alive while you play.

## Download

Grab the zip from [Releases](../../releases/latest). What changed in each version is in [CHANGELOG.md](CHANGELOG.md).

This repository holds the releases and the issue tracker. The source code isn't published.

## Install

Unzip it anywhere. The two files that matter have to stay in the same folder:

- `ValheimTrainer.exe`
- `ValheimTrainer.dll`

Run `ValheimTrainer.exe` whenever you like, before or after Valheim. It'll wait for the game to show up, load the trainer, and tell you when it's in. From there, **Insert** or **F1** opens the menu.

One thing that catches people: if Valheim is running as administrator, the exe has to as well.

Done playing? **Unload trainer** at the bottom of the menu takes it back out. And if you ever need everything off right now, **End** is the panic key: every feature off, every window closed.

## The menu

Six tabs: Player, Combat, Inventory, World, Build, Travel. Every feature is a checkbox, and the ones with knobs to turn have a **+** next to them. The buttons along the bottom of each tab are one-off actions rather than toggles. There's a search box above the tabs, which is honestly the fastest way to find anything once the list got this long.

You can drag the window wherever you want it, and **Settings...** handles the cosmetic side: text size, dark or light, and how see-through the windows are. Every hotkey can be rebound. Your settings live in `ValheimTrainer.cfg` next to the game's saves, in `%USERPROFILE%\AppData\LocalLow\IronGate\Valheim`. Which features you had switched on isn't saved, and that's deliberate: every session starts clean with everything off.

After a Valheim update, hit **Check compatibility** before anything else. It goes looking for everything the trainer needs from the game, turns none of it on, and tells you what broke. And if something does break while it's running, the trainer quietly switches that one feature off rather than taking the rest down with it.

## What's in it

**Player.** Reverse Damage is the one I actually use. You take less, the attacker gets some of it back, you heal over time, and your health won't drop past a floor you set. Next to it sit god mode, ghost mode, no debuffs, and keeping everything on death. Then the numbers: higher base health and stamina, three stamina modes depending on how far you want to take it, infinite eitr, food that never runs down, always rested, Forsaken power with no cooldown. Movement speed, a higher jump without the fall damage that normally comes with it, flight, no weight limit, armor that doesn't slow you down, a longer auto-pickup reach, faster skill gain. There's also a party aura that heals and buffs the players around you, and Share my features for friends who run the trainer too.

**Combat.** More damage against creatures. Chopping and mining sped up, or down to a single hit when you've got a forest in the way. Infinite ammo, and an aimbot for bows. More loot, with an option to make the trophy always drop. ESP for enemies, friends, ore, treasure, pickables, dropped items and dungeons. Switch off the ones you don't need, your framerate will thank you.

**Inventory.** This tab started as pure laziness. Infinite durability, bigger stacks, extra rows, teleport with anything, food and potions that don't get consumed, crafting and building straight out of nearby chests, and a filter so auto-pickup stops hoovering up junk you'll never use. The buttons do the boring part: add items, clean out the inventory, repair everything, stack into nearby chests, sort the backpack, or edit an item directly.

**World.** Lock the time of day, lock the weather, clear the fog. Yes, that includes the Mistlands mist. Faster production, plants that grow instantly and yield more, no fuel needed, instant taming. A HUD with coordinates, biome, day, time and FPS, plus a free camera, camera zoom and a bigger map reveal radius. The buttons reveal bosses and traders, tame the animals around you, spawn creatures, or explore the whole map. Game speed lives here too, read [the note about it](#on-a-server) before you touch it.

**Build.** Free building and crafting, longer reach, bigger terrain leveling, infinite support, no rain damage, and planting wherever you like. One button repairs every structure around you, and terraform (raise, lower, level, smooth) comes with an undo, which you will end up needing.

**Travel.** Tailwind and a faster boat, because sailing in this game is lovely for about the first twenty hours. Teleports to the last pin, any pin, the map cursor, your bed, wherever you died, another player, or a position you saved earlier.

## On a server

Your friends don't need the trainer, and they won't notice most of it.

- Combat features never touch players or tamed animals. The damage boost, kill nearby, the aimbot, enemy ESP, the reflected damage, none of them.
- Reverse Damage ignores hits that came from another player, so it won't make you a wall in PvP.
- The only things the trainer sends another player's way are the good ones: the heal button and the party aura. Both ride on what the game already lets players do to each other. The aura skips anyone with PvP on, the heal button heals everyone in range.
- Share my features only reaches friends who run the trainer too. Anyone can turn it down with **Accept features shared by others**, and nothing is applied to a player with PvP on.
- Beyond that, nothing can reach someone who isn't running the trainer. Damage, stamina and inventory are all worked out on each player's own PC.
- It won't start raids or events, won't touch the server's global keys, and won't delete structures.
- Crafting from chests leaves other people's private chests alone, along with chests behind a ward you don't have access to, chests somebody currently has open, and tombstones.

Now the awkward part, because a few things can't really be "mine only":

- God mode and ghost mode are the game's own switches, not mine. They don't care who's swinging at you, so turn them off before any PvP.
- The world features (production, fuel, plants, fire, structural support, rain damage, taming) only apply in zones your client owns, which usually means whoever got there first. Standing in a friend's zone, they do nothing at all.
- Game speed is client side. Day and night still follow the server's clock, but creatures in zones you own move at your speed, and friends standing nearby will see that.
- Spawned creatures, terraforming, and anything you pull out of a shared chest change the world for everybody. Terraforming doesn't stop at wards either. Talk to your group first.
- Killing things in god or ghost mode marks the loot as cheated. In practice that only matters for Steam achievements and stats, but if those matter to you, bear in mind that cheating on a character is something Valheim keeps a note of.

Three buttons write to your character permanently and there's no taking them back: **Raise skills**, **Unlock everything** and **Explore the whole map**. The last two ask you first.

**Bigger stacks** and **More inventory rows** want the trainer loaded before you enter the world. Stacks go back to their normal size when you leave or switch it off. Whatever sits in the extra rows is kept as long as the trainer was loaded first. If you stop using it, or you're going to load it after entering the world, empty those rows first, or the game drops what's in them.

## If something goes wrong

- **It doesn't load.** `ValheimTrainer.exe` will tell you why, and `ValheimTrainer.log` next to it has the full story.
- **The message appeared but Insert does nothing.** Try F1. A lot of laptops don't have an Insert key at all.
- **CPU or temperatures through the roof.** Check Game speed first. Anything above x1 means the game is simulating more per second, and that costs CPU no matter what else you have on. A wide ESP range with pickables and dropped items will eat frames too. The End key switches everything off at once, which makes it easy to compare.
- **One feature isn't working.** Press **Check compatibility** and read what it lists. Trainer lines in `Player.log`, in the same folder as the settings, start with `[ValheimTrainer]`.
- **Antivirus is unhappy.** Fair enough, loading code into another program is exactly what malware does, so some scanners flag the exe. If you'd rather not add an exception, you can inject `ValheimTrainer.dll` into `valheim.exe` with any LoadLibrary injector instead.

If none of that helps, [open an issue](../../issues) and attach `ValheimTrainer.log` along with what Check compatibility says.

## Credits

Patching is done with [Harmony](https://github.com/pardeike/Harmony) by Andreas Pardeike (MIT). Released under the MIT license, see [LICENSE](LICENSE).

Not affiliated with Iron Gate or Coffee Stain in any way. Use it on servers where everyone's fine with it.
