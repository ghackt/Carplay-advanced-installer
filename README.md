# Carplay-Advanced-Installer. Identical to NBT EVO APK Originally Developed by @BimmerTuner. But for Carplay Capabilities for ID5 and ID6

<img width="5712" height="4284" alt="IMG_4478" src="https://github.com/user-attachments/assets/86b581c7-0184-4280-9d90-d2d12e09d181" />
<img width="4284" height="5712" alt="IMG_4483" src="https://github.com/user-attachments/assets/29c190d7-90f9-4dd4-9872-16484c7fd069" />
<img width="4284" height="5712" alt="IMG_4485" src="https://github.com/user-attachments/assets/6e45b9f1-9bd6-442a-8fca-8f155e095d26" />
<img width="4284" height="5712" alt="IMG_4484" src="https://github.com/user-attachments/assets/cf7ebf08-760f-4d72-98b5-b1a4aafd8690" />
<img width="4284" height="5712" alt="IMG_4487" src="https://github.com/user-attachments/assets/29448410-a0fe-45c1-a91d-b6e6a4bd8a68" />


An easy AIO installer for those who have issues using SSH and installing things manually like I do sometimes.

## Requirements

ENET with USB-C Adapter

Android Device

When connecting with Ethernet Tethering you will need a WiFi hot spot of some sort to pull request the files from repository.

## What it does

This has been rebuilt off of BimmerTuner's APK file but to allow install for CarPlay Custom Nav Menu and custom HUD arrows (if Cluster and HU support it or will use native supported).

I do not take credit for this software: it is beyond my level of expertise and it was rebuilt using AI.
**Please report any bugs if you come across them** (open an Issue).

Android app that connects to a BMW NBT Evo head unit, unlocks SSH, backs up the head unit, installs
[nbtevo-carplay-advanced](https://github.com/st1ng/nbtevo-carplay-advanced) (v1.1.0 and beyond bundled in the app) and can uninstall/restore.

Also has "Connect to your BMW" and "Restart head unit". The release list is read live from the st1ng repo (offline it falls back to the bundled list).

Apple CarPlay add-ons for the BMW / MINI NBT Evo head unit (iDrive 5 and iDrive 6): a CarPlay Advanced Settings menu in Media/Radio, and the iPhone's turn-by-turn directions in the cluster and the head-up display.

It unlocks SSH on the head unit the same way the original app did.
It checks the head unit’s software and saves a backup to your phone.
It allows for easy updates as developer continues to add new things and fixes bugs.
It uploads the installer script and the plugin files, and checks each upload by comparing its SHA-256 hash.
It runs carplay-advanced.sh install on the head unit, in full mode for known software versions and in HUD-only mode for any other.
It copies the head unit’s backup folder back to your phone.

The app launches the project’s own installer script, not a reimplementation, and I checked the command line against that script. The two software versions the script knows about are ID5 1803-510-1749MA Build 71 and ID5 1703-490-1650ZD Build 139. Anything else gets the HUD-only install.

Things that could still go wrong on a real car:

A mistake in the new smali I wrote for the upload, install or backup steps, which I could only read through.
The SSH unlock failing on your head unit.
The install script taking longer than the app’s 60-second wait for a command to finish.

The install command targets ID5 (--kind id5), so I haven’t checked ID6 units. Try it with the car connected and send me whatever the app’s log shows. If it stops partway, I can fix it from that.

It is an HMI plugin plus a few small libraries that hook into the head unit's own processes at run time. Apart from one line added to the boot script, no system file is replaced or patched on disk, and one installer script puts it on (and takes it off) over the car's ENET connection, with backups of everything it touches.

Disclaimer. This project is for educational purposes only. Run it only on a car you own, at your own risk: you alone are responsible for whatever it does to your head unit, your car and its warranty, and for using it in line with the law where you drive. Never operate it while driving. It comes with no warranty of any kind.

> tested on a real head unit. J29 / A90 Supra but use at your own risk; back up first.

## Download

https://github.com/ghackt/Carplay-advanced-installer/releases/

See [`release/`](release/): `CarPlay_Advanced_Installer_1.1.0.apk`, the payload zips and `SHA256SUMS.txt`.

## Credits (all original work belongs to them)
- **@st1ng** - author of [nbtevo-carplay-advanced](https://github.com/st1ng/nbtevo-carplay-advanced), the payload this app installs.
- **@Sq00ky** - [Supra-iDrive6-Android-Auto](https://github.com/Sq00ky/Supra-iDrive6-Android-Auto), where the original NBTEvo Release Manager app comes from.
- **@BimmerTuner** - the APK this was rebuilt from was shared via their repo [BimmerTuner/Supra-iDrive6-Android-Auto](https://github.com/BimmerTuner/Supra-iDrive6-Android-Auto). I have not confirmed they wrote any of it.

 ## I don't Charge for Anything. If you paid for this or someone is stealing this work please report it.
 - If you feel generous I like a lot of Starbucks coffee.. (: <link>https://www.paypal.me/JamieBland371</link>

## License
The bundled nbtevo-carplay-advanced files are under the **PolyForm Noncommercial 1.0.0** licence: personal/hobby use only, no selling or commercial use. Copies of its LICENSE and NOTICE are in [`licenses/`](licenses/).
I have not verified the licence of the original app; rights in it remain with its authors.
