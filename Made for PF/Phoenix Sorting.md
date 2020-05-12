# Phoenix Sorting

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

In the **Custom Files** mod folder, I've included the default VIS lyrConf.xml and the DEF_INV_TABS.xml files.

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
