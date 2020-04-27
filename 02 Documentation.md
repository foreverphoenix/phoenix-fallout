![logo](Media/Logo.png)

**TABLE OF CONTENTS**
- [The Documentation](#the-documentation)
- [Preparations](#preparations)
- [Game Folder Files](#game-folder-files)
- [Essentials](#essentials)
  - [Armor and Weapon Keywords Community Resource](#armor-and-weapon-keywords-community-resource)
  - [Armorsmith Extended](#armorsmith-extended)
- [Item Sorting](#item-sorting)
  - [Valdacil's Item Sorting](#valdacils-item-sorting)
  - [VIS Expanded](#vis-expanded)
  - [Custom DEF_INV_TAGS](#custom-def_inv_tags)

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
- [Armor and Weapons Keywords Community Resource (AWKCR)](https://www.nexusmods.com/fallout4/mods/6091) is a stripped down copy with only the new keywords.
- Also stripped down [Armorsmith Extended](https://www.nexusmods.com/fallout4/mods/2228) to its equipment slot features (see below).
- For [DEF_UI](https://www.nexusmods.com/fallout4/mods/10654), I chose both DEF_HUD and DEF_INV in the FOMOD, as well as 

## Armor and Weapon Keywords Community Resource

[Armor and Weapons Keywords Community Resource (AWKCR)](https://www.nexusmods.com/fallout4/mods/6091) is one of key mod for Fallout 4 but has been suffering from feature creep in recent years. I am using the old version 4.02, forwarded some UFO4P edits, and stripped out the additional workbenches and ammo crafting features. The BSAs were also deleted as they are now redundant.

Literally all the mod does anymore is add proper keywords.

## Armorsmith Extended

Like AWKCR, [Armorsmith Extended](https://www.nexusmods.com/fallout4/mods/2228) has been suffering from bloat over the years. Using the latest version (4.6), I stripped it down to the essentials. What I kept from the original mod:

- Super mutants (eg Strong) can equip most headwear pieces.
- Nick Valentine can wear anything.
- You can wear armor pieces on top of clothing / outfits.
- Different pieces of headware can be combined if they don't overlap (helmet and bandana etc).

![separator](/Media/Separator.png)

# Item Sorting

## Valdacil's Item Sorting

While [Valdacil's Item Sorting](https://www.nexusmods.com/fallout4/mods/3877) has technically been superceeded by [VIS-G Item Sorting](https://www.nexusmods.com/fallout4/mods/33383). However, I am a stubborn person, and much prefer VIS' more simplistic sorting and icons over VIS-G, so that is what I am using.

- **ValdacilsItemSorting-Perks.esp:** Forwarded UFO4P edits.
- **ValdacilsItemSorting-ExplosivesSortTop.esp:** Sort to Top with weight version. Forwarded `_WeaponType_Thrown [KYWD:08000959]` from AWKCR for each record.
- **ValdacilsItemSorting-AidReducedWeight.esp** Chems and Syringer Ammo have weight again, but quest items remain weightless. Set weight for gourds and melons to 0.5. Forwarded UFO4P edits.
- **ValdacilsItemSorting-Misc.esp:** Forwarded UFO4P edits.
- **ValdacilsItemSorting-JunkBetter+DEF_INV.esp** Merged NotJunk changes into BetterJunkDEF_INV. Renamed all empty bottles to "Empty {Bottle Type}". Forwarded UFO4P edits.
- **ValdacilsItemSorting-Mods.esp:** Vanilla weight version. Records are untouched.
- **ValdacilsItemSorting-Ammo.esp:** Vanilla weight version. Added DLC support.

## VIS Expanded

This plugin adds missing keywords to some pieces of armor / clothing, and manually tags all items that the game didn't recognise for some reason (even though they have the correct keywords).

## Custom DEF_INV_TAGS

- Set `hidetag` for armor / power armor pieces and weapons to 'true'.
- Added several new tags for faction armor that had no icon associated with them:
  - (Minutemen)
  - (BOS) Brotherhood of Steel
  - (COA) Child of Atom
  - (DC) Diamond City