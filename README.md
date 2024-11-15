# YouTube Origin for Google TV

This project allows you to enjoy YouTube on Google TV without any ads, providing a seamless and uninterrupted viewing experience.

## Features
- Watch YouTube without ads
- Compatible with Google TV
- Original UI
- Support VP9, AV1 codecs.
- Block ads with uBlock Origin.
- Skip sponsor segments with SponsorBlock.
- Adjust video speed using **Up/Down** buttons (up to ∞) on the remote with Youtube Speed Control.
- Replaces thumbnails with Clickbait Remover for Youtube (experiment, not available now).

## Requirements
- **Android 9+** (Google TV, FireOS, Android TV, Android tablets, Android phones)
- Require Bluetooth remote to use YouTube Origin.

## Hardware Requirements

### For ARM-based Devices
- Processor: Minimum 2x Cortex-A76 cores, 6x Cortex-A55 cores (Tested)
- GPU: Mali-G76 MP4
- RAM: 8GB DDR4
- Storage: UFS 2.1

### For x86-based Devices
- Processor: Intel Core i3 1005G1 (Tested)
- RAM: 4GB

## Codecs

- AVC1 codec (HW and SW decoding supported)
- VP9 codec (HW decoding only, SW decoding not supported)
- AV1 codec (HW and SW decoding supported)

**Notes**:
- AV1 [SW] is preferred over VP9 [HW] in this project (original app prioritizes HW over SW).
- This project is currently facing an issue with accurately detecting processors that support hardware decoding for both AVC1 & VP9 on some devices (MediaTek, Amlogic, Allwinner, Rockchip, Realtek & Broadcom). I’ll work on fixing this issue in next months.
- To test AV1 videos, try TheFatRat's music videos, they all support the AV1 codec.

## Installation

### 1. Install "Send Files to TV" App
Download and install the **"Send Files to TV"** app on your Android phone and Google TV.

### 2. Install "ZArchiver" App
Download and install the **"ZArchiver"** app on your Android phone.

### 3. Download YouTube Origin

**Version 1.3.2**

- **[armeabi-v7a](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.2/youtube_origin_googletv_armeabi-v7a_release2.zip?ref_type=heads)** `82.46 MB`

- **[arm64-v8a](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.2/youtube_origin_googletv_arm64-v8a_release2.zip?ref_type=heads)** `85.67 MB`

- **[x86](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.2/youtube_origin_googletv_x86-32bit_release2.zip?ref_type=heads)** `93.72 MB`

- **[x86_64](https://gitlab.com/energylove/originproject/-/blob/main/Releases/v1.3.2/youtube_origin_googletv_x86-64bit__release2.zip?ref_type=heads)** `89.43 MB`


### 4. Extract the ZIP file
Open the downloaded ZIP file in **"ZArchiver"** to extract it, you will find an APK file inside.

### 5. Transfer APK
Use **"Send Files to TV"** to send that APK file to your Google TV.

### 6. Install APK on Google TV
Once the APK file is transferred, click to install it.

### 7. Done
After installation, launch app to enjoy YouTube Origin.


## Changes

**V1.3.2**

- Updated to v5.12.300 (YouTube for Android TV)
- Updated to v5.9.5 (SponsorBlock)
- Fixed some bugs
- Updated layout engine
- Hardware requirements changed due to the new UI

Support and discuss more at **[XDA Forums](https://xdaforums.com/t/app-android-tv-youtube-origin-for-google-tv.4699190/)**.

---

**YouTube Origin Project**

![IMAGE_DESCRIPTION](https://image.jimcdn.com/app/cms/image/transf/none/path/s293f5a94d3403280/image/i4074178470a6059a/version/1677224408/image.png)
