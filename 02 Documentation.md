![logo](Media/Logo.png)

**TABLE OF CONTENTS**
- [The Documentation](#the-documentation)
  - [Preface](#preface)
  - [Features](#features)
  - [My Tools](#my-tools)
  - [Preparations](#preparations)
  - [Game Folder Files](#game-folder-files)
- [Essentials](#essentials)
- [Frameworks](#frameworks)
- [Item Sorting](#item-sorting)
  - [Overview](#overview)
  - [Valdacil's Item Sorting](#valdacils-item-sorting)
  - [Phoenix - Weapon Sorting](#phoenix---weapon-sorting)
  - [Armor Tab Sorting](#armor-tab-sorting)
  - [Phoenix - Armor Sorting](#phoenix---armor-sorting)
  - [Phoenix - Power Armor Sorting](#phoenix---power-armor-sorting)
  - [Phoenix - Cosmetics Sorting](#phoenix---cosmetics-sorting)
  - [Custom DEF_INV_TAGS](#custom-def_inv_tags)
- [Simple Crafting Stations](#simple-crafting-stations)
- [Fixes](#fixes)
- [Tweaks](#tweaks)
- [Interface](#interface)
- [Weathers](#weathers)
- [Lighting](#lighting)
- [LUT](#lut)
- [Visual Effects](#visual-effects)
- [Landscape](#landscape)
- [Vehicles](#vehicles)
- [Architecture](#architecture)
- [Creatures](#creatures)
- [Body & Skin](#body--skin)
- [Overhauls](#overhauls)
- [Power Armor](#power-armor)
- [Settlements](#settlements)
- [Sound Effects](#sound-effects)
- [Music](#music)
- [Player Voice](#player-voice)
- [Late Loader](#late-loader)

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

## My Tools

- SSEEdit
- zEdit
- Bethesda Archive Extractor
- [XWM Music Converter](https://www.nexusmods.com/fallout4/mods/24888)

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
- The [Unofficial Fallout 4 Patch](https://www.nexusmods.com/fallout4/mods/4598) includes numerous bug and consistency fixes. I removed the modgroups file.
- [Private Profile Redirector](https://www.nexusmods.com/fallout4/mods/33947) speeds up the game launch. It requires F4SE and the xSE Plugin Preloader.
- [Achievements](https://www.nexusmods.com/fallout4/mods/12465) allows for Steam achievements to be earned in a modded playthrough.
- [Mod Configuration Menu](https://www.nexusmods.com/fallout4/mods/21497) implements MCM functionality in Fallout 4, used for customisation by many mods.
- [Canary Save File Monitor](https://www.nexusmods.com/fallout4/mods/44949) can detect data loss in saves for supported mods.
- [Better Console](https://www.nexusmods.com/fallout4/mods/26582) mostly helps me with figuring out issues ingame by allowing me to check an object's form ID.

![separator](/Media/Separator.png)

# Frameworks

- [DEF_UI](https://www.nexusmods.com/fallout4/mods/10654) is required for icon tagging and customising the interface.
- [HUD Framework](https://www.nexusmods.com/fallout4/mods/20309) is required for some of the interface mods. The DEF_UI Patch was installed as well.
- [Bullet Counter Reload System](https://www.nexusmods.com/fallout4/mods/41178) finally fixes the inconsistency between shots fired and bullets being reloaded.
- [Workshop Framework](https://www.nexusmods.com/fallout4/mods/35004) improves upon the settlement system with rewritten scripts and many new features.
- [Transfer Settlements - Shareable Settlement Blueprints](https://www.nexusmods.com/fallout4/mods/22442) enables import and export of settlement builds.
- [Settlement Menu Manager](https://www.nexusmods.com/fallout4/mods/24204) offers a simple, script-based solution for implementing new workshop menus.

![separator](/Media/Separator.png)

# Item Sorting

## Overview

- [Valdacil's Item Sorting](https://www.nexusmods.com/fallout4/mods/3877) is my preferred sorting overhaul, although I heavily customised all files.
- [Updated IconLibs2 for DEF_UI](https://www.nexusmods.com/fallout4/mods/13957) contains new and improved icons for DEF_UI. Some of the new icons are used in my tweaked version of VIS.

## Valdacil's Item Sorting

While [Valdacil's Item Sorting](https://www.nexusmods.com/fallout4/mods/3877) has technically been superceeded by [VIS-G Item Sorting](https://www.nexusmods.com/fallout4/mods/33383). However, I am a stubborn person, and much prefer VIS' more simplistic sorting and icons over VIS-G, so that is what I am using.

Added DLC support for all plugins listed below. Forwarded UFO4P edits where necessary.

- **ValdacilsItemSorting-ExplosivesSortBottom.esp:** Added new tag {Trap} for the Far Harbor traps (which are classified as explosives).
- **ValdacilsItemSorting-AidReducedWeight.esp:** Chems and Syringer Ammo have weight again, but quest items remain weightless. Set weight for gourds and melons to 0.5.
- **ValdacilsItemSorting-Misc.esp**
- **ValdacilsItemSorting-JunkBetter+DEF_INV.esp:** Merged NotJunk changes into BetterJunkDEF_INV. Renamed all empty bottles to "Empty {Bottle Type}". Also Shem Drowne's Skull is listed as (Unique) now and can no longer be scrapped.
- **ValdacilsItemSorting-Mods.esp** Vanilla weight version.
- **ValdacilsItemSorting-Ammo.esp** Vanilla weight version. Mini Nukes now have a unique icon.
- **ValdacilsItemSorting-Perks.esp**

## Phoenix - Weapon Sorting

Weapons are split up as follows:

- (Generic)
- [Heavy]
- {Special}
- |Melee|

I removed the **Deliverer** from the dn_CommonWeapon INNR so that it doesn't get its name changed when you upgrade it. It's a unique weapon anyway.

Some Nuka World weapons (Thirst Zapper, Acid Soaker, Paddle Ball, Animatronic Alien Blaster) also had the WeaponTypePistol keyword added to them so that they can show up on weapon racks.

Melee weapons have VIS sorting, although I redid Ruleset #0 for my new Melee weapon tags and removed the Ruleset for material / color.

**Melee:** `|Bat| Swatter of Ghoul Slaying (Barbed)`

## Armor Tab Sorting

With the Armor, Power Armor and Clothing Sorting modules, items will be sorted in the Armor tab as follows:

- (Accessories)
- [Outfits]
- {Armor pieces}
- |Power Armor|

## Phoenix - Armor Sorting

While VIS uses AWKCR keywords to distinguish the different types of Disciple (Metal, Strapped Spiked, Wrapped) and Pack (Bone, Stuffed) armor pieces in the dn_CommonArmor INNR, there are no distinct names for the Heavy Operator pieces. I fixed that.

I also slightly tweaked the INNR so that the resulting names have the armor slot in them, eg "{LegL} Operators Heavy Left Leg" instead of "{LegL} Operators Heavy Armor" (the tags are hidden).

## Phoenix - Power Armor Sorting

**Vanilla:** `Jet Pack Atom Cats T-60c Helmet`

**Modded:** `|PA Helmet| T-60 Helmet Mk. 3 of Cloaking (Jet Pack)`

- Ruleset #0: The sorting tag (power armor piece, sort by slot).
- Ruleset #1: The type of power armor (T-60, X-01, etc).
- Ruleset #2: The armor piece in question (torso, helmet, etc).
- Ruleset #3: The upgrade level (used to be different for all PAs).
- Ruleset #4: The legendary effect if the item is legendary.
- Ruleset #5: The additional enhancement (like Bracers or Databased).

In the ArmorBySlot override, I discovered that while there are several INNR lists for power armor, they are identical. I pointed all power armor sets at the primary **dn_PowerArmor** list and disregarded the other ones. I also replicated keywords that AWKCR added for four paint jobs that were missing in the original game, renamed "Raider Power > Raider" and "Overboss Power > Power" as well as added the piece to the name "X-01 Mk. 1 > X-01 Left Arm Mk. 1".

The naming scheme is essentially the one from VIS with some small tweaks. I added Ruleset #2 and removed the space (Mk.1 > Mk. 1) in Ruleset #3. I also removed Ruleset #6 which added tags based on the material because this will later be covered by PAMAP.

## Phoenix - Cosmetics Sorting

Assigning tags through the dn_Clothes INNR is unfortunately fairly unreliable, I have added the tags manually to each piece of clothing or apparel. I am using the same categories as VIS. The tags are:


| Acessories  | Outfits     | Faction-Specific |
| ----------- | ----------- | --------------   |
| (Hat)       | [Casual]    | [Military]       |
| (Eyewear)   | [Dapper]    | [Raider]         |
| (Mask)      | [Dress]     | [Vault Tec]      |
| (Bandana)   | [Rugged]    | [BOS]            |
| (Bandolier) | [Skimpy]    | [Railroad]       |
| (Ring)      | [Skimpy]    | [Minutemen]      |
| (Dog)       | [Biosuit]   | [Institute]      |
|             |             | [COA]            |
|             |             | [Diamond City]   |
|             |             | [Super Mutant]   |

## Custom DEF_INV_TAGS

- Added many new tags for the custom sorting modules.
- Set `hidetag` for armor / power armor pieces and weapons to 'true'.

![separator](/Media/Separator.png)

# Simple Crafting Stations

### Implementation

Since I did not want to include AWKCR with all its feature creep, I initially thought that item crafting would be impossible altogether. Then I found [Simple Immersive Chem Benches for Crafting](https://www.nexusmods.com/fallout4/mods/44691), and it's brilliant. What it does is change the chem bench models so that they rather look they general crafting benches. My plugin changes their name (Chemistry Station > Crafting Workbench) and adds a bunch of new menus (keywords) to sort mod-added items into.

- Phoenix - Simple Crafting Stations
- [Simple Immersive Chem Benches for Crafting](https://www.nexusmods.com/fallout4/mods/44691)

### Patches

- **Workshop Framework:** Disables non-VIS holotape. Moves VIS holotape to the MOD CONFIG menu.
- **True Storms:** Moved both holotapes to the MOD CONFIG menu.

![separator](/Media/Separator.png)

# Fixes

- [Faster Workshop (Workshop Lag Fix)](https://www.nexusmods.com/fallout4/mods/35382)
- [Crafting Highlight Fix](https://www.nexusmods.com/fallout4/mods/27479)
- [Console Name Fix](https://www.nexusmods.com/fallout4/mods/25568)
- [Fixed Gobo Effects](https://www.nexusmods.com/fallout4/mods/27445)
- [Wetness Shader Fix](https://www.nexusmods.com/fallout4/mods/23389)
- [Fixed Alpha Maps](https://www.nexusmods.com/fallout4/mods/28974), ESL-ified the plugin.
- [Fixed Protectron Textures](https://www.nexusmods.com/fallout4/mods/27144)
- [Eye Normal Map Fix](https://www.nexusmods.com/fallout4/mods/819)
- [Workshop Spotlight Fix](https://www.nexusmods.com/fallout4/mods/11090), DLC version, default range, and no shadows.
- [Workshop Lightbulb Emittance Fix](https://www.nexusmods.com/fallout4/mods/8709)
- [Power Armor Map Fix](https://www.nexusmods.com/fallout4/mods/8854)
- [Duffle Bag Sound Fix](https://www.nexusmods.com/fallout4/mods/44855)
- [Starlight Drive-In LOD Fix](https://www.nexusmods.com/fallout4/mods/23034), turned the ESL into an ESP-FE.
- [Nuka-World Bottle Scenery Fix](https://www.nexusmods.com/fallout4/mods/17853), ESL-ified the plugin.
- [No More Floating Razorgrain](https://www.nexusmods.com/fallout4/mods/13823)
- [Companion Stealth Distance Fix](https://www.nexusmods.com/fallout4/mods/15823), ESL-ified the plugin.
- [Weapon Rack Fixes](https://www.nexusmods.com/fallout4/mods/19324), ESL-ified the plugin. Removed Weapon edits (keyword already added in Phoenix - Weapon Sorting).
- [Flicker Fixer](https://www.nexusmods.com/fallout4/mods/35720?)

![separator](/Media/Separator.png)

# Tweaks

- [Faster Terminal Displays](https://www.nexusmods.com/fallout4/mods/937), 10x version, ESL-ified the plugin.
- [Easy Hacking](https://www.nexusmods.com/fallout4/mods/266), ESL-ified the plugin.
- [Hush Dogmeat - No Sounds While Sneaking](https://www.nexusmods.com/fallout4/mods/3855), ESL-ified the plugin.
- [Docile Radstags](https://www.nexusmods.com/fallout4/mods/3208), ESL-ified the plugin.
- [Vertibird Jump](https://www.nexusmods.com/fallout4/mods/20190)
- [No Lockpick Activate](https://www.nexusmods.com/fallout4/mods/38675)
- [Scrolling Doesn't Switch PoV](https://www.nexusmods.com/fallout4/mods/38673)
- [Laser Weapons 1st Person Reposition](https://www.nexusmods.com/fallout4/mods/23102), ESL-ified the plugin.
- [Less Annoying Berry Mentats](https://www.nexusmods.com/fallout4/mods/11838), ESL-ified the plugin.
- [Keep Radiants in the Commonwealth](https://www.nexusmods.com/fallout4/mods/25934), ESL-ified the plugin, forwarded some UFO4P edits.
- [No Aggro Impact Landing (Power Armor)](https://www.nexusmods.com/fallout4/mods/9019), ESL-ified the plugin.
- [Depth of Field (DOF) Removal](https://www.nexusmods.com/fallout4/mods/4172/?), Keep Inspection version, ESL-ified the plugin.

![separator](/Media/Separator.png)

# Interface

- [Full Dialogue Interface](https://www.nexusmods.com/fallout4/mods/1235), Horizontal Brackets without numbers version.
- [String Patches for Full Dialogue Interface](https://www.nexusmods.com/fallout4/mods/41659), ESL-ified the plugin.
- [Immersive HUD](https://www.nexusmods.com/fallout4/mods/20830) 
- [Holotime - HUD Clock Widget](https://www.nexusmods.com/fallout4/mods/20300)
- [Improved Map with Visible Roads](https://www.nexusmods.com/fallout4/mods/1215), chose default options for all three maps (Commonwealth, Far Harbor, Nuka World).
- [Small Map Markers](https://www.nexusmods.com/fallout4/mods/13400), selected 75% size option.
- [LooksMenu](https://www.nexusmods.com/fallout4/mods/12631)
- [Ultimate (Main) Menus (Video Replacer) - Stormy Weathers](https://www.nexusmods.com/fallout4/mods/9762/?tab=files)
- [CCCleaner](https://www.nexusmods.com/fallout4/mods/26592)
- [Clock Widget - Show Real Time While Loading](https://www.nexusmods.com/fallout4/mods/26759)

![separator](/Media/Separator.png)

# Weathers

- [True Storms](https://www.nexusmods.com/fallout4/mods/4472) turns the overcast, rainy, and stormy weathers into much more intense experiences with many additional features such as sneak buffs in foggy weathers as well as new textures and sound effects. I added sorting tags to the included config holotapes. FOMOD choices:
  - 3x radiation damage in the Glowing Sea (18 rads/sec).
  - 2x radiation damage in the Far Habor fog (6 rads/sec).
  - Standard vanilla sunsets.
  - New heavy fogs (may impact performance on weaker systems).
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

# Visual Effects

- [CROSS Crit Gore-verhaul](https://www.nexusmods.com/fallout4/mods/23780), update (BSA) was merged into the main file. Merged records from the Far Harbor plugin into the main file and deleted it.

![separator](/Media/Separator.png)

# Landscape

- [Natural Landscapes 4K](https://www.nexusmods.com/fallout4/mods/38841), turned all ESL plugins into ESP-FEs.
  - Natural Landscapes 4K
  - Natural Roads 4K
  - Natural Rocks
- [Quintessential Quarries 4K](https://www.nexusmods.com/fallout4/mods/44163), turned the ESL plugin into an ESP-FE.
- [Lush Landscapes - Dried Edition](https://www.nexusmods.com/fallout4/mods/23532)
- [Grass Reworked - Lush Landscapes](https://www.nexusmods.com/fallout4/mods/37891), ESL-ified the plugin.
- [Indubitable Ivy - Unhealthy](https://www.nexusmods.com/fallout4/mods/42390)
- [Grimey Puddles (Flickering Puddle Fix)](https://www.nexusmods.com/fallout4/mods/39329/)
- [WET - Water Enhancement Textures](https://www.nexusmods.com/fallout4/mods/20775)
- [WAVE - Wave Animations Vanilla Enhanced](https://www.nexusmods.com/fallout4/mods/41568)

![separator](/Media/Separator.png)

# Vehicles

- [Vehicle Overhaul](https://www.nexusmods.com/fallout4/mods/18732)
- [Spiff's Military Vehicles Retextured](https://www.nexusmods.com/fallout4/mods/43721), turned the ESL plugin into an ESP-FE.
- [Train Engine - Game Jam 2015 Edition](https://www.nexusmods.com/fallout4/mods/34307), turned the ESL plugin into an ESP-FE.
- [Simple Yellow Forklift](https://www.nexusmods.com/fallout4/mods/37296), turned the ESL plugin into an ESP-FE.

![separator](/Media/Separator.png)

# Architecture

- [Langley's HD Texture Workshop (Packed)](https://www.nexusmods.com/fallout4/mods/23500), ESL-ified the ESP.
- [Fallout 4 Ultimate Window Overhaul](https://www.nexusmods.com/fallout4/mods/43458)
- [Burly Bunkers 4K](https://www.nexusmods.com/fallout4/mods/44236), turned the ESL plugin into an ESP-FE.
- [Gritty Subway Stations 4K](https://www.nexusmods.com/fallout4/mods/36157), ESL-ified the ESP.

![separator](/Media/Separator.png)

# Creatures

- [Assaultron HD](https://www.nexusmods.com/fallout4/mods/36045), Medium version.

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

# Power Armor

- [Restore Power Armor Frames](https://www.nexusmods.com/fallout4/mods/20890)
- [Power Armor Animation Changes](https://www.nexusmods.com/fallout4/mods/4408)

![separator](/Media/Separator.png)

# Settlements

- [Scrapping Machine](https://www.nexusmods.com/fallout4/mods/35793) allows you to quickly scrap all your junk by tossing them into a repurposed washing machine. Changed the ESL plugin to ESP-FE.
- [Compact Crafting](https://www.nexusmods.com/fallout4/mods/18264) adds small versions of the crafting benches. I disabled the all-purpose version as I felt it was cheesy, plus junk scrapping can be done with Scrapping Machine. The Chem stations were renamed to Crafting Workbenches for consistency with Simple Crafting Stations. The BSA was replaced with the 2K textures version.

![separator](/Media/Separator.png)

# Sound Effects

- [Reverb and Ambience Overhaul](https://www.nexusmods.com/fallout4/mods/10189/?)
- [LOST Audio Tweaks](https://www.nexusmods.com/fallout4/mods/38448)
- [PAMS - Power Armor Movement Sounds](https://www.nexusmods.com/fallout4/mods/1544), light version plus Louder High Landing.

![separator](/Media/Separator.png)

# Music

Fallout Suite, Bleak Beauty and Musical Lore add many, *many* new tracks of music to the original soundtrack (without replacing any of Inon Zur's score). They were chosen for their quality and consistency with the vanilla music. All three had their plugins ESL-ified, and the added music tracks are merged into the **Phoenix - Music Patch**.

- [Fallout Suite - Soundtrack Extension for Fallout 4](https://www.nexusmods.com/fallout4/mods/15870), ESL-ified the plugin and removed one ITM.
- [Bleak Beauty - A Fallout 4 Fanmade OST](https://www.nexusmods.com/fallout4/mods/9663),ESL-ified the plugin.
- [Musical Lore - Wasteland Edition](https://www.nexusmods.com/fallout4/mods/14531),ESL-ified the plugin.
- [Elvani's Track Pack for Diamond City Radio](https://www.nexusmods.com/fallout4/mods/5467), plugin with fixed audio levels merged into the main mod folder.
- [More Where That Came From - Diamond City Radio Edition](https://www.nexusmods.com/fallout4/mods/637), forwarded new Output Model from RAO into the plugin.

![separator](/Media/Separator.png)

# Player Voice

- [No Player Comments - Chems Only](https://www.nexusmods.com/fallout4/mods/5702)

![separator](/Media/Separator.png)

# Late Loader

- [Boston FPS Fix](https://www.nexusmods.com/fallout4/mods/26286)
