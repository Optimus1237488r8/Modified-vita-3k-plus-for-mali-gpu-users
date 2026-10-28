# Vita3K-Plus with Custom GPU Driver option for Mali (unofficial)

Vita3K-Plus hides the **Custom GPU Driver** option on Mali GPUs. This is a
modified build that shows it, so Mali users can import a custom driver.

**No game files, firmware, or dumps are included or needed here.**

Not affiliated with Vita3K or Vita3K-Plus. All credit for the emulator goes
to its developers:
- Vita3K-Plus: https://github.com/nckstwrt/Vita3K-Plus
- Vita3K (original, GPLv2): https://github.com/Vita3K/Vita3K

Credit for custom drivers goes to their authors. I did not make any of them.

## Download
Go to the **Releases** page of this repo and download the APK.

Patched from: **Vita3K-Plus v1.3.3**

## Install
1. **Back up** your Vita3K data first (games, saves, config). Uninstalling
   the app can delete its data.
2. Uninstall the original Vita3K-Plus. This build uses a different signature,
   so it cannot be installed over the original.
3. Install the APK from this repo. Android may ask you to allow installing
   from unknown sources.
4. Open **Settings**. The **Custom GPU Driver** section now shows
   **Install Driver**.
5. Import your Mali driver and select it. The app should show
   "The selected custom driver is loaded and active."

## Drivers
- Not every Mali driver works. Experimental PanVK builds are made for
  specific chips. Check the driver's `meta.json` for the supported GPUs and
  the minimum Android version.
- If a driver crashes the app, select **Default** again, or remove the driver.

## Tested on
- Phone / GPU: <<Samsung Galaxy A22 5g, Mali GPU>>
- Android: <<13>>
- Driver: <<panvk_faux123_v1.0.2.adpkg, FristOneRR>>

Results may differ on other phones, app versions, or drivers.

## What was changed
One thing only: the app asks its native code whether to show the driver
options, and on Mali that check says no. In this build the result is forced
to "yes", so the option shows. The rest of the driver loading is the original
app's code. No game content was added or removed.

## Warnings
- This is unofficial and was tested only on the setup listed above.
- The APK is signed with a public test key, not a private release key.
- Back up your data before installing.

## License
Vita3K is licensed under GPLv2. This modified build keeps that license. The
original source is at the links above, and the change is described in
"What was changed".
