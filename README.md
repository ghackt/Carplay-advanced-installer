# Carplay-advanced-installer

An easy installer for those who have issues using SSH and installing things manually.

This has been rebuilt off of BimmerTuner's APK file but to allow install for CarPlay nav.
I do not take credit for this software: it is beyond my level of expertise and it was rebuilt using AI.
**Please report any bugs if you come across them** (open an Issue).

## What it does
Android app that connects to a BMW NBT Evo head unit, unlocks SSH, backs up the head unit, installs
[nbtevo-carplay-advanced](https://github.com/st1ng/nbtevo-carplay-advanced) (v1.1.0 or v1.0.0, bundled in the app), and can uninstall/restore.
Also has "Connect to your BMW" and "Restart head unit". The release list is read live from the st1ng repo (offline it falls back to the bundled list).

Apple CarPlay add-ons for the BMW / MINI NBT Evo head unit (iDrive 5 and iDrive 6): a CarPlay Advanced Settings menu in Media/Radio, and the iPhone's turn-by-turn directions in the cluster and the head-up display.

It is an HMI plugin plus a few small libraries that hook into the head unit's own processes at run time. Apart from one line added to the boot script, no system file is replaced or patched on disk, and one installer script puts it on (and takes it off) over the car's ENET connection, with backups of everything it touches.

Disclaimer. This project is for educational purposes only. Run it only on a car you own, at your own risk: you alone are responsible for whatever it does to your head unit, your car and its warranty, and for using it in line with the law where you drive. Never operate it while driving. It comes with no warranty of any kind.

> Untested on a real head unit. Use at your own risk; back up first.

## Download
See [`release/`](release/): `CarPlay_Advanced_Installer_1.1.0.apk`, the payload zips and `SHA256SUMS.txt`.

## Credits (all original work belongs to them)
- **@st1ng** - author of [nbtevo-carplay-advanced](https://github.com/st1ng/nbtevo-carplay-advanced), the payload this app installs.
- **@Sq00ky** - [Supra-iDrive6-Android-Auto](https://github.com/Sq00ky/Supra-iDrive6-Android-Auto), where the original NBTEvo Release Manager app comes from.
- **@BimmerTuner** - the APK this was rebuilt from was shared via their repo [BimmerTuner/Supra-iDrive6-Android-Auto](https://github.com/BimmerTuner/Supra-iDrive6-Android-Auto). I have not confirmed they wrote any of it.

## Licence
The bundled nbtevo-carplay-advanced files are under the **PolyForm Noncommercial 1.0.0** licence: personal/hobby use only, no selling or commercial use. Copies of its LICENSE and NOTICE are in [`licenses/`](licenses/).
I have not verified the licence of the original app; rights in it remain with its authors.
