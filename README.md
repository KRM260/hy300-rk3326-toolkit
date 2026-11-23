# HY300 PROJECTOR TOOLKIT - Rockchip RK3326 version

A one-click upgrade for the cheap "HY300" mini projector, ONLY the version
with the Rockchip RK3326 chip and Android 12. Made by KRM Studio.

## What it does
- Backs up your projector's whole system to your PC first, and checks
  every piece of the copy. Nothing changes until the backup is verified.
- Switches off the factory junk and the risky parts: test apps, a hidden
  IPTV app pretending to be part of Android, a Chinese voice assistant,
  the factory "updater" that can install apps silently, and a background
  app that reports your serial number to an advertising server.
- Replaces the factory home screen with Projectivy Launcher.
- Speeds things up: faster menus, main apps pre-built so they open quicker.
- Brighter picture: the factory set brightness to 30/100 and dimmed the
  colours. This sets brightness 50, neutral white, gamma 1.6.
- New startup: a red loading spinner while the picture is still upside
  down, then a spray-paint graffiti intro.
- Everything can be undone from the menu.

Not touched: Google Play, YouTube, Netflix, screen mirroring, keystone, focus.


## Is my projector the right one?
Many different projectors are sold as "HY300". This is ONLY for the Rockchip
one. To check:
  1. Install "CPU-Z" on the projector (copy the .apk from cpuid.com onto a
     USB stick and open it in the projector's File Manager).
  2. On the SoC tab, "Model" must say RK3326.
     (CPU-Z may show "RK3066" at the top. That is a known bug. The Model
     line is the real one.)
If it says Allwinner H713 or H726, do NOT use this. Look for the custom
firmware on androidpctv.com instead.
The toolkit checks the model itself as well, and stops without changing
anything if the projector is a different one.


## Step by step
1. Unzip this toolkit somewhere easy, for example your Desktop.

2. Get ADB (free from Google):
   - Search "Android SDK Platform-Tools", download the Windows version.
   - Unzip it and put the "platform-tools" folder INSIDE this toolkit folder.

3. Get Projectivy Launcher (free):
   - Go to apkmirror.com and search "Projectivy Launcher".
   - Download the variant marked "armeabi-v7a" (Android 12L+). It is a
     ".apkm" bundle file. That is fine.
   - Put the file in the "apps" folder of this toolkit. Do not rename it.

4. Find your projector's IP address:
   On the projector: Settings - Wi-Fi - click your network. It looks like
   192.168.1.45. Your PC and projector must be on the same Wi-Fi.

5. Double-click START.bat, type the IP address, then choose 1 (Full upgrade).
   - The first time, the projector may show "Allow USB debugging?".
     Tick "Always allow" and press OK with the remote.
   - The backup takes 10-15 minutes. Then the rest takes about 10 minutes,
     and the projector restarts 3 times. Leave it alone until the window
     says ALL DONE.

6. Your backup is in a folder called BACKUP_<number> inside the toolkit.
   Copy it somewhere safe (Google Drive, USB stick). It is your only way
   back to factory state.


## If something goes wrong
- Wrong picture or startup you don't like: START.bat - choose 3 (Undo).
- Projector seems stuck on the startup animation: wait two minutes (the
  first start after changes is slow), then run START.bat - 3 (Undo).
- "Could not reach the projector": check the IP (menu option 5) and that
  both devices are on the same Wi-Fi.
- Undo keeps Projectivy as the home screen on purpose: the factory home
  screen can get stuck in a crash loop once it has been switched off.


## Good to know
- Startup takes about a minute on this chip. That is normal. The projector
  keeps the animation on screen until the home screen has fully loaded.
- A factory reset removes most of the upgrade. Just run the toolkit again.
- The factory updater stays off, so the maker can no longer push updates.
  That is on purpose, because it was the back door.
- Games: install F-Droid (f-droid.org), then Lemuroid from it. This chip
  handles NES, SNES, Game Boy, GBA, Mega Drive, arcade and PS1 well.
  N64 is hit or miss. PSP and newer will not run well.
  Only play games you own or that are free/homebrew (itch.io, pdroms.de).
- The brighter-picture idea comes from a Habr.com article about the same
  Rockchip HY300.


## Use at your own risk
This changes system settings on your projector. It was tested on one
Rockchip HY300 (build rk3326_sgo, July 2025). It makes a verified backup
first and has an undo, but there is no warranty.


## Download

Get the latest `HY300-RK3326-Toolkit.zip` from the **Releases** section on the right of this page.
