# New Keywords

## Weapons

All weapons had keywords added to them so that they can finally be distinguished. They all had to be edited in order to add the new keywords to them.

Some Nuka World weapons (Thirst Zapper, Acid Soaker, Paddle Ball, Animatronic Alien Blaster) also had the WeaponTypePistol keyword added to them so that they can show up on weapon racks.

**Firearms**

- `phx_WeaponType10mm`
- `phx_WeaponTypePipe`
- `phx_WeaponTypeRevolver`
- `phx_WeaponTypeShotgun`
- `phx_WeaponTypeMusket`
- `phx_WeaponTypeHunting`
- `phx_WeaponTypeCombat`
- `phx_WeaponTypeAssault`
- `phx_WeaponTypeSubmachine`
- `phx_WeaponTypeRadium`
- `phx_WeaponTypeLeverAction`
- `phx_WeaponTypeHandmade`
- `phx_WeaponTypeLaser`
- `phx_WeaponTypeInstitute`
- `phx_WeaponTypePlasma`
- `phx_WeaponTypeGamma`
- `phx_WeaponTypeAlien`
- `phx_WeaponTypeRail`
- `phx_WeaponTypeMinigun`
- `phx_WeaponTypeMissile`
- `phx_WeaponTypeFatman`
- `phx_WeaponTypeGauss`
- `phx_WeaponTypeGatling`
- `phx_WeaponTypeTesla`
- `phx_WeaponTypeFlamer`
- `phx_WeaponTypeCryo`
- `phx_WeaponTypeBroadsider`
- `phx_WeaponTypeHarpoon`
- `phx_WeaponTypeAssaultron`
- `phx_WeaponTypeJunk`
- `phx_WeaponTypeZapper`
- `phx_WeaponTypeSyringer`
- `phx_WeaponTypeFlare`
- `phx_WeaponTypePaddle`
- `phx_WeaponTypeAcid`

**Melee**

- `phx_WeaponTypeMelee`
- `phx_WeaponTypeKnife`
- `phx_WeaponTypeBlade`
- `phx_WeaponTypeFist`
- `phx_WeaponTypeBat`
- `phx_WeaponTypeSledgehammer`
- `phx_WeaponTypeRipper`
- `phx_WeaponTypeShishkebab`

## Contraptions

The Contraptions Workshop DLC adds mortars and paint guns that can shoot fireworks and paint balls respectively. Both can be modded but keywords to distinguish the different mods are missing. So I added them.

**Mortar Ammo**

- `phx_FireworksMinutemen`
- `phx_FireworksPalmGold`
- `phx_FireworksPalmSilver`
- `phx_FireworksBlue`
- `phx_FireworksCrackle`
- `phx_FireworksGreen`
- `phx_FireworksPink`
- `phx_FireworksRed`
- `phx_FireworksYellow`
- `phx_FireworksWeatherClear`
- `phx_FireworksWeatherRadstorm`
- `phx_FireworksWeatherRain`

**Paintgun Ammo**

- `phx_PaintballBlue`
- `phx_PaintballGreen`
- `phx_PaintballRed`
- `phx_PaintballOrange`
- `phx_PaintballGlow`
- `phx_PaintballWhite`
- `phx_PaintballYellow`

## Cosmetics

While at present I am not using naming rules and keywords to sort accessories and outfits, I added new keywords to them so that they may be distinguished from one another. Only a few of them are actually used in the current setup.

**Accessories**

- `phx_AccessoryTypeHat`
- `phx_AccessoryTypeEyewear`
- `phx_AccessoryTypeMask`
- `phx_AccessoryTypeRing`
- `phx_AccessoryTypeBandolier`
- `phx_AccessoryTypeDog`

**Outfit Types**

- `phx_OutfitTypeCasual`
- `phx_OutfitTypeDapper`
- `phx_OutfitTypeDress`
- `phx_OutfitTypeRugged`
- `phx_OutfitTypeSkimpy`
- `phx_OutfitTypeBiosuit`

**Outfit Faction**

- `phx_OutfitFactionMinutemen`
- `phx_OutfitFactionVaultTec`
- `phx_OutfitFactionInstitute`
- `phx_OutfitFactionMilitary`
- `phx_OutfitFactionRaider`
- `phx_OutfitFactionBOS`
- `phx_OutfitFactionAtom`
- `phx_OutfitFactionSuperMutant`
- `phx_OutfitFactionRailroad`

## Armor Slots

In vanilla, armor slots do not separate keywords for some reason. I created separate keywords and added them to all relevant armor records.

- `phx_ArmorSlotChest`
- `phx_ArmorSlotArmL`
- `phx_ArmorSlotArmR`
- `phx_ArmorSlotLegL`
- `phx_ArmorSlotLegR`
- `phx_ArmorSlotHelmet`

## Additional Armor Types

Some armor types do not have separate keywords which makes it impossible to give them appropriate names through INNRs. Therefore some more specific keywords were added.

- `phx_ArmorTypeSecurity`
- `phx_ArmorTypeDCGuard`
- `phx_ArmorTypeRobot`
- `phx_ArmorTypeDiscipleMetal`
- `phx_ArmorTypeDiscipleStrapped`
- `phx_ArmorTypeDiscipleSpiked`
- `phx_ArmorTypeDiscipleWrapped`
- `phx_ArmorTypePackBone`
- `phx_ArmorTypePackStuffed`
- `phx_ArmorTypeOperatorHeavy`

## Power Armor

While the vanilla power armors (Raider, T-45, T-51, T-60, and X-01) have proper keywords to distinguish them, the DLC-added sets do not. This affects the Tesla T-60 added by Automatron and the Overboss set added by Nuka World. I also edited the records for the Tesla and Overboss pieces to add the new keywords.

- `phx_TeslaPA`
- `phx_OverbossPA`

## Power Armor Paint Jobs

The four power armor paint jobs added by the Contraptions Workshop (Abraxo, Sugar Boms) and Far Harbor (Vim! Red, Vim! Green) did not have keywords in vanilla which makes it impossible to distinguish them for sorting plugins. While at present I do not add unique names for paint jobs, I nonetheless added these keywords. I also edited the relevant OMOD records to add the keywords when the paint jobs are applied.

- `phx_HasMaterialAbraxo`
- `phx_HasMaterialSugarbombs`
- `phx_HasMaterialVimGreen`
- `phx_HasMaterialVimRed`

![separator](../../Media/Separator.png)

# Credits

None of this would have been possible without AWKCR which in many cases showed me where keywords were missing and how to implement them.