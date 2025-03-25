<div align="center">
<img src="https://xdaforums.com/attachments/play_store_512-png.6161047/" alt="play_store_512.png" width="115" height="115">
</div>

<div align="center">

### YouTube Origin for Google TV

</div>

> **This project allows you to enjoy YouTube on Google TV without any ads, providing a seamless and uninterrupted viewing experience.**

## Features
- Watch YouTube without ads
- Original UI
- Compatible with Google TV
- Remove over-sharpening for video playback
- Support hardware decoding
- Block ads with uBlock Origin
- Skip sponsor segments with SponsorBlock
- Adjust video speed using **Up/Down** buttons (up to ∞) on the remote with Youtube Speed Control.
- Replaces thumbnails with Clickbait Remover for Youtube (experiment, not available now).

## Requirements
- **Android 9+** (Google TV, Fire TV, Android TV, Android tablets, Android phones)
- Bluetooth remote is required for use.

## Hardware Requirements

### For ARM-based Devices
- CPU: Minimum 2x Cortex-A76 + 6x Cortex-A55 (Tested)
- GPU: Mali-G76 MP4
- RAM: 8GB LPDDR4x
- Storage: UFS 2.1

### For x86-based Devices
- Processor: Intel® Core™ i3-1005G1 (Tested)
- RAM: 4GB

## Codecs

### For Android 10+ Devices
- By default, YouTube Origin supports **HW decoding** for video playback for **all devices** (except no-name Chinese devices with fake technical specs when checked with tools like AIDA64, CPU-Z, Antutu, Device Info HW, etc.).
- For **certified** Android devices without AV1 HW decoder, the app will default to using the **dav1d** decoder (dav1d is a default AV1 SW decoder on Android, available through the March 2024 Google Play System update).
- If the device does not have the dav1d decoder, the HW VP9 decoder will always take priority.

### For Android 9 Devices
Starting from version 1.3.7, YouTube Origin has added support for hardware decoding on Android 9 devices, including the following codecs:
- **H264/AVC1:** Hardware decoding is supported for most processors, including: Qualcomm, Intel, Samsung Exynos, Nvidia, Imagination Technologies, Texas Instruments, Huawei HiSilicon, MediaTek, Allwinner, Amlogic, Rockchip  (note that **Nvidia Shield** has been updated to Android 11, so this can be ignored).
- **VP9:** Hardware decoding is supported for Qualcomm, Samsung Exynos, Allwinner, Amlogic, MediaTek, Nvidia, and Rockchip.  
- **AV1:** Only supports SW decoding via dav1d decoder but it is highly unlikely that Android 9 devices will have **dav1d** available, meaning 90% of Android 9 devices will not support AV1.

**YouTube Origin works best on Android 10+ devices.** Therefore, although YouTube Origin supports Android 9 devices, newer devices are still recommended for the best experience.

To test AV1 videos, try TheFatRat's music videos, they all support the AV1 codec. You can check for frame drops and the codec being used in the video through the **Stats for Nerds** feature (this functionality will be available in upcoming updates).

## Playback

### Priority order for codecs

- HW decoding: AV1 > VP9 > AVC1
- SW decoding: AV1 (dav1d) > AVC1 (not supported VP9 SW)

### Video quality

- YouTube Origin supports video playback up to 4K@30fps (require device support 4K UI for all apps). However, most devices will be limited to 1080P@30fps, except for devices with Realtek chipsets.

> YouTube Origin does not support 60fps video streams for any resolution (only 30fps streams are supported). This means that if you search for a 4K@60fps video in YouTube Origin, you will only get maximum resolution at 720P@30fps. This happens because YouTube does not provide 30fps streams for 4K@60fps or 1080P@60fps videos. As a result, only 720P or lower resolutions are available at 30fps and will be selected for playback. Additionally, YouTube Origin does not support HDR for most videos on YouTube.

- Starting from March 2024, YouTube will gradually replace VP9 with the new default codec AV1, so there are many videos being upgraded to AV1 causing certain resolutions to be unavailable in specific codecs.

> For example, if you watching a video with 1080P set as the default quality, but for the next video, you check **Quality for current video** showing 720P, this is normal. This happens because 720P might be the highest available quality in AV1 (while 1080P is only available in VP9). Meaning, between 1080P VP9 & 720P AV1, 720P AV1 will be chosen for playback. Similarly, between 1080P AVC1 & 720P VP9, 720P VP9 will be preferred.

### Playback Limitation on 4K TVs

- This app only plays in 1080P on 4K TVs due to the weak GPUs found in most streaming devices, which can handle 4K video but render the UI at 1080P. As a result, everything displayed, including the UI, is at 1080P.

- YouTube Origin determines playback resolution based on the UI resolution. If the UI is rendered at 1080P, the app can only offer a maximum of 1080P@30fps or 720P@30fps. In contrast, the official YouTube app can detect the TV's actual resolution and force 4K playback, even with a 1080P UI.

- I’ve tried to enable 4K playback by forcing the viewport, but it’s not consistently reliable. For now, I’ll stick to the native UI for easier maintenance. This issue should resolve itself once all streaming devices support 4K UI.

Currently, only a few streaming devices support a real 4K UI, and most of these use Realtek chipsets (e.g., RTD1315C, RTD1325) with Mali-G57 capable of handling 4K UI. YouTube Origin supports 4K@30fps on these Realtek-based devices.

## Installation

### 1. Install "Send Files to TV" App
Download and install the **"Send Files to TV"** app on both your Android phone and Google TV.

### 2. Install "ZArchiver" App
Download and install the **"ZArchiver"** app on your Android phone.

### 3. Download YouTube Origin

#### Version 1.3.7

- **[armeabi-v7a](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.7/youtube_origin_googletv_armeabi-v7a_release35.zip)** `83.04 MB` (recommended for 90% of streaming devices)

- **[arm64-v8a](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.7/youtube_origin_googletv_arm64-v8a_release35.zip)** `86.30 MB`

- **[x86](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.7/youtube_origin_googletv_x86_release35.zip)** `94.90 MB`

- **[x86_64](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.7/youtube_origin_googletv_x86_64_release35.zip)** `90.97 MB`

##### Support and discuss more at [XDA Forums](https://xdaforums.com/t/app-android-tv-youtube-origin-for-google-tv.4699190/).

Please enable **Push Notifications** in the XDA Forums **[here](https://xdaforums.com/account/preferences)** and follow the official thread **[here](https://xdaforums.com/t/app-android-tv-youtube-origin-for-google-tv.4699190/watch)** to receive alerts about the latest updates for YouTube Origin. If you do not have an XDA account, you will need to create one.

You will need to manually install updates following the **[installation](https://gitlab.com/energylove/originproject#installation)**, so if you are satisfied with a specific release, the advice is that you do not necessarily need to update the app. A single release of YouTube Origin can be used for 6 months to 1 year without requiring updates.

### 4. Extract the ZIP file
Open the downloaded ZIP file in **"ZArchiver"** to extract it, you will find an APK file inside.

### 5. Transfer APK
Use the **"Send Files to TV"** to send that APK file to your Google TV.

### 6. Install APK on Google TV
Once the APK file is transferred, click to install it. You may need to grant permissions to install the APK.

### 7. Done
After installation, launch app to enjoy YouTube Origin.


## Changes

#### Version 1.3.7 `03.25.2025`

- Updated to v5.30.301 (YouTube for Android TV)
- Updated to v1.63.2 (uBlock Origin)
- Updated to v5.11.8 (SponsorBlock)
- Updated the latest rendering engine
- **New:** Added support for hardware decoding on Android 9 devices
- Optimized for Google TV Streamer with the latest firmware version
- Updated post #1 on XDA & GitLab, added information about the Codecs.

---

##### YouTube Origin Project.

![IMAGE_DESCRIPTION](https://image.jimcdn.com/app/cms/image/transf/none/path/s293f5a94d3403280/image/i4074178470a6059a/version/1677224408/image.png)
