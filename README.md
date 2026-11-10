# BindRunner

Button mapping for a Razer Naga V3 Pro mouse, a Logitech G502 Hero mouse and a Razer Tartarus keypad, without Logitech G HUB or Razer Synapse running. Each device has its own tab.

BindRunner was made for one person's setup, so each device needs a little setting up the first time. The steps are below, and the "? Help" button inside the app has them too.

> This application is built by AI. I made this for myself and I'm uploading it to GitHub for backup and to share in case anyone can get any use out of it. It's pretty specific to my setup and my needs, but if you can get any use out of it, then enjoy.
>
> Use at your own risk. I offer no warranty or guarantees for this software.

## Download

**Latest version: v1.8** (Nov 10, 2026)

- [BindRunner_v1.8_no-install.zip](https://github.com/codenomics/BindRunner/releases/download/v1.8/BindRunner_v1.8_no-install.zip) - 139 KB
- [BindRunner_v1.8_Setup.exe](https://github.com/codenomics/BindRunner/releases/download/v1.8/BindRunner_v1.8_Setup.exe) - 207 KB
- [BindRunner_v1.8_source.zip](https://github.com/codenomics/BindRunner/releases/download/v1.8/BindRunner_v1.8_source.zip) - 126 KB

What's new in v1.8:

- New: Razer Naga V3 Pro tab, with a picture of the mouse's buttons
- Naga: pick the side plate you have fitted (12, 6 or 2 buttons); each plate keeps its own settings
- Naga: change or record what every side button, wheel tilt, wheel click and top button does
- Naga: with BindRunner in front, press a mouse button to pick it on the picture
- Naga: works without Razer Synapse running, once the mouse's settings are saved to its on-board memory
- The Naga and the Tartarus work at the same time

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

## Source code

Want to see how it works, or build it yourself? Download the file ending in `_source.zip` above, extract it and double-click `Build.bat`. It only uses the C# compiler that already comes with Windows, so there is nothing to install.

## More details

```
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


RAZER NAGA V3 PRO
-----------------
The Naga tab uses the free Interception driver too (see Razer Tartarus
below for how to install it). It works with the mouse on its wireless
dongle.
1. Side buttons: leave them on their normal Synapse settings (number keys,
   or mouse buttons 4 and 5 on the 2-button plate).
2. Top buttons and wheel tilt: in Razer Synapse, set each to its own spare
   key so BindRunner can tell them apart:
      Wheel tilt left = F17, Wheel tilt right = F18,
      Left click front button = F21, Left click back button = F22,
      Ring finger button (Hypershift) = F23,
      Middle buttons: Cycle Scroll Mode = F24, AI Prompt Master = F20,
      Bottom button (Cycle Up Profile) = F19.
   Save it to the mouse's on-board memory, then fully exit Synapse.
3. In BindRunner's Naga tab, pick the side plate you have fitted (the
   mouse can't tell BindRunner which one is on). Click a button on the
   picture - or press it while BindRunner is the window in front - then
   click "Change" or "Record" to choose what it does.
   Buttons left on "Default" do what they normally do.
DPI and Smart-Reel stay in Synapse (save them to the mouse before you
exit it).


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
  Playing the PTU or Hotfix? Pick Live, PTU or Hotfix in that same menu, or
  leave it on Automatic to follow whichever game is running.
- Updates: shortly after it starts, BindRunner quietly checks GitHub for a
  newer version. If there is one, the tray menu item "Check for updates"
  changes to "Update available" and you get one small tray note - it never
  pops up a window while you're gaming. Click the menu item to update.
  Turn the startup check off in Help ("Check for updates when BindRunner
  starts").
- Buttons don't work while an "admin" window (like Task Manager) is in
  front. That's a Windows security rule.
- Settings: %APPDATA%\BindRunner. "Export" (top of the window) saves a
  backup copy or opens that folder.
- If something goes wrong, BindRunner-log.txt next to BindRunner.exe says what.
- To remove BindRunner: untick "Start with Windows", Exit from the tray,
  then delete its folder and %APPDATA%\BindRunner.
```

