# BindRunner

> This application is built by AI. I made this for myself and I'm uploading it to GitHub for backup and to share in case anyone can get any use out of it. It's pretty specific to my setup and my needs, but if you can get any use out of it, then enjoy.
>
> Use at your own risk. I offer no warranty or guarantees for this software.

## Download

**Latest version: v1.3** (Oct 3, 2026)

- [BindRunner_v1.3_no-install.zip](https://github.com/codenomics/BindRunner/releases/download/v1.3/BindRunner_v1.3_no-install.zip) - 126 KB
- [BindRunner_v1.3_Setup.exe](https://github.com/codenomics/BindRunner/releases/download/v1.3/BindRunner_v1.3_Setup.exe) - 195 KB

What's new in v1.3:

No notes for this version.

Older versions are on the [Releases page](https://github.com/codenomics/BindRunner/releases).

## Getting started

### Installer (recommended)

1. Download the file ending in `_Setup.exe` above.
2. Double-click it and click Install. It installs just for you - no admin password needed - and adds Start menu and Desktop shortcuts.
3. To remove it later: Windows Settings > Apps, find BindRunner and click Uninstall.

### No install (portable zip)

1. Download the file ending in `_no-install.zip` above.
2. Right-click it > Extract All, and pick a folder. Don't run it from inside the zip.
3. Open the folder and double-click the app's .exe. Nothing is installed; delete the folder to remove it.

Windows says "Windows protected your PC"? Click More info > Run anyway. It shows that for apps without a paid signing certificate.

## More details

```
BINDRUNNER
==========

Button mapping for a Logitech G502 Hero mouse and a Razer Tartarus keypad,
without Logitech G HUB or Razer Synapse running. Each device has its own tab.

BindRunner was made for one person's setup, so each device needs a little
setting up the first time. The steps are below, and the "? Help" button
inside the app has them too.


GETTING STARTED
---------------
Pick one. Both give you the same app.

OPTION 1 - INSTALLER (recommended)
  Download the file ending in _Setup.exe, double-click it and click Install.
  It installs just for you (no admin password) and adds Start menu and
  Desktop shortcuts. Needs Windows 10 or 11 (64-bit).
  To remove it later: Windows Settings > Apps > BindRunner > Uninstall.

OPTION 2 - NO INSTALL (zip)
  1. Download the file ending in _no-install.zip. Right-click it -> Extract
  All... and put the BindRunner folder somewhere it can stay (for example
  Documents). Don't run it from inside the zip. Keep interception.dll next
  to BindRunner.exe.
  2. Double-click BindRunner.exe. Nothing is installed; to remove it, delete
  the folder.

EITHER WAY
  Tick "Start with Windows" (Tartarus tab, or the tray menu) so it's always
  running. Closing the window keeps it running in the tray (near the clock);
  right-click the tray icon -> Exit to fully quit.

"Windows protected your PC"? Click "More info" -> "Run anyway".
Windows shows that for apps downloaded from the internet that aren't
signed with a paid certificate.


LOGITECH G502 HERO
------------------
BindRunner listens for hidden keys (F13-F20) that the mouse sends. Set them
once with Logitech G HUB, saved to the mouse's on-board memory:
   Thumb front = F13, Thumb back = F14, Sniper = F15,
   Beside left click front = F16, back = F17,
   Wheel tilt left = F18, Wheel tilt right = F19, Behind the wheel = F20.
Save it to the mouse, then close or uninstall G HUB.
In BindRunner's G502 tab, click "Change" or "Record" next to a button to
choose what it does.


RAZER TARTARUS
--------------
The Tartarus tab needs the free Interception driver, which lets BindRunner
tell the Tartarus apart from your normal keyboard.
1. Download Interception: https://github.com/oblitum/Interception/releases
   Unzip it, open Command Prompt as administrator, go into its
   "command line installer" folder and run:
      install-interception.exe /install
   Then restart the PC.
2. In Razer Synapse, give EVERY Tartarus key its own ordinary key in the
   keymap saved on the Tartarus (no two the same, none on "Disable" -
   numpad keys work well). Then fully exit Synapse.
3. In BindRunner's Tartarus tab: click "Find my Tartarus", then
   "Re-teach keys" and press each key as it glows pink.
4. Click a key on the picture (or press it) to choose what it sends, its
   color, and which keymap it belongs to.

Optional - stop games also seeing the thumbstick as a game controller:
use the free Zadig tool (https://zadig.akeo.ie/). Options -> tick
"List All Devices", pick the Tartarus entry whose driver shows xusb22,
set the target driver to WinUSB and click "Replace Driver", then unplug
and replug the Tartarus. "? Help" in the app explains how to undo it.

Heads-up: Interception is a low-level input driver. Some online games'
anti-cheat systems may not like it - check before using it with those.


GOOD TO KNOW
------------
- Profiles switch by themselves when a game linked to a profile is the
  window in front. Each profile can have several keymaps.
- Star Citizen: BindRunner can switch your Star Citizen profile to its
  "Flight" keymap when you sit at a ship's helm and to "Walk" when you get
  up (Profile menu -> "Star Citizen: sit / stand switching").
- Buttons don't work while an "admin" window (like Task Manager) is in
  front. That's a Windows security rule.
- Settings: %APPDATA%\BindRunner. "Export" (top of the window) saves a
  backup copy or opens that folder.
- If something goes wrong, BindRunner-log.txt next to BindRunner.exe says what.
- To remove BindRunner: untick "Start with Windows", Exit from the tray,
  then delete its folder and %APPDATA%\BindRunner.
```

