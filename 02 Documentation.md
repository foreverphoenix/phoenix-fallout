![logo](Media/Logo.png)

**TABLE OF CONTENTS**
- [The Documentation](#the-documentation)
- [Game Folder Files](#game-folder-files)
- [Essentials](#essentials)
- [Frameworks](#frameworks)
- [Item Sorting](#item-sorting)
- [Simple Crafting Stations](#simple-crafting-stations)
- [Fixes](#fixes)
- [Tweaks](#tweaks)
- [Interface](#interface)
- [DEF HUD Presets](#def-hud-presets)
- [Weathers](#weathers)
- [Lighting](#lighting)
- [LUT](#lut)
- [Visual Effects](#visual-effects)
- [Landscape](#landscape)
- [Locations](#locations)
- [Retextures](#retextures)
- [Body and Skin](#body-and-skin)
- [Appearance](#appearance)
- [NPC Overhauls](#npc-overhauls)
- [Gameplay](#gameplay)
- [Balancing](#balancing)
- [Non-Player Characters](#non-player-characters)
- [Power Armor](#power-armor)
- [Quests](#quests)
- [Settlements](#settlements)
- [Sound Effects](#sound-effects)
- [Music](#music)
- [Player Voice](#player-voice)
- [Late Loader](#late-loader)

![separator](/Media/Separator.png)

# The Documentation

This page serves two purposes: One, to inform the user about the contents of this Wabbajack list, and two, remind me what I did to which files. You don't have to read it but it will help you understand how Phoenix: Fallout changes the game and what my thoughts behind each mod addition were.

**This page does not include any instructions whatsoever.** There is nothing you have to do yourself. It's just information on the Wabbajack list and my personal notes.

### My Tools

- [FO4Edit](https://www.nexusmods.com/fallout4/mods/2737)
- zEdit
- [Bethesda Archive Extractor](https://www.nexusmods.com/fallout4/mods/78)
- [Fallout 4 Texture Compressor](https://www.nexusmods.com/fallout4/mods/25691)
- [Material Editor](https://www.nexusmods.com/fallout4/mods/3635)
- [MultiXWM](https://www.nexusmods.com/fallout4/mods/3663)
- [Champollion Pex to Papyrus Decompiler](https://www.nexusmods.com/fallout4/mods/3742)
- [FOMOD Creation Tool](https://www.nexusmods.com/fallout4/mods/6821)

### Preparations

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
- [Console Commands](/Custom%20Files/Console%20Commands/README.md), custom file.

![separator](/Media/Separator.png)

# Frameworks

- [DEF_UI](https://www.nexusmods.com/fallout4/mods/10654) is required for icon tagging and customising the interface. Deleted Translation file, downloaded the F4SE plugin.
- [HUD Framework](https://www.nexusmods.com/fallout4/mods/20309) is required for some of the interface mods. The DEF_UI Patch was installed as well.
- [Bullet Counter Reload System](https://www.nexusmods.com/fallout4/mods/41178) finally fixes the inconsistency between shots fired and bullets being reloaded.
- [Workshop Framework](https://www.nexusmods.com/fallout4/mods/35004) improves upon the settlement system with rewritten scripts and many new features.
- [Transfer Settlements - Shareable Settlement Blueprints](https://www.nexusmods.com/fallout4/mods/22442) enables import and export of settlement builds.
- [Settlement Menu Manager](https://www.nexusmods.com/fallout4/mods/24204) offers a simple, script-based solution for implementing new workshop menus.
- [Phoenix - Keywords](/Custom%20Files/Phoenix%20Keywords/README.md) is a heavily stripped-down, custom AWKCR replacer, required for my sorting modules.

![separator](/Media/Separator.png)

# Item Sorting

VIS is my preferred sorting overhaul, although I heavily customised all files and created derivatives for Weapon, Cosmetic, Armor and Power Armor sorting that depend on my Keywords ESM instead of AWKCR. Details can be found [here](/Custom%20Files/Phoenix%20Sorting/README.md). All plugins were ESL-ified since they exclusively edit vanilla records.

- [Phoenix - Weapon Sorting](/Custom%20Files/Phoenix%20Sorting/README.md), custom file.
- [Phoenix - Cosmetic Sorting](/Custom%20Files/Phoenix%20Sorting/README.md), custom file.
- [Phoenix - Armor Sorting](/Custom%20Files/Phoenix%20Sorting/README.md), custom file.
- [Phoenix - Power Armor Sorting](/Custom%20Files/Phoenix%20Sorting/README.md), custom file.
- [Valdacil's Item Sorting](https://www.nexusmods.com/fallout4/mods/3877) 
- [Updated IconLibs2 for DEF_UI](https://www.nexusmods.com/fallout4/mods/13957)
- [Custom DEF_INV_TAGS xml](/Custom%20Files/Phoenix%20Sorting/README.md), custom file.

![separator](/Media/Separator.png)

# Simple Crafting Stations

### Implementation

Since I did not want to include AWKCR with all its feature creep, I initially thought that item crafting would be impossible altogether. Then I found [Simple Immersive Chem Benches for Crafting](https://www.nexusmods.com/fallout4/mods/44691), and it's brilliant. What it does is change the chem bench models so that they rather look they general crafting benches. My plugin changes their name (Chemistry Station > Crafting Workbench) and adds a bunch of new menus (keywords) to sort mod-added items into.

- Phoenix - Simple Crafting Stations
- [Simple Immersive Chem Benches for Crafting](https://www.nexusmods.com/fallout4/mods/44691)

### Integration

The Integration plugin is a unified patch that changes the category keyword for all relevant, mod-added items. When necessary, I also disabled redundant recipes and removed crafting requirements for any mod configuration holotapes.

- **Workshop Framework:** Disabled non-VIS holotape crafting. Moved VIS holotape to the MOD CONFIG menu. No longer requires scrap to craft.
- **Transfer Settlements:** Moved holotape to the MOD CONFIG menu. No longer requires scrap to craft.
- **Settlement Menu Manager:** Disabled non-VIS holotape crafting. Moved VIS holotape to the MOD CONFIG menu. No longer requires scrap to craft.
- **True Storms:** Moved both holotapes to the MOD CONFIG menu.
- **NPCs Travel:** Moved config holotape to the MOD CONFIG menu.
- **Restore Power Armor Frame:** Moved holotape to the MOD CONFIG menu. No longer requires scrap to craft.

![separator](/Media/Separator.png)

# Fixes

- [Faster Workshop (Workshop Lag Fix)](https://www.nexusmods.com/fallout4/mods/35382)
- [Crafting Highlight Fix](https://www.nexusmods.com/fallout4/mods/27479)
- [Console Name Fix](https://www.nexusmods.com/fallout4/mods/25568)
- [Grab the Damn Mag](https://www.nexusmods.com/fallout4/mods/17299)
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
- [Companion Stealth Distance Fix](https://www.nexusmods.com/fallout4/mods/15823), ESL-ified the plugin.
- [Weapon Rack Fixes](https://www.nexusmods.com/fallout4/mods/19324), ESL-ified the plugin. Removed Weapon edits (keyword already added in Phoenix - Weapon Sorting).
- [Flicker Fixer](https://www.nexusmods.com/fallout4/mods/35720?)
- [Marine Wet Suit Material Fix](https://www.nexusmods.com/fallout4/mods/19843)
- [Decayed Army Fatigues Fix](https://www.nexusmods.com/fallout4/mods/43089), 2K version.
- [Valentine Jaw Sync](https://www.nexusmods.com/fallout4/mods/42985)
- [Molerat Disease Fix](https://www.nexusmods.com/fallout4/mods/41597)

![separator](/Media/Separator.png)

# Tweaks

- [Easy Hacking](https://www.nexusmods.com/fallout4/mods/266), ESL-ified the plugin.
- [No Crafting Experience](https://www.nexusmods.com/fallout4/mods/15203), Automatron version, ESL-ified the plugin.
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
- [Not So Bright Pins](https://www.nexusmods.com/fallout4/mods/35097)
- [Armor Workbench No Fire Barrel](https://www.nexusmods.com/fallout4/mods/23199)
- [Randomized Diamond City GUard Outfits](https://www.nexusmods.com/fallout4/mods/12100/?), ESL-ified the plugin.
- [Dismemberment Tweaks](/Custom%20Files/Dismemberment%20Tweaks/README.md), custom file.
- [No Legendary Items from Creatures](https://www.nexusmods.com/fallout4/mods/21864), ESL-ified the plugin.
- [Binary Speech Checks](https://www.nexusmods.com/fallout4/mods/2100), Normal Edition, ESL-ified the plugin.
- [No Halloween Decoration](https://www.nexusmods.com/fallout4/mods/11503), forwarded PreVis edits from the UFO4P, ESL-ified the plugin.
- [Corpse Collision](https://www.nexusmods.com/fallout4/mods/37133), turned the ESL into an ESP-FE.
- [No Lollygagging Settlers](https://www.nexusmods.com/fallout4/mods/10461), ESL-ified the plugin.
- [Better Female Sitting Animation](https://www.nexusmods.com/fallout4/mods/3426)
- [Better Bloatflies](https://www.nexusmods.com/fallout4/mods/44117)

![separator](/Media/Separator.png)

# Interface

- [Full Dialogue Interface](https://www.nexusmods.com/fallout4/mods/1235), Horizontal Brackets without numbers version.
- [String Patches for Full Dialogue Interface](https://www.nexusmods.com/fallout4/mods/41659), ESL-ified the plugin.
- [Immersive HUD](https://www.nexusmods.com/fallout4/mods/20830)
- [Power Armor HUD - paHUD](https://www.nexusmods.com/fallout4/mods/21622)
- [Holotime - HUD Clock Widget](https://www.nexusmods.com/fallout4/mods/20300)
- [Improved Map with Visible Roads](https://www.nexusmods.com/fallout4/mods/1215), chose default options for all three maps (Commonwealth, Far Harbor, Nuka World).
- [Small Map Markers](https://www.nexusmods.com/fallout4/mods/13400), selected 75% size option.
- [LooksMenu](https://www.nexusmods.com/fallout4/mods/12631)
- [Ultimate (Main) Menus (Video Replacer) - Stormy Weathers](https://www.nexusmods.com/fallout4/mods/9762/?tab=files)
- [CCCleaner](https://www.nexusmods.com/fallout4/mods/26592)
- [Clock Widget - Show Real Time While Loading](https://www.nexusmods.com/fallout4/mods/26759)

![separator](/Media/Separator.png)

# DEF HUD Presets

Only have one active at a time.

- DEF_HUD - Phoenix Preset

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

- [Enhanced Blood Textures](https://www.nexusmods.com/fallout4/mods/212), Basic version.
- [Bloody Mess - Enhanced Blood Textures Add-on](https://www.nexusmods.com/fallout4/mods/6549), 2K version.
- [Gore Overhaul](https://www.nexusmods.com/fallout4/mods/21216), Cuts and Bruises file.
- [CROSS Crit Gore-verhaul](https://www.nexusmods.com/fallout4/mods/23780), update (BSA) was merged into the main file. Merged records from the Far Harbor plugin into the main file and deleted it.

![separator](/Media/Separator.png)

# Landscape

- [Natural Landscapes 4K](https://www.nexusmods.com/fallout4/mods/38841), turned all ESL plugins into ESP-FEs.
  - Natural Landscapes 4K
  - Natural Roads 4K
  - Natural Rocks
- [Quintessential Quarries 4K](https://www.nexusmods.com/fallout4/mods/44163), turned the ESL plugin into an ESP-FE.
- [Lush Landscapes - Dried Edition](https://www.nexusmods.com/fallout4/mods/23532), packed loose assets into BA2s.
- [Grass Reworked - Lush Landscapes](https://www.nexusmods.com/fallout4/mods/37891), ESL-ified the plugin.
- [Indubitable Ivy - Unhealthy](https://www.nexusmods.com/fallout4/mods/42390)
- [Grimey Puddles (Flickering Puddle Fix)](https://www.nexusmods.com/fallout4/mods/39329/)
- [WET - Water Enhancement Textures](https://www.nexusmods.com/fallout4/mods/20775)
- [WAVE - Wave Animations Vanilla Enhanced](https://www.nexusmods.com/fallout4/mods/41568)

![separator](/Media/Separator.png)

# Locations

- [The Sanctuary Bridge](https://www.nexusmods.com/fallout4/mods/22949), forwarded a UFO4P edit.

![separator](/Media/Separator.png)

# Retextures

### Main

- [Langley's HD Texture Workshop (Packed)](https://www.nexusmods.com/fallout4/mods/23500), ESL-ified the ESP.
- [Patch Job - Fill Those Holes](https://www.nexusmods.com/fallout4/mods/1934)
- [Better Settlements and Camps 2](https://www.nexusmods.com/fallout4/mods/2461), 2K version.
- [Haul'd Out](https://www.nexusmods.com/fallout4/mods/5086), Pier 2K, Warehouse 2K, Warehouse NoHolesMetal 2K. All files merged into one folder.
- [Fallout 4 Ultimate Window Overhaul](https://www.nexusmods.com/fallout4/mods/43458)
- [Burly Bunkers 4K](https://www.nexusmods.com/fallout4/mods/44236), turned the ESL plugin into an ESP-FE.
- [Gritty Subway Stations 4K](https://www.nexusmods.com/fallout4/mods/36157), ESL-ified the ESP.
- [Shack Walls Redone](https://www.nexusmods.com/fallout4/mods/2174), Dull 2K version.
- [NMC's Sanctuary Bridge](https://www.nexusmods.com/fallout4/mods/28138), 2K regular version.
- [Really Red Rocket](https://www.nexusmods.com/fallout4/mods/9870), 2K Worn version.
- [Vehicle Overhaul](https://www.nexusmods.com/fallout4/mods/18732)
- [Spiff's Military Vehicles Retextured](https://www.nexusmods.com/fallout4/mods/43721), turned the ESL plugin into an ESP-FE.
- [Spiff's Workshop](https://www.nexusmods.com/fallout4/mods/45002), ESls turned to ESP-FE, downloaded files:
  - Simple Yellow Forklifts
  - Train Engine - Game Jam 2015 Edition

### Clutter

- [Chem Redux](https://www.nexusmods.com/fallout4/mods/2099), No Glow version, forwarded UFO4P and VIS changes, ESL-ified the plugin.
- [Grey Tortoise Cigarettes Redux](https://www.nexusmods.com/fallout4/mods/28204)
- [Bottles Labels Overhaul](https://www.nexusmods.com/fallout4/mods/1500), 1K version, no water bottles.
- [Retextured Water - by Ben Ephla](https://www.nexusmods.com/fallout4/mods/20399)
- [Components Redone](https://www.nexusmods.com/fallout4/mods/25188), 1K version and copper fix, selected Vanilla Weights VIS in the FOMOD, ESL-ified the plugin.
- [Better Ammo Boxes](https://www.nexusmods.com/fallout4/mods/8087), all three main files, merged together into one mod folder, selected 1K variants in the FOMOD.
- [Retextured First Aid Kits](https://www.nexusmods.com/fallout4/mods/16841), v1.
- [PatrickJr's Redone Bobbleheads](https://www.nexusmods.com/fallout4/mods/12062)
- [Robot Model Kit 2K Retextures](https://www.nexusmods.com/fallout4/mods/24189)
- [Nuka Recipe Book 2K Retextures](https://www.nexusmods.com/fallout4/mods/32292), ESL version, turned the ESL into an ESP-FE.
- [Lockpicking Retexture](https://www.nexusmods.com/fallout4/mods/19935), ESL version, turned the ESL into an ESP-FE.

### Apparel 

- [Proto Vault Suit](https://www.nexusmods.com/fallout4/mods/2187/?), vanilla replacer.
- [Hazmat Suit Redux](https://www.nexusmods.com/fallout4/mods/31799), forwarded sorting tags and ESL-ified the plugin.
- [Combat Armor No Star Decal](https://www.nexusmods.com/fallout4/mods/524/?)
- [Robot Armor Retextured](https://www.nexusmods.com/fallout4/mods/12187), 2K black version.
- [Mechanist Armor Retextured](https://www.nexusmods.com/fallout4/mods/13053), 2K version.
- [Marine Helmet with Tactical Hood](https://www.nexusmods.com/fallout4/mods/14340)
- [Piper's Coat HR](https://www.nexusmods.com/fallout4/mods/14010), downsized coat textures to 2K.
- [Better House Dress Shoes](https://www.nexusmods.com/fallout4/mods/36704), 2K version.
- [Eyewear and Mask Retexture](https://www.nexusmods.com/fallout4/mods/5021), removed Patrolman sunglasses edit (feature creep) and ESL-ified the plugin.

### Pip-Boy

This section contains multiple Pip-Boy retextures. Only activate one.

- [Immersive Wastelander Series - Pip-Boy](https://www.nexusmods.com/fallout4/mods/486), all three versions.
- [Pipboy UHD](https://www.nexusmods.com/fallout4/mods/40633), 2K version.
- [Rusty Black Pip-Boy](https://www.nexusmods.com/fallout4/mods/2279)
  
### Weapons

- [Authentic Handmade Weaponry (Pipe Gun Retexture)](https://www.nexusmods.com/fallout4/mods/43655), 2K version, turned the ESL into an ESP-FE.
- [10mm HD](https://www.nexusmods.com/fallout4/mods/33107), 2K version.
- [The Fantastic Forty Four](https://www.nexusmods.com/fallout4/mods/24398)
- [The Humble Hunting Rifle](https://www.nexusmods.com/fallout4/mods/24642), vanilla mesh.
- [ScratchMade - New Double Barrel Shotgun Textures](https://www.nexusmods.com/fallout4/mods/2211)
- [ScratchMade - New Combat Shotgun and Rifle Textures](https://www.nexusmods.com/fallout4/mods/4046), 2K version.
- [Assault Rifle Retexture](https://www.nexusmods.com/fallout4/mods/15556), 2K version.
- [The Top-Notch Tommy Gun](https://www.nexusmods.com/fallout4/mods/24988)
- [The Lavish Laser Musket](https://www.nexusmods.com/fallout4/mods/24711)
- [The Lavish Laser Collection](https://www.nexusmods.com/fallout4/mods/25164)
- [CC's FUHD Institute Laser Weapons](https://www.nexusmods.com/fallout4/mods/37723), 2K version.
- [The Meritable Minigun](https://www.nexusmods.com/fallout4/mods/24506)
- [Missile Launcher HD](https://www.nexusmods.com/fallout4/mods/33381), 2K version.
- [The Fancy Fatman](https://www.nexusmods.com/fallout4/mods/24460)
- [Gauss Rifle UHD](https://www.nexusmods.com/fallout4/mods/41107)
- [Cryolator HD](https://www.nexusmods.com/fallout4/mods/31564)
- [Broadsider HD](https://www.nexusmods.com/fallout4/mods/31611)
- [The Delightful Deliverer](https://www.nexusmods.com/fallout4/mods/24813)
- [The Radical Ripper](https://www.nexusmods.com/fallout4/mods/24606)
- [Grognak's Axe](https://www.nexusmods.com/fallout4/mods/38644), downsized textures to 2K.
- [Kremvh's Tooth Replacer](https://www.nexusmods.com/fallout4/mods/6960), downsized textures to 2K.
- [M26 Framentation Grenade Replacer](https://www.nexusmods.com/fallout4/mods/37749), compressed and downsized textures to 1K.
- [Better Recon Scope](https://www.nexusmods.com/fallout4/mods/554)

### Creatures

- [Delightful Dead Fish](https://www.nexusmods.com/fallout4/mods/14726), Unhealthy version.
- [Fallout 3 / NV Feral Ghouls Replacer](https://www.nexusmods.com/fallout4/mods/39290), ESL-ified the plugin.
- [Retextured Super Mutants](https://www.nexusmods.com/fallout4/mods/24514)
- [CC's UHD Bloatflies](https://www.nexusmods.com/fallout4/mods/36484), 2K version.
- [CC's UHD Radscorpions](https://www.nexusmods.com/fallout4/mods/36533), 2K version.
- [CC's Enhanced Vanilla Mirelurks](https://www.nexusmods.com/fallout4/mods/36434), 2K version.
- [Detailed Deathclaws](https://www.nexusmods.com/fallout4/mods/2865), 2K version.
- [Protectron HD](https://www.nexusmods.com/fallout4/mods/15038), 2K version.
- [Assaultron HD](https://www.nexusmods.com/fallout4/mods/36045), Medium version.
- [CC's FUHD Sentry Bots](https://www.nexusmods.com/fallout4/mods/37680), 2K version.
- [CC's FUHD Fog Crawlers](https://www.nexusmods.com/fallout4/mods/36857), 2K version.
- [CC's UHD Aliens](https://www.nexusmods.com/fallout4/mods/36460), 2K version.

![separator](/Media/Separator.png)

# Body and Skin

- [Caliente's Beautiful Bodies Enhancer (CBBE)](https://www.nexusmods.com/fallout4/mods/15), Nevernude option with CBBE Reduced for dismemberment and the vanilla-shape body. Merged CBBE Reduced into the main file.
- [Skeletal Adjustments for CBBE](https://www.nexusmods.com/fallout4/mods/39006)
- [Valkyr Female Face and Body Textures](https://www.nexusmods.com/fallout4/mods/3841)
- [CBBE Ida Body Texture](https://www.nexusmods.com/fallout4/mods/10726)
- [Enhanced Vanilla Bodies](https://www.nexusmods.com/fallout4/mods/22110)

![separator](/Media/Separator.png)

# Appearance

- [Starlight Eyes](https://www.nexusmods.com/fallout4/mods/6213)
- [deLuxe Makeup](https://www.nexusmods.com/fallout4/mods/4398), both main files, merged into one mod folder.
- [Appealing Moles](https://www.nexusmods.com/fallout4/mods/3802)
- [Immersive Mouth and Teeth](https://www.nexusmods.com/fallout4/mods/903)
- [Hair Tones Redux - A Hair Color Overhaul](https://www.nexusmods.com/fallout4/mods/36637), darker brows version.
- [Pony Hairstyles by Azar](https://www.nexusmods.com/fallout4/mods/8126)
- [Lots More Female Hairstyles](https://www.nexusmods.com/fallout4/mods/10543)
- [Lots More Male Hairstyles](https://www.nexusmods.com/fallout4/mods/10695)
- [Lots More Facial Hair](https://www.nexusmods.com/fallout4/mods/10746)
  
![separator](/Media/Separator.png)

# NPC Overhauls

- [Valentine Reborn](https://www.nexusmods.com/fallout4/mods/9568), yellow eyes (like vanilla)
- [FOFW Redux](https://www.nexusmods.com/fallout4/mods/9363), Vanilla AIO.
- [Immersive Mama Murphy](https://www.nexusmods.com/fallout4/mods/25108)
- [SeriouslySarcastic's Immersive Companions](https://www.nexusmods.com/fallout4/mods/30079)
- [Seriously Sarcastic's Kellogg Face Overhaul](https://www.nexusmods.com/fallout4/mods/30703)
- [SeriouslySarcastic's Diamond City Faces Overhaul](https://www.nexusmods.com/fallout4/mods/30207), named NPCs only version.
- [SeriouslySarcastic's Minutemen Faces Overhaul](https://www.nexusmods.com/fallout4/mods/30563)
- [Varied Diamond City Guards](https://www.nexusmods.com/fallout4/mods/15419)
- [Varied Raiders](https://www.nexusmods.com/fallout4/mods/15780), both main file and Trappers expansion.
- [Varied Gunners](https://www.nexusmods.com/fallout4/mods/15784)

![separator](/Media/Separator.png)

# Gameplay

- [VAFS Redux - Bullet Time and Manual Critical](https://www.nexusmods.com/fallout4/mods/36519)
- [Pip-Boy Flashlight](https://www.nexusmods.com/fallout4/mods/10840), selected Alternate animations, the Nave Plate Pip-Boy flashlight, Maglite 300L power armor flaslight, and default light distance (no shadows) in the FOMOD.
- [Better Companions - No Conflicts](https://www.nexusmods.com/fallout4/mods/24233)
- [Everyone's Best Friend](https://www.nexusmods.com/fallout4/mods/13459)
- [EBF UFO4P Compatibility Fix](https://www.nexusmods.com/fallout4/mods/43409)
- [Automatically Lowered Weapons](https://www.nexusmods.com/fallout4/mods/20093)
- [Capital Wasteland Behemoths](https://www.nexusmods.com/fallout4/mods/41549), tagged the included mystery Misc Item as (Unique)
- [Auto Gamepad Switch](https://www.nexusmods.com/fallout4/mods/23136)

![separator](/Media/Separator.png)

# Balancing

- [Loot Logic and Reduction](https://www.nexusmods.com/fallout4/mods/21366), reverted most changed to ammunition rarity back to vanilla, ESL-ified the plugins.
- [LootBalance](https://www.nexusmods.com/fallout4/mods/41121), only to reduce the amount of Medical Items and Chems lying around in the Commonwealth. Cleaned masters and removed the core plugin as it's not needed for the combination we're using.
- [NPC Loot Drop Balance](https://www.nexusmods.com/fallout4/mods/24163/?)
- [Vendor Diversity Overhaul](https://www.nexusmods.com/fallout4/mods/24969)
- [Scavenge Station Improvements](https://www.nexusmods.com/fallout4/mods/24142), Tiered Scrap only version, ESL-ified the ESP.

![separator](/Media/Separator.png)

# Non-Player Characters

- [Better Settlers](https://www.nexusmods.com/fallout4/mods/4772/?), default FOMOD options (no changes to gender ratio, mortality, etc) plus Vanilla Assets Extended.
- [Settler Sandbox Expansion](https://www.nexusmods.com/fallout4/mods/20442), turned the ESL into and ESP-FE.
- [Stationary Scavengers](https://www.nexusmods.com/fallout4/mods/17790), ESL-ified the plugin.
- [NPCs Travel](https://www.nexusmods.com/fallout4/mods/16987/?)

![separator](/Media/Separator.png)

# Power Armor

### Gameplay

- [Power Armor Animation Changes](https://www.nexusmods.com/fallout4/mods/4408)
- [Restore Power Armor Frames](https://www.nexusmods.com/fallout4/mods/20890)
- [Take Your Cores](https://www.nexusmods.com/fallout4/mods/14773)

### Power Armor Paint Jobs

Paints and materials are now two different types of mods. Paints are purely cosmetic, cheap to apply, and all power armors have access to more paint jobs that can be applied to them.

- [Consistent Power Armor Overhaul](https://www.nexusmods.com/fallout4/mods/11234), deleted textures folder (covered by PARE).
- [Power Armor Materials and Paints (PAMAP)](https://www.nexusmods.com/fallout4/mods/4619), with DLC support but no Additional Materials.
- [Minutemen Paint Job](https://www.nexusmods.com/fallout4/mods/28029), deleted textures.bsa (covered by PARE).
- [Phoenix - Power Armor Paint Jobs](/Custom%20Files/PA%20Paint%20Jobs/README.md), custom file.

### Retextures

- [Power Armors Redone](https://www.nexusmods.com/fallout4/mods/27917), main file and X-01 helmet fix.
- [Power Armors Redone Extended](https://www.nexusmods.com/fallout4/mods/28033), CPAO and Minutemen Paint Job files.
- [Power Armor Jetpack HD](https://www.nexusmods.com/fallout4/mods/30796), 2K version.
- [Power Armor Frame UHD](https://www.nexusmods.com/fallout4/mods/39711)

![separator](/Media/Separator.png)

# Quests

- [Start Me Up](https://www.nexusmods.com/fallout4/mods/18946/?), Basic version.
- [Main Quest Choices Extended](https://www.nexusmods.com/fallout4/mods/19835)
- [Nuka World - Skip Raiding Your Own Settlements](https://www.nexusmods.com/fallout4/mods/18121), forwarded UFO4P / FDI Patch edits, ESL-ified the plugin.

![separator](/Media/Separator.png)

# Settlements

### Improvements

- [Place Everywhere](https://www.nexusmods.com/fallout4/mods/9424)
- [New Infinite Settlement Budget Plugin](https://www.nexusmods.com/fallout4/mods/16939)
- [Workshop Plus](https://www.nexusmods.com/fallout4/mods/35005)
- [BS Defence](https://www.nexusmods.com/fallout4/mods/20137), UFO4P version.
- [More Attackers - Get Off My Build Zone](https://www.nexusmods.com/fallout4/mods/27465), selected DLC and BS Defence support in the FOMOD.
- [Un-Randomize Workshop Turrets](https://www.nexusmods.com/fallout4/mods/11096), ESL-ified the plugin.
- [Red Rocket - Window Shutters](https://www.nexusmods.com/fallout4/mods/15308), Shutters Only version.
- [Corrunda's Red Rocket - Light and Curb Fix](https://www.nexusmods.com/fallout4/mods/39208)
- [Fixed and Cleaned Homeplate](https://www.nexusmods.com/fallout4/mods/38364), ESL version, turned the ESL into an ESP-FE.

### New Objects

- [Workshop Rearranged](https://www.nexusmods.com/fallout4/mods/16181), selected the following patches from the patch pack FOMOD:
  - DEF_UI + VIS: Standalone patch. Forwarded my Empty Bottle changes.
  - Vehicle Overhaul: Standalone patch.
  - Lore Friendly Posters: Replacer plugin.
  - Vault 88 More Rooms: Standalone patch.
- [The Cozy Scavver](https://www.nexusmods.com/fallout4/mods/38982), 2K main file and bed hotfix.
- [Relight (WWE)](https://www.nexusmods.com/fallout4/mods/23454)
- [Workshop Rearranged - Relight](/Custom%20Files/Custom%20Patches/README.md), custom patch.
- [Scrapping Machine](https://www.nexusmods.com/fallout4/mods/35793) allows you to quickly scrap all your junk by tossing them into a repurposed washing machine. Changed the ESL plugin to ESP-FE.
- [Vault 88 - More Vault Rooms](https://www.nexusmods.com/fallout4/mods/16896)
- [Lore-Friendly Posters](https://www.nexusmods.com/fallout4/mods/7145), deleted plugin.
- [Compact Crafting](https://www.nexusmods.com/fallout4/mods/18264) adds small versions of the crafting benches. I disabled the all-purpose version as I felt it was cheesy, plus junk scrapping can be done with Scrapping Machine. The Chem stations were renamed to Crafting Workbenches for consistency with Simple Crafting Stations. The BSA was replaced with the 2K textures version.
- [Graf's Security Fences](https://www.nexusmods.com/fallout4/mods/39252), scripted version.
- [Handmade Turrets](https://www.nexusmods.com/fallout4/mods/37877)
- [Real Troughs - New Brahmin Feeders](https://www.nexusmods.com/fallout4/mods/12945), ESL-ified the plugin.
- [Mama Murphy's Chair Redone](https://www.nexusmods.com/fallout4/mods/24819/?), restored the quest requirement and ESL-ified the plugin.

![separator](/Media/Separator.png)

# Sound Effects

- [Reverb and Ambience Overhaul](https://www.nexusmods.com/fallout4/mods/10189/?)
- [LOST Audio Tweaks](https://www.nexusmods.com/fallout4/mods/38448)
- [Project Reality Footsteps](https://www.nexusmods.com/fallout4/mods/35904), BA2 version, ESL-ified the ESP.
- [PAMS - Power Armor Movement Sounds](https://www.nexusmods.com/fallout4/mods/1544), light version plus Louder High Landing.
- [Quieter Settlements](https://www.nexusmods.com/fallout4/mods/2819), recommended AIO, ESL-ified the plugin.

![separator](/Media/Separator.png)

# Music

Fallout Suite, Bleak Beauty and Musical Lore add many, *many* new tracks of music to the original soundtrack (without replacing any of Inon Zur's score). They were chosen for their quality and consistency with the vanilla music. All three had their plugins ESL-ified, and the added music tracks are merged into the **Phoenix - Music Patch**.

- [Fallout Suite - Soundtrack Extension for Fallout 4](https://www.nexusmods.com/fallout4/mods/15870), ESL-ified the plugin and removed one ITM.
- [Bleak Beauty - A Fallout 4 Fanmade OST](https://www.nexusmods.com/fallout4/mods/9663),ESL-ified the plugin.
- [Musical Lore - Wasteland Edition](https://www.nexusmods.com/fallout4/mods/14531),ESL-ified the plugin.
- [Phoenix - Music Patch](/Custom%20Files/Custom%20Patches/README.md), custom file.
- [Elvani's Track Pack for Diamond City Radio](https://www.nexusmods.com/fallout4/mods/5467), plugin with fixed audio levels merged into the main mod folder.
- [More Where That Came From - Diamond City Radio Edition](https://www.nexusmods.com/fallout4/mods/637), forwarded new Output Model from RAO into the plugin.

![separator](/Media/Separator.png)

# Player Voice

- [No Player Comments - Chems Only](https://www.nexusmods.com/fallout4/mods/5702)

![separator](/Media/Separator.png)

# Late Loader

- [Boston FPS Fix](https://www.nexusmods.com/fallout4/mods/26286)
- [Conflict Resolution Patch](Custom%20Files/Custom%20Patches/README.md), custom file.
