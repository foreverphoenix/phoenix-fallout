![logo](Media/Logo.png)

**TABLE OF CONTENTS**
- [The Documentation](#the-documentation)
  - [Preface](#preface)
  - [Features](#features)
  - [Preparations](#preparations)
  - [Game Folder Files](#game-folder-files)
- [Essentials](#essentials)
- [Frameworks](#frameworks)
- [Item Sorting](#item-sorting)
  - [Valdacil's Item Sorting](#valdacils-item-sorting)
  - [Custom DEF_INV Files](#custom-def_inv-files)
- [Fixes](#fixes)
- [Tweaks](#tweaks)
- [Interface](#interface)
- [Weathers](#weathers)
- [Lighting](#lighting)
- [LUT](#lut)
- [Landscape](#landscape)
- [Vehicles](#vehicles)
- [Architecture](#architecture)
- [Creatures](#creatures)
- [Body & Skin](#body--skin)
- [Overhauls](#overhauls)
- [Voice & Sound](#voice--sound)

![separator](/Media/Separator.png)

# The Documentation

## Preface

This page serves two purposes: One, to inform the user about the contents of this Wabbajack list, and two, remind me what I did to which files. You don't have to read it but it will help you understand how Phoenix: Fallout changes the game and what my thoughts behind each mod addition were.

**This page does not include any instructions whatsoever.** There is nothing you have to do yourself. It's just information on the Wabbajack list and my personal notes.

## Features

- Adventure with Dogmeat and another companion.
- Customisation:
  - LUTs
  - DEF_HUD presets?

## Preparations

- Set up [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194) (2.2.2.1).
- Improved INI files with [BethINI](https://www.nexusmods.com/fallout4/mods/67) 3.3 (not using Custom INIs).
- Sorted DLC in the mod order to match the load order.

## Game Folder Files

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

- [PhyOp - Overhauled Optimized Textures](https://www.nexusmods.com/fallout4/mods/27038) improves the vanilla textures, reducing their file size and using a different compression. The included files are listed below, they were merged together into one mod folder, the updated BSAs overwriting the original ones to reduce the overall file size.
  -  PhyOp (Light) Base Game 1.2a
  -  PhyOp (Light) DLC 1.2a
  -  PhyOp (Light) Base Game 1.2a (2k Brahmin Pack Textures)
  -  PhyOp (Light) Base Game 1.2a Face Sculpting Fix
- The [F4SE](http://f4se.silverlock.org/) scripts are packaged separately and installed in MO2.
- The [Unofficial Fallout 4 Patch](https://www.nexusmods.com/fallout4/mods/4598) includes numerous bug and consistency fixes.
- [Private Profile Redirector](https://www.nexusmods.com/fallout4/mods/33947) speeds up the game launch. It requires F4SE and the xSE Plugin Preloader.
- [Achievements](https://www.nexusmods.com/fallout4/mods/12465) allows for Steam achievements to be earned in a modded playthrough.
- [Mod Configuration Menu](https://www.nexusmods.com/fallout4/mods/21497) implements MCM functionality in Fallout 4, used for customisation by many mods.

![separator](/Media/Separator.png)

# Frameworks

- [DEF_UI](https://www.nexusmods.com/fallout4/mods/10654) is required for icon tagging and customising the interface.
- [HUD Framework](https://www.nexusmods.com/fallout4/mods/20309) is required for some of the interface mods. The DEF_UI Patch was installed as well.
- [Bullet Counter Reload System](https://www.nexusmods.com/fallout4/mods/41178) finally fixes the inconsistency between shots fired and bullets being reloaded.
- [Workshop Framework](https://www.nexusmods.com/fallout4/mods/35004) improves upon the settlement system with rewritten scripts and many new features.

![separator](/Media/Separator.png)

# Item Sorting

- [Valdacil's Item Sorting](https://www.nexusmods.com/fallout4/mods/3877) is my preferred sorting overhaul, although I heavily customised all files.
- [Updated IconLibs2 for DEF_UI](https://www.nexusmods.com/fallout4/mods/13957) contains new and improved icons for DEF_UI. Some of the new icons are used in my tweaked version of VIS.

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

![separator](/Media/Separator.png)

# Fixes

- [Faster Workshop (Workshop Lag Fix)](https://www.nexusmods.com/fallout4/mods/35382)
- [Crafting Highlight Fix](https://www.nexusmods.com/fallout4/mods/27479)
- [Console Name Fix](https://www.nexusmods.com/fallout4/mods/25568)
- [Smooth First Person Sprint - Less Jerkiness and Stutter](https://www.nexusmods.com/fallout4/mods/29828)
- [Fixed Gobo Effects](https://www.nexusmods.com/fallout4/mods/27445)
- [Wetness Shader Fix](https://www.nexusmods.com/fallout4/mods/23389)
- [Fixed Protectron Textures](https://www.nexusmods.com/fallout4/mods/27144)
- [Eye Normal Map Fix](https://www.nexusmods.com/fallout4/mods/819)
- [Workshop Lightbulb Emittance Fix](https://www.nexusmods.com/fallout4/mods/8709)
- [Power Armor Map Fix](https://www.nexusmods.com/fallout4/mods/8854)

![separator](/Media/Separator.png)

# Tweaks

- [Hush Dogmeat - No Sounds While Sneaking](https://www.nexusmods.com/fallout4/mods/3855)
- [Docile Radstags](https://www.nexusmods.com/fallout4/mods/3208)
- [No Lockpick Activate](https://www.nexusmods.com/fallout4/mods/38675)
- [Scrolling Doesn't Switch PoV](https://www.nexusmods.com/fallout4/mods/38673)

![separator](/Media/Separator.png)

# Interface

- [Full Dialogue Interface](https://www.nexusmods.com/fallout4/mods/1235), Horizontal Brackets without numbers version.
- [String Patches for Full Dialogue Interface](https://www.nexusmods.com/fallout4/mods/41659)
- [Immersive HUD](https://www.nexusmods.com/fallout4/mods/20830) 
- [Holotime - HUD Clock Widget](https://www.nexusmods.com/fallout4/mods/20300)
- [Improved Map with Visible Roads](https://www.nexusmods.com/fallout4/mods/1215), chose default options for all three maps (Commonwealth, Far Harbor, Nuka World).
- [Small Map Markers](https://www.nexusmods.com/fallout4/mods/13400), selected 75% size option.
- [Ultimate (Main) Menus (Video Replacer) - Stormy Weathers](https://www.nexusmods.com/fallout4/mods/9762/?tab=files)
- [CCCleaner](https://www.nexusmods.com/fallout4/mods/26592)
- [Clock Widget - Show Real Time While Loading](https://www.nexusmods.com/fallout4/mods/26759)

![separator](/Media/Separator.png)

# Weathers

- [True Storms](https://www.nexusmods.com/fallout4/mods/4472) turns the overcast, rainy, and stormy weathers into much more intense experiences with many additional features such as sneak buffs in foggy weathers as well as new textures and sound effects. FOMOD choices:
  - 3x radiation damage in the Glowing Sea (18 rads/sec)
  - 2x radiation damage in the Far Habor fog (6 rads/sec)
  - standard vanilla sunsets
  - new heavy fogs (may impact performance on weaker systems)
- [True Nights](https://www.nexusmods.com/fallout4/mods/9253) is a beautiful addition to True Storms for atmospheric nights that are not impossibly dark.

![separator](/Media/Separator.png)

# Lighting

- [Polluted Climate - Tweaked Interiors](https://www.nexusmods.com/fallout4/mods/33774) overhauls the general tone and saturation of interior image spaces.
- [Interiors Enhanced - Darker Ambient Light and Fog](https://www.nexusmods.com/fallout4/mods/8768/)

![separator](/Media/Separator.png)

# LUT

This is completely optional. LUTs affect the overall colours without impacting performance. Only enable one at a time and figure out which one you like best.

- [Fallout 4 Enhanced Color Correction](https://www.nexusmods.com/fallout4/mods/5060)
- [Fallout 4 Enhanced Color Correction - Gloom](https://www.nexusmods.com/fallout4/mods/5060)
- [Fallout 4 Neutral LUTs](https://www.nexusmods.com/fallout4/mods/1016)

![separator](/Media/Separator.png)

# Landscape

- [Natural Landscapes 4K](https://www.nexusmods.com/fallout4/mods/38841) (turned all ESLs into ESP-FEs)
  - Natural Landscapes 4K
  - Natural Roads 4K
  - Natural Rocks
- [Quintessential Quarries 4K](https://www.nexusmods.com/fallout4/mods/44163) (turned the ESL into an ESP-FE)
- [Lush Landscapes - Dried Edition](https://www.nexusmods.com/fallout4/mods/23532)
- [Grass Reworked - Lush Landscapes](https://www.nexusmods.com/fallout4/mods/37891)
- [Indubitable Ivy - Unhealthy](https://www.nexusmods.com/fallout4/mods/42390)
- [Grimey Puddles (Flickering Puddle Fix)](https://www.nexusmods.com/fallout4/mods/39329/)
- [WET - Water Enhancement Textures](https://www.nexusmods.com/fallout4/mods/20775)
- [WAVE - Wave Animations Vanilla Enhanced](https://www.nexusmods.com/fallout4/mods/41568)

![separator](/Media/Separator.png)

# Vehicles

- [Vehicle Overhaul](https://www.nexusmods.com/fallout4/mods/18732)
- [Spiff's Military Vehicles Retextured](https://www.nexusmods.com/fallout4/mods/43721) (turned the ESL into an ESP-FE)
- [Train Engine - Game Jam 2015 Edition](https://www.nexusmods.com/fallout4/mods/34307) (turned the ESL into an ESP-FE)
- [Simple Yellow Forklift](https://www.nexusmods.com/fallout4/mods/37296) (turned the ESL into an ESP-FE)

![separator](/Media/Separator.png)

# Architecture

- [Langley's HD Texture Workshop (Packed)](https://www.nexusmods.com/fallout4/mods/23500) (ESL-ified the ESP)
- [Fallout 4 Ultimate Window Overhaul](https://www.nexusmods.com/fallout4/mods/43458)
- [Burly Bunkers 4K](https://www.nexusmods.com/fallout4/mods/44236) (turned the ESL into an ESP-FE)
- [Gritty Subway Stations 4K](https://www.nexusmods.com/fallout4/mods/36157) (ESL-ified the ESP)

![separator](/Media/Separator.png)

# Creatures

- [Assaultron HD](https://www.nexusmods.com/fallout4/mods/36045) (Medium version)

![separator](/Media/Separator.png)

# Body & Skin

- [Caliente's Beautiful Bodies Enhancer (CBBE)](https://www.nexusmods.com/fallout4/mods/15), Nevernude option with CBBE Reduced for dismemberment and the vanilla-shape body. Merged CBBE Reduced into the main file.
- [Skeletal Adjustments for CBBE](https://www.nexusmods.com/fallout4/mods/39006)
- [Valkyr Female Face and Body Textures](https://www.nexusmods.com/fallout4/mods/3841)
- [CBBE Ida Body Texture](https://www.nexusmods.com/fallout4/mods/10726)
- [Enhanced Vanilla Bodies](https://www.nexusmods.com/fallout4/mods/22110)

![separator](/Media/Separator.png)

# Overhauls

- [Everyone's Best Friend](https://www.nexusmods.com/fallout4/mods/13459)
- [EBF UFO4P Compatibility Fix](https://www.nexusmods.com/fallout4/mods/43409)

![separator](/Media/Separator.png)

# Voice & Sound

- [No Player Comments - Chems Only](https://www.nexusmods.com/fallout4/mods/5702)
