## YouTube Origin for Google TV

This project allows you to enjoy YouTube on Google TV without any ads, providing a seamless and uninterrupted viewing experience.

## Features
- Watch YouTube without ads
- Original UI
- Compatible with Google TV
- Support Hardware decoding.
- Block ads with uBlock Origin.
- Skip sponsor segments with SponsorBlock
- Adjust video speed using **Up/Down** buttons (up to ∞) on the remote with Youtube Speed Control.
- Replaces thumbnails with Clickbait Remover for Youtube (experiment, not available now).

## Requirements
- **Android 9+** (Google TV, Fire TV, Android TV, Android tablets, Android phones)
- Require Bluetooth remote to use YouTube Origin.

## Hardware Requirements

#### For ARM-based Devices:
- CPU: Minimum 2x Cortex-A76 cores, 6x Cortex-A55 cores (Tested)
- GPU: Mali-G76 MP4
- RAM: 8GB LPDDR4x
- Storage: UFS 2.1

#### For x86-based Devices:
- Processor: Intel Core i3 1005G1 (Tested)
- RAM: 4GB

## Codecs

#### For Android 10+ Devices:
- By default, **YouTube Origin** supports **HW decoding** for video playback for **all devices** (except no-name Chinese devices with fake technical specs when checked with tools like AIDA64, CPU-Z, Antutu, Device Info HW, etc.).
- For **certified** Android devices without AV1 HW decoder, the app will default to using the **dav1d** decoder (dav1d is a default AV1 SW decoder on Android, available through the March 2024 Google Play System update).
- If the device does not have the dav1d decoder, the HW VP9 decoder will always take priority.

#### For Android 9 Devices:
- **H264/AVC1:** HW decoding is only supported for **Qualcomm, MediaTek, Samsung Exynos**, and **Nvidia Tegra** devices (note that **Nvidia Shield** has been updated to Android 11, so this can be ignored).
- **VP9:** HW decoding is only supported for **Qualcomm** and **Exynos** devices.
- **AV1:** Only supports SW decoding via dav1d decoder but it is highly unlikely that Android 9 devices will have **dav1d** available, meaning 90% of Android 9 devices will not support AV1.

**YouTube Origin works best on Android 10+ devices.** Therefore, devices running Android 9 with chipsets from Amlogic, Allwinner, Rockchip will not be able to use HW decoding at all. I'm working on this to find ways to optimize HW playback for all codecs with the processors listed here with Android 9. If you experience dropped frames while using YouTube Origin, please be patient, wait for updates or upgrade to Android 10+ devices.

To test AV1 videos, try TheFatRat's music videos, they all support the AV1 codec. You can check for frame drops and the codec being used in the video through Stats for Nerds.

## Playback

#### Priority order for codecs:

- HW decoding: AV1 > VP9 > AVC1
- SW decoding: AV1 (dav1d) > AVC1 (not supported VP9 SW)

#### Video quality:

- YouTube Origin supports video playback up to 1080P/2K (always prioritizing AV1 when available).
- Starting from March 2024, YouTube will gradually replace VP9 with the new default codec AV1, so there are many videos being upgraded to AV1 causing certain resolutions to be unavailable in specific codecs.

For example, if you watching a video with 1080P set as the default quality, but for the next video, you check **Quality for current video** showing 720P, this is normal. This happens because 720P might be the highest available quality in AV1 (while 1080P is only available in VP9). Meaning, between 1080P VP9 & 720P AV1, 720P AV1 will be chosen for playback. Similarly, between 1080P AVC1 & 720P VP9, 720P VP9 will be preferred.

## Installation

### 1. Install "Send Files to TV" App
Download and install the **"Send Files to TV"** app on your Android phone and Google TV.

### 2. Install "ZArchiver" App
Download and install the **"ZArchiver"** app on your Android phone.

### 3. Download YouTube Origin

**Version 1.3.3**

- **[armeabi-v7a](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.3/youtube_origin_googletv_armeabi-v7a_release5.zip)** `83.36 MB` (recommended for 90% of streaming devices)

- **[arm64-v8a](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.3/youtube_origin_googletv_arm64-v8a_release5.zip)** `86.51 MB`

- **[x86](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.3/youtube_origin_googletv_x86_release5.zip)** `95.09 MB`

- **[x86_64](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.3/youtube_origin_googletv_x86_64_release5.zip)** `90.74 MB`

**Support and discuss more at [XDA Forums](https://xdaforums.com/t/app-android-tv-youtube-origin-for-google-tv.4699190/)**.

### 4. Extract the ZIP file
Open the downloaded ZIP file in **"ZArchiver"** to extract it, you will find an APK file inside.

### 5. Transfer APK
Use **"Send Files to TV"** to send that APK file to your Google TV.

### 6. Install APK on Google TV
Once the APK file is transferred, click to install it.

### 7. Done
After installation, launch app to enjoy YouTube Origin.


## Changes

**V1.3.3**

- Updated to v5.13.300 (YouTube for Android TV)
- Updated to v1.61.0 (uBlock Origin)
- Updated to v5.9.6 (SponsorBlock)
- Fixed white screen issue when open app
- Fixed navigation bar flickering issue
- Fixed the multi-touch issue on touch screen
- Fixed screen rotation issue on Android tablets/mobiles (Samsung Tab S10 tested)
- Fixed screensaver issue on Google TV
- Fixed crash issue on some devices
- ~~Enabled playback at the highest resolution quality (1080P/2K)~~
- Updated banner logo for Projectivy Launcher, Android TV launcher
- Optimization for Google TV Streamer, Fire TV Stick (MediaTek)
- Updated layout engine
- Updated **[Codecs](https://gitlab.com/energylove/originproject#codecs)** on XDA & GitLab. For Android 9 & 10+ devices, please read **Codecs** again.

---

**YouTube Origin Project**

![IMAGE_DESCRIPTION](https://image.jimcdn.com/app/cms/image/transf/none/path/s293f5a94d3403280/image/i4074178470a6059a/version/1677224408/image.png)
