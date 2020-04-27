![logo](Media/Logo.png)

**TABLE OF CONTENTS**
- [The Documentation](#the-documentation)
- [Preparations](#preparations)
- [Game Folder Files](#game-folder-files)
- [Essentials](#essentials)
- [Item Sorting](#item-sorting)
  - [Valdacil's Item Sorting](#valdacils-item-sorting)
  - [Phoenix - Weapon Sorting](#phoenix---weapon-sorting)
  - [Custom DEF_INV Files](#custom-def_inv-files)

![separator](/Media/Separator.png)

# The Documentation

This page serves two purposes: One, to inform the user about the contents of this Wabbajack list, and two, remind me what I did to which files. You don't have to read it but it will help you understand how Phoenix: Fallout changes the game and what my thoughts behind each mod addition were.

**This page does not include any instructions whatsoever.** There is nothing you have to do yourself. It's just information on the Wabbajack list and my personal notes.

![separator](/Media/Separator.png)

# Preparations

- Set up [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) (2.2.2.1).
- Improved INI files with [BethINI](https://www.nexusmods.com/fallout4/mods/67) 3.3 (not using Custom INIs).
- Sorted DLC in the mod order to match the load order.

![separator](/Media/Separator.png)

# Game Folder Files

Not all mods can be installed into the **Data** folder or be handled by Mod Organizer 2. The following mods need their files inside the **root** folder:

- The [Fallout 4 Script Extender (F4SE)](http://f4se.silverlock.org/) executable and DLLs have to be inside the root folder:
  - `f4se_1_10_163.dll`
  - `f4se_loader.exe`
  - `f4se_steam_loader.dll`
- [Dynamic Performance Tuner and Load Accelerator](https://www.nexusmods.com/fallout4/mods/28143/) caps the frame rate at 60FPS, dynamically adjusts shadow distance, and speeds up load times. Only its core files need to be in the root folder:
  - `dxgi.dll`
  - `dynaperf.ini`
- The [Configuration Files for Dynamic Performance Tuner and Load Accelerator](https://www.nexusmods.com/fallout4/mods/33632) are required for the previous mod to work properly with the current version of Fallout 4. The INI file belongs in the root folder:
  - `fallout4-addresses-1.10.163.0.ini`
- The [xSE Plugin Preloader F4](https://www.nexusmods.com/fallout4/mods/33946) is required for Private Profile Redirector. Its DLL and INI file must be inside the root folder:
  - `IpHlpAPI.dll`
  - `xSE PluginPreloader.ini`

![Game Folder Files](Media/documentation/game_folder_files.png)

![separator](/Media/Separator.png)

# Essentials

- The [F4SE](http://f4se.silverlock.org/) scripts are packaged separately and installed in MO2.
- The base for all modded Bethesda games is as always the [Unofficial Fallout 4 Patch](https://www.nexusmods.com/fallout4/mods/4598).
- [Private Profile Redirector](https://www.nexusmods.com/fallout4/mods/33947) speeds up the game launch. It requires F4SE and the xSE Plugin Preloader.
- [Achievements](https://www.nexusmods.com/fallout4/mods/12465) allows for Steam achievements to be earned in a modded playthrough.
- [PhyOp - Overhauled Optimized Textures](https://www.nexusmods.com/fallout4/mods/27038) improves the vanilla textures, reducing their file size and using a different compression. The included files are listed below, they were merged together into one mod folder, the updated BSAs overwriting the original ones to reduce the overall file size.
  -  PhyOp (Light) Base Game 1.2a
  -  PhyOp (Light) DLC 1.2a
  -  PhyOp (Light) Base Game 1.2a (2k Brahmin Pack Textures)
  -  PhyOp (Light) Base Game 1.2a Face Sculpting Fix
- For [DEF_UI](https://www.nexusmods.com/fallout4/mods/10654), I chose both DEF_HUD and DEF_INV in the FOMOD.

![separator](/Media/Separator.png)

# Item Sorting

## Valdacil's Item Sorting

While [Valdacil's Item Sorting](https://www.nexusmods.com/fallout4/mods/3877) has technically been superceeded by [VIS-G Item Sorting](https://www.nexusmods.com/fallout4/mods/33383). However, I am a stubborn person, and much prefer VIS' more simplistic sorting and icons over VIS-G, so that is what I am using.

- **ValdacilsItemSorting-ZZ-DLCArmorBySlotOverride.esp:** Tweaked Power Armor naming rules (see below).
- **ValdacilsItemSorting-ZZ-DLCWeaponsOverride.esp:** Removed the Instance Naming Rules. Edited the leveled list name overrides to match my sorting tags. Removed AWKCR as a master.
- **ValdacilsItemSorting-ExplosivesSortBottom.esp:** Sort to Top with weight version. Changed {Explosive} to |Explosive|. Added new tag |Trap| for the Far Harbor traps (which are classified as explosives).
- **ValdacilsItemSorting-AidReducedWeight.esp** Chems and Syringer Ammo have weight again, but quest items remain weightless. Set weight for gourds and melons to 0.5. Forwarded UFO4P edits.
- **ValdacilsItemSorting-Misc.esp:** Forwarded UFO4P edits.
- **ValdacilsItemSorting-JunkBetter+DEF_INV.esp** Merged NotJunk changes into BetterJunkDEF_INV. Renamed all empty bottles to "Empty {Bottle Type}". Forwarded UFO4P edits.
- **ValdacilsItemSorting-Mods.esp:** Vanilla weight version. Records are untouched.
- **ValdacilsItemSorting-Ammo.esp:** Vanilla weight version. Added DLC support.
- **ValdacilsItemSorting-Perks.esp:** Forwarded UFO4P edits.

In the ArmorBySlot override, I discovered that while there are several INNR lists for power armor, they are identical. I pointed all power armor sets at the primary **dn_PowerArmor** list and disregarded the other ones. I also replicated keywords that AWKCR added for four paint jobs that were missing in the original game, renamed "Raider Power > Raider" and "Overboss Power > Power" as well as added the piece to the name "X-01 Mk. 1 > X-01 Left Arm Mk. 1".

## Phoenix - Weapon Sorting

Weapons are tagged with matching icons and sorted as follows:

- (Firearms)
- [Heavy Weapons]
- {Melee Weapons}

|Explosives| are no longer in their own sub-section but they will sort to bottom, below all other weapons.

## Custom DEF_INV Files

### DEF_INV_TAGS

- Set `hidetag` for armor / power armor pieces and weapons to 'true'.
- Added several new tags for faction armor that had no icon associated with them:
  - (Minutemen)
  - (BOS) Brotherhood of Steel
  - (COA) Child of Atom
  - (DC) Diamond City

### DEF_INV_TABS / lyrConf.xml

- Removed the Explosives section. All explosives now sort to the bottom of the Weapons tab.