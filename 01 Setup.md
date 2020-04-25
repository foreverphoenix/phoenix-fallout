
![logo](Media/Logo.png)

**TABLE OF CONTENTS**
- [Getting Started](#getting-started)
  - [Prelude](#prelude)
  - [Requirements](#requirements)
  - [Modding Folder](#modding-folder)
  - [VC Redists](#vc-redists)
- [Fallout 4](#fallout-4)
  - [Installation Directory](#installation-directory)
  - [Preferred Hard Drive](#preferred-hard-drive)
  - [Uninstalling the game](#uninstalling-the-game)
  - [INI Folder](#ini-folder)
  - [Steam Library](#steam-library)
  - [Reinstalling the game](#reinstalling-the-game)
  - [Regenerating INI Files](#regenerating-ini-files)
  - [Future Updates](#future-updates)
  - [Disable Auto Updates](#disable-auto-updates)
  - [Executables Backup](#executables-backup)
  - [Official High Resolution Texture Pack DLC](#official-high-resolution-texture-pack-dlc)
  - [Creation Club Content](#creation-club-content)
- [Wabbajack](#wabbajack)
  - [Installation](#installation)
  - [Game Folder Files](#game-folder-files)
  - [Final Step](#final-step)

![separator](Media/Separator.png)

# Getting Started

## Prelude

While Wabbajack takes care of 99% of the work, there are still some steps that need to be completed by the user. The Setup will take you through the process from start to finish and you are expected to follow it to the letter.

None of the instructions here are specific to the Phoenix: Fallout list. Any other Wabbajack list authors are welcome to copy this page, or simply link back here.

## Requirements

- A copy of Fallout 4 with all official DLC (Game of the Year Edition) on Steam.
- A [Nexus Mods](https://www.nexusmods.com/fallout4) account, preferrably with a Premium subscription.
- A hard drive (SSD preferred) with at least 100GB of free space.

## Modding Folder

- On a hard drive with plenty of free space (that is not your SSD), create a new folder called **Fallout 4 Modding**.
- Create several more folders inside:
  - `Fallout 4 Modding\Backups\Creation Club`
  - `Fallout 4 Modding\Backups\Executables 1.10.163.0`
  - `Fallout 4 Modding\Wabbajack`

## VC Redists

Mod Organizer 2 requires the latest Microsoft Visual C++ Redistributable.

- Open the [official VC Redists page](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads) and download the following file:
  - vc_redist.x64.exe
- Run downloaded executable. It will guide you through the installation process.
- You may have to restart your computer in order to finalise the installation.

![VC Redists](Media/setup/vc_redists.png)

![separator](Media/Separator.png)

# Fallout 4

## Installation Directory

In order to ensure that your Fallout 4 installation is pristine and vanilla, we are going to completely re-install Fallout 4. This is especially important if you have modded the game previously as left-over files might interfere with the Phoenix Fallout installation.

The reinstallation also serves the purpose of relocating the game files to a better directory. Using UAC protected folders (such as `C:\Program Files` or `C:\Program Files x86`) for the game or any modding tools has a high risk of causing issues down the line which is why you should avoid those folders. Most Wabbajack list authors will not provide support for people that disregard this warning and use UAC protected folders anyway.

Note that this does not include the Steam client. Most people will have it installed under `C:\Program Files x86\Steam` which is completely fine.

## Preferred Hard Drive

Fallout 4 and Mod Organizer 2 should always be installed on the same hard drive. Ideally that hard drive would be an SSD to reduce loading times and eliminate stuttering.

## Uninstalling the game

- If you have Fallout 4 currently installed, go to your Steam Library.
- Find **Fallout 4** in the list, right-click it and select **Manage** > **Uninstall**.
- Click **Uninstall** to confirm.
- Navigate to your Fallout 4 directory. This is most likely:
  - `C:\Program File x86\Steam\steamapps\common\Fallout 4`
- Delete any left-over files in this folder.

## INI Folder

 More Fallout-related files are located inside the so-called **INI Folder** which needs to be cleaned out as well. It contains your savegames as well as the game's INI files and, if you modded Fallout 4 before, F4SE plugin logs.

- Navigate to the **INI Folder:**
  - `C:\Users\{Your User Name}\Documents\My Games\Fallout4`
- If you have an ongoing vanilla playthrough, back up the **Saves** folder.
- Delete everything inside the **Fallout4** folder.

> You can simply move the **Saves** folder to `Fallout 4 Modding\Backups`.

## Steam Library

In order to prevent some confusion, I will refer to the Library in Steam as the **Game Library**. It is the second of four items in the top menu in the Steam client and contains a list of all your games.

A **Steam Library** on the other hand is a folder on your hard drive into which Steam games are installed. By default this would be `C:\Program Files x86\Steam\steamapps\common\`. Since we do not want to have files inside a UAC protected folder like Program Files x86, we should not install Fallout 4 in the default directory. A new **Steam Library** is required.

> It is important to note that Steam only allows one Steam Library per hard drive, although there is a workaround. If for instance you already have a Steam Library on your C drive, but you want to have your modding files on C as well, you need to create a second Steam Library manually following the instructions [here](https://steamcommunity.com/discussions/forum/1/1355112940663240029).

If you already have a separate Steam Library outside the UAC protected folders on the drive you want to install Fallout 4 and Mod Organizer 2 on, skip ahead to the next step.

Otherwise follow the instructions below to create a new Steam Library:

- Open Steam and go into the Settings.
- In the Downloads tab, select Steam Library Folders.
- Click Add Library Folder.
- Point it to a location somewhere outside the UAC protected folders:
  - For example: `G:\Steam Library\`.
- Close all windows when you’re done.

## Reinstalling the game

- Open Steam and go into your **Game Library**.
- Find **Fallout 4** in the list and click **Install**.
- As location, select the **Steam Library** you just created and click **Next**.

Wait for Fallout 4 to be downloaded before you proceed.

## Regenerating INI Files

After re-installing the game, it is important to launch it at least once through Steam so that the registry keys are set up. Otherwise, certain modding tools may not recognise the game. Upon launching the game, the default set of INI files will also be regenerated.

- Find **Fallout 4** in your **Games Library** and hit **Play**.
- You will be prompted with a notification that Fallout 4 is configuring your video options, click **OK**.
- Click **OK** again to the next window and hit **Exit** to close the launcher again.

![Regenerate INIs](Media/setup/regenerate_inis.png)

## Future Updates

The most important mod for any Bethesda game is the **Script Extender**, a resource that is required by many key mods. The **Fallout 4 Script Extender** (F4SE) is *version dependent*. It requires a specific version of Fallout 4. For instance, F4SE 0.6.21 *requires* Fallout 4 1.10.163, and will not work with any other version of the game.

Unfortunately any update for the Creation Club requires the game executables to be updated which breaks F4SE every time. When that happens, the Script Extender team usually updates F4Se within a few days. Any F4SE plugins will have to be updated by their respective authors as well which can take several weeks.

In order to prevent Creation Club updates from interrupting your playthrough and breaking your game, we are going to disable automatic updates in Steam. We are also going to backup the current version's executables so you can restore them at any time.

## Disable Auto Updates

- Open Steam and find **Fallout 4** in your **Game Library**.
- Right-click it and select **Properties**
- In the **Updates** tab, change **Automatic updates** to the following setting:
  - Only update the game when I launch it
- Close the **Properties** window.

![Steam Disable Auto Updates](Media/setup/steam_disable_auto_updates.png)

## Executables Backup

Although Steam will no longer update Fallout 4 automatically, I still recommend keeping backups of the two executables (**Fallout4.exe** and **Fallout4Launcher.exe**), just in case. If you accidentally updated, all you need to do to roll back is replace the executables in your **root** folder with the ones you backed up. This also comes in handy if you had to regenerate INI files or validate game files through Steam for whatever reason and were forced to update.

- Navigate to `steamapps\common\Fallout4` and copy (CTRL + C) the following files:
  - **Fallout4.exe**
  - **Fallout4Launcher.exe**
- Paste (CTRL + V) them to `Fallout 4 Modding\Backups\Executables 1.10.163.0`.

## Official High Resolution Texture Pack DLC

Bethesda published a free 55GB texture pack with upscaled 4K textures that are nowhere near worth the hard drive space, especially not when compared to higher quality mod-added textures. If you had the HD DLC installed previously, you need to disable it in Steam.

- Open **Steam** and go into your **Game Library**.
- Go to the **Fallout 4** page and click **Manage my 8 DLC**.
- Uncheck **Fallout 4 - High Resolution Texture Pack** in the list and click **Save**.

![Disable HD DLC](Media/setup/disable_hd_dlc.png)

## Creation Club Content

If you bought any "creations" from the Creation Club (or grabbed some while they were available for free), they will have been re-downloaded alongside the game. Wabbajack lists do not typically support Creation Club content so you should remove the files from your Data folder for the time being.

- Navigate to `steamapps\common\Fallout4\Data` and cut (CTRL + X) all files starting with **cc**.
- Paste (CTRL + V) all files to `Fallout 4 Modding\Backups\Creation Club`.

![separator](Media/Separator.png)

# Wabbajack

## Installation

- Download [the latest Wabbajack archive](https://github.com/wabbajack-tools/wabbajack/releases) from Github.
- Extract the downloaded archive to `Fallout 4 Modding\Wabbajack`.
- Double-click **Wabbajack.exe**.

## Game Folder Files

- Navigate to your Wabbajack installation directory and open the **Game Folder Files** folder.
- Move all files inside to `steamapps\common\Fallout4`.

## Final Step

- Go read your Wabbajack list's readme and follow any additional instructions.