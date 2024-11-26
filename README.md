# ProtonAOSP

ProtonAOSP is a minimal custom Android ROM focused on UI/UX and performance, with a touch of security and privacy. It is based on [Android Open Source Project (AOSP)](https://source.android.com/).

## Getting source code

First, make sure you have an [Android build environment](https://source.android.com/setup/build/initializing) and the [repo tool](https://source.android.com/setup/build/downloading) set up. After that, run the following commands:

```
repo init -u https://github.com/asterixiverz/ProtonAOSP -b manifest
```
```
repo sync -c --optimized-fetch -j$(nproc --all)
```
```
source build/envsetup.sh
```
```
lunch fog-userdebug
```
```
m otapackage -j$(nproc --all)
```
With Google Apps
```
export WITH_GMS=true
```
If you build with Google Apps, and want to use Pixel Launcher:
```
export PIXEL_LAUNCHER_VARIANT=ammit/horus/khonsu/tawaret (select one)
export ICONS_VARIANT=acons/cayicons/dgicons/lawnicons/rkicons/teamfilesicons (select one)
export AOSP_ENHANCER=true (Only if you want that)
```
For variants, you can choose one from the list above, the flag above is just a format.
For more information about Pixel Launcher, [read here](https://docs.google.com/document/d/1F8Ro0OyVr9CIkPQ2BOJASTlb88OpghnQJG4H0rip5yg/edit?tab=t.0#heading=h.jbs18coini1v).

This is a large download that will take approximately 100 GB of disk space, so plan accordingly.

## Building

You will need to create a device tree to build this ROM for your device. Below are some examples that have been customized to work well with ProtonAOSP:

- [Unified base tree for Pixel 5 and 4a 5G](https://github.com/ProtonAOSP/android_device_google_redbull)
- [Device-specific tree for Pixel 5](https://github.com/ProtonAOSP/android_device_google_redfin)
- [Device-specific tree for Pixel 4a 5G](https://github.com/ProtonAOSP/android_device_google_bramble)
- [Proprietary vendor blobs tree for Pixel 5 and 4a 5G](https://github.com/ProtonAOSP/android_vendor_google)

Good luck!
