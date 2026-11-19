# Carplay-Advanced-Installer. Identical to NBT EVO APK Originally Developed by @BimmerTuner. Fully Redesigned from bits of code by @ghackt with many additional features But for Carplay Gauge / HUD Navigation Capabilities side for ID5 and ID6. This is not Android Auto Installer. This can work along side Android Auto tweak.

First of all thank you all for giving me a shot and my files. If you encounter any issues PLEASE OPEN A TICKET https://github.com/ghackt/Carplay-advanced-installer/issues/new

<img width="1206" height="880" alt="IMG_4488" src="https://github.com/user-attachments/assets/63d0d81f-be19-4f0c-a967-fed3e2ceee84" />
<img width="5712" height="4284" alt="IMG_4478" src="https://github.com/user-attachments/assets/86b581c7-0184-4280-9d90-d2d12e09d181" />
<img width="4284" height="5712" alt="IMG_4483" src="https://github.com/user-attachments/assets/29c190d7-90f9-4dd4-9872-16484c7fd069" />
<img width="4284" height="5712" alt="IMG_4485" src="https://github.com/user-attachments/assets/6e45b9f1-9bd6-442a-8fca-8f155e095d26" />
<img width="4284" height="5712" alt="IMG_4484" src="https://github.com/user-attachments/assets/cf7ebf08-760f-4d72-98b5-b1a4aafd8690" />
<img width="4284" height="5712" alt="IMG_4487" src="https://github.com/user-attachments/assets/29448410-a0fe-45c1-a91d-b6e6a4bd8a68" />


An easy AIO installer for those who have issues using SSH and installing things manually like I do sometimes.

## Features Wired and wireless 

Separate connection modes for Wired ENET and Wireless Adapter (BM3 & MHD).

Wireless adapter support remains experimental until further releases are made and requires compatible hardware.

## Requirements

ENET with USB-C Adapter
<img width="702" height="621" alt="Screenshot 2026-11-17 015742" src="https://github.com/user-attachments/assets/ef89e84e-a7f4-4b11-8a95-e51c3a39af1f" />

BM3 or MHD dongles
<img width="862" height="582" alt="Screenshot 2026-11-17 015927" src="https://github.com/user-attachments/assets/9119b5af-80d3-45f9-9450-9e264324ec56" />

A Reliable Android Device with storage space

When connecting with Ethernet Tethering you will need a WiFi hot spot of some sort to pull request the files from repository.

Ethernet tethering can be enabled in your “hotspot settings” for most Android devices

## Please restart Head Unit from the app after Flash is complete.

## NOTE

IF SSH IN FAILS. RESTART HU WITHIN THE APP AND ATTEMPT TO RECONNECT WHILE IT's RESTARTING.

## What is this?

This has been rebuilt off of BimmerTuner's APK file but to allow install for CarPlay Custom Nav Menu and custom HUD arrows (if Cluster and HU support it or will use native supported).

Android app that connects to a BMW NBT Evo head unit, unlocks SSH, backs up the head unit, installs
[nbtevo-carplay-advanced](https://github.com/st1ng/nbtevo-carplay-advanced) (v1.1.0 and beyond bundled in the app) and can uninstall/restore.

Also has "Connect to your BMW" and "Restart head unit". The release list is read live from the st1ng repo (offline it falls back to the bundled list).

Apple CarPlay add-ons for the BMW / MINI NBT Evo head unit (iDrive 5 and iDrive 6): a CarPlay Advanced Settings menu in Media/Radio, and the iPhone's turn-by-turn directions in the cluster and the head-up display.

## What does the app do?

-It has .apk Auto Update pulled from my repository if an update is avaliable.

-Backup head unit directory stored elsewhere so when you update the app it no longer deletes your backup.

-.APK releases not longer allow to be accidently installed though the app and is blocked. Only .zip files are recognized to be installed on the app.

-Buttons now show check marks so you know what you are pressing.

-It unlocks SSH on the head unit the same way the original app did.

-It checks the head unit’s software and saves a backup to your phone.

-It allows for easy updates as developer continues to add new things and fixes bugs.

-It uploads the installer script and the plugin files, and checks each upload by comparing its SHA-256 hash.

-It runs carplay-advanced.sh install on the head unit, in full mode for known software versions and in HUD-only mode for any other.

-It copies the head unit’s backup folder back to your phone.

The app launches the project’s own installer script, not a reimplementation, and I checked the command line against that script. The two software versions the script knows about are ID5 1803-510-1749MA Build 71 and ID5 1703-490-1650ZD Build 139. Anything else gets the HUD-only install.

The install command targets ID5 (--kind id5), so I haven’t checked ID6 units. Try it with the car connected and send me whatever the app’s log shows. If it stops partway, I can fix it from that.

It is an HMI plugin plus a few small libraries that hook into the head unit's own processes at run time. Apart from one line added to the boot script, no system file is replaced or patched on disk, and one installer script puts it on (and takes it off) over the car's ENET connection, with backups of everything it touches.

## Things that could go wrong on a car

A mistake in the new smali I wrote for the upload, install or backup steps, which I could only read through.
The SSH unlock failing on your head unit.
The install script taking longer than 5 mins as decompression of install is around 60MB flash.
You are testing on a non iDrive 5 or iDrive 6 Headunit.
Your Head Unit Base Firmware needs support.
a 3rd party used a tool that rewrote and locked the file system for some other modifications to the Head Unit.

## Known issues…
Waze does not natively fully support cluster and heads-up Display.
regarding Waze: https://waze.uservoice.com/forums/59223-waze-suggestion-box/suggestions/50043126-prioritize-full-carplay-integration-hud-instrum
**You may still use Apple Maps and Google Maps with no issues**

## How do I install this?
Step 1 — Download the app
1.  On your Android phone, go to the Releases page.
2.  Download CarPlay_Advanced_Installer_1.1.0.apk (or the newest version listed).
3.  Optional but smart: compare the file's hash against SHA256SUMS.txt from the same release.
The tweak payload (v1.1.0 and later) is bundled inside the app, so you don't need to download the payload zips separately unless you want a specific release.
Step 2 — Install the APK
1.  Open the downloaded APK on your phone.
2.  If Android blocks it, allow Install unknown apps for your browser or file manager when prompted.
3.  Finish the install and open CarPlay Advanced Installer.
The app updates itself from the author's repository when a new version is available, and it keeps your head-unit backup in a separate location so updating the app doesn't delete it.
Step 3 — Set up the connection
Wired (ENET) — recommended
1.  Plug the ENET cable into the car's OBD port and connect it to your phone with the USB-C adapter.
2.  On the phone, turn on Ethernet tethering — on most Android phones it's in the Hotspot / tethering settings.
3.  Connect the phone to a Wi-Fi hotspot so it still has internet access.
4.  In the app, choose the Wired ENET connection mode.
Wireless (BM3 / MHD) — experimental
1.  Plug your BM3 or MHD dongle into the car.
2.  In the app, choose the Wireless Adapter connection mode.
Tip (general advice, not from the README): keep the ignition on for the whole process and consider a battery maintainer, so the car doesn't shut down mid-install.
Step 4 — Connect and unlock SSH
1.  Tap Connect to your BMW.
2.  Let the app unlock SSH on the head unit.
3.  If SSH fails: tap Restart head unit in the app, then try to reconnect while it is restarting.
Buttons show a check mark once that step has been done, so you can track where you are.
Step 5 — Back up the head unit
Run the backup before installing anything. The app checks the head unit's software version and saves a backup to your phone. Don't skip this — it's what lets you restore later.
Step 6 — Install the tweak
1.  Pick the release to install. The list is read live from @st1ng's repository; offline, the app uses its bundled list. Only .zip payloads can be installed (APK files are blocked on purpose).
2.  Start the install. The app uploads the installer script and plugin files, verifies each upload by SHA-256, then runs carplay-advanced.sh install on the head unit — full mode for the known ID5 versions, HUD-only for anything else.
3.  Wait. It can take over 5 minutes. Don't disconnect or turn the car off.
4.  When it finishes, the app copies the head unit's backup folder back to your phone.
Step 7 — Restart the head unit
After the flash completes, tap Restart head unit in the app. The new menu appears after the restart.
Step 8 — Find and set up the new settings
Go to Media/Radio → CarPlay Advanced Settings.
iDrive 5 menu
• Full-screen CarPlay
• CarPlay directions in HUD
• HUD effects: Fill toward the turn / Blink near the turn / Effect colour (Orange, Grey, White)
• iDrive control: Enable knob tilts
• Touchpad: Enable touchpad / Tap touchpad as click / Touchpad sensitivity (Low, Medium, High) / Two fingers tap to back
• Enable rotation as zoom
• Restart to apply
iDrive 6 menu (HUD-only)
• CarPlay directions in HUD
• HUD effects: Fill toward the turn / Blink near the turn / Effect colour (Orange, Grey, White)
Use Restart to apply after changing settings.
Uninstalling or restoring
The same app can uninstall the tweak and restore your backup. Connect the same way (Steps 3–4) and use the uninstall/restore option. The tweak only adds one line to the boot script and doesn't replace system files on disk, so removal is clean.
Troubleshooting & known issues
• SSH won't connect: restart the head unit from the app and reconnect while it reboots.
• Install seems slow: over 5 minutes is normal; give it time.
• Install stops partway (especially on ID6): copy the app's log and open an issue at github.com/ghackt/Carplay-advanced-installer/issues/new.
• Waze: doesn't fully support cluster/HUD directions. Apple Maps and Google Maps work fine.
• Android Auto tweak also installed: reported to work, but don't use CarPlay and Android Auto at the same time; no guarantees.
• Likely to fail if: your head unit isn't iDrive 5/6, its base firmware isn't supported, or a previous third-party tool rewrote and locked the file system.


## I have tested this also while having Android Auto Install. I did not have any issues or complications as HUD nav is taken priority by whether you are using Carplay or Android Auto would not recommend trying to use both at the same time. Also cannot guarantee you will not run into issues using both installs.

Disclaimer. This project is for educational purposes only. Run it only on a car you own, at your own risk: you alone are responsible for whatever it does to your head unit, your car and its warranty, and for using it in line with the law where you drive. Never operate it while driving. It comes with no warranty of any kind.

> ## Tested on a real head unit. J29 / A90 Supra but use at your own risk; Always back up first.

## Credits (all original work belongs to them)
## NBT-AAD by nanaisu: Android Auto for the NBT Evo. This project stands on their reverse engineering: the HMI plugin interface, the MOST/DSI client and the HUD terminal layout, and the Ethernet KOMBI route-guidance stack, which src/kombi.h ports (with their captured route graph, src/kombitemplate.h, unchanged). Thank you.
## NBT-AAD USB Tools by Yalozo: the installer's pre-installation checks follow theirs.
## Mapbox Navigation SDK for iOS v0.40.0: the maneuver and lane drawings (ISC licence), turned into HUD polygons by tools/hud_glyphs.py.
## ftojke/BMW-iDrive6-CarPlay-HUD, JayJay3071/nbt-android-auto, luka-dev/mib2q-carplay-rgi and f-io/LIVI: findings and formats that helped (AGENTS.md, References).
- **@st1ng** - author of [nbtevo-carplay-advanced](https://github.com/st1ng/nbtevo-carplay-advanced), the payload this app installs.
- **@Sq00ky** - [Supra-iDrive6-Android-Auto](https://github.com/Sq00ky/Supra-iDrive6-Android-Auto), where the original NBTEvo Release Manager app comes from.
- **@BimmerTuner** - the APK this was rebuilt from was shared via their repo [BimmerTuner/Supra-iDrive6-Android-Auto](https://github.com/BimmerTuner/Supra-iDrive6-Android-Auto). I have not confirmed they wrote any of it.
- **@Ghackt** compiling all sources into a tested and working android application.

 ## I don't charge for Anything. If you paid for this from someone or someone is stealing this work, please report it to us. https://github.com/ghackt/Carplay-advanced-installer/issues/new

- **@st1ng** 
- **@Sq00ky** 
- **@BimmerTuner**

 ## Donations or Coffee Giving

 - Tired of all these companies charging outrageous prices for other people’s work. Also tired of these Chinese companies forcing people to buy MMI boxes and taking advantage of us all.
   
 - If you are feeling generous I like a lot of Starbucks coffee.. (:
 
 <link>https://www.paypal.me/JamieBland371</link>///////<link>https://www.venmo.com/ItsJamesB</link>/////or @ItsJamesB in the venmo app search.

 

 ## Download

https://github.com/ghackt/Carplay-advanced-installer/releases/

See [`release/`](release/): `CarPlay_Advanced_Installer_1.1.0.apk`, the payload zips and `SHA256SUMS.txt`.

## Additional Information

I do not take full credit for this software: it is beyond my level of expertise, and it was rebuilt using some of my knowledge and some AI for stability tweaks.
**Please report any bugs if you come across them** (open an Issue).

## License

The bundled nbtevo-carplay-advanced files are under the **PolyForm Noncommercial 1.0.0** license: personal/hobby use only, no selling or commercial use. Copies of its LICENSE and NOTICE are in [`licenses/`](licenses/).
I have not verified the license of the original app; rights in it remain with its authors.
