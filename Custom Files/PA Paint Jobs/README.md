# Power Armor Paint Jobs

- **x** marks which PA the paint job can be applied to
- **c** marks additions by mods

### Faction

| Paint Job    | T-45 | T-51 | T-60 | X-01 |
| ------------ | ---- | ---- | ---- | ---- |
| Vault-Tec    | x    | x    | x    | x    |
| Minutemen    | x    | c    | c    | c    |
| Railroad     |      | x    |      |      |
| Institute    |      |      |      | x    |
| BOS Knight   | c    | c    | x    | c    |
| BOS Paladin  | c    | c    | x    | c    |
| BOS Sentinel | c    | c    | x    | c    |

### Misc

| Paint Job        | T-45 | T-51 | T-60 | X-01 |
| ---------------- | ---- | ---- | ---- | ---- |
| Factory          | c    | c    | c    | c    |
| Military         | x    | x    | x    | x    |
| Winterized       | x    | x    | x    | c    |
| Atom Cats        | c    | c    | x    | c    |
| Hot Rod Flames   | x    | x    | x    | x    |
| Hot Rod Shark    | x    | x    | x    | x    |
| Hot Rod Hot Pink | x    | x    | x    | x    |
| Sugar Bombs      |      | x    |      |      |
| Abraxo           |      | x    |      |      |
| Vim! Red         |      | x    |      |      |
| Vim! Green       |      | x    |      |      |

![separator](../../Media/Separator.png)

# Tweaks

### Consistent Power Armor Overhaul

- All three BOS paint jobs can now be applied to T-45, T-51, and X-01 pieces.
- The Atom Cats paint job can now be applied to T-45, T-51, and X-01 pieces.
- The Winterized Coating paint job can now be applied to X-01 pieces.
- Added Factory paint job.

I renamed the "Standard Issue Paint" for the T-51 armor to "Classic Paint".

### PAMAP - My Changes

- Forwarded CPAO changes.
- Removed the Photovoltaic section for helmets.
- Fixed some missing keywords.
- Renamed "No Paint" to "No Paint Job".
- Removed INNR changes.

### Phoenix - Power Armor Paint Jobs

- Removed additional effects (+1 Agility, etc) from all paint jobs.
- Switching paint jobs no longer yields loose mods. Only some were having loose mods anyway and it's easier to remove them altogether than add the missing ones. Plus the paint jobs are now very cheap to craft anyway.
- Applying any paint job requires 2 oil and 2 steel.
- Removed weight and value changes.
- Renamed "Winterized Coating" to "Winterized Paint".

![separator](../../Media/Separator.png)

# Missing Power Armors

So why not give the Railroad and Institute paint jobs the same treatment and allow them to be applied to all power armors?

Switching paint jobs basically means replacing the texture. Obviously we are not using Bethesda's default textures for the power armors, they are replaced by [Power Armors Redone](https://www.nexusmods.com/fallout4/mods/27917). Thankfully, the author has covered the textures for CPAO and Minutemen Paint Job in [Power Armors Redone](https://www.nexusmods.com/fallout4/mods/28033/?) so that the new paint jobs (e.g. Winterized for the X-01) appears in the same style and quality.

While I could easily add [Institute Paint for all Power Armors](https://www.nexusmods.com/fallout4/mods/4847) and [Railroad Paint for all Power Armors](https://www.nexusmods.com/fallout4/mods/3359) so that all faction paint jobs can be applied to all power armors, the textures wouldn't be consistent with the rest. Unfortunately, Power Armors Redone hasn't been updated in a long time so support for the two mentioned mods seems unlikely to be added. As it stands, I prefer inconsistency in the availability of paint jobs for power armors over inconsistent texture quality.

![separator](../../Media/Separator.png)

# Testing

### Unlock all paint jobs
```
set bospaintjobknight to 1
set bospaintjobpaladin to 1
set bospaintjobsentinel to 1
set pa_global_material_minuteman to 1
set PA_global_material_railroad to 1 
set pa_global_material_atomcat to 1
set pa_global_material_institute to 1 
player.additem 00185cd1 1
player.additem 00180a24 1
player.additem 00185cbf 1
```