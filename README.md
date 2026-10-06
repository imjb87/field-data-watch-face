# Field Data Pixel

Field Data Pixel is a resource-only Wear OS watch face built with Watch Face
Format 1. It is designed for the Pixel Watch 3: a quiet dark field, a clear
local-time readout, and useful at-a-glance data for steps and battery.

## Build locally

The project needs a Java 17+ runtime and an Android SDK with platform 35.

```sh
./gradlew :watchface:assembleDebug
```

The installable debug APK is written to:

```text
watchface/build/outputs/apk/debug/watchface-debug.apk
```

## Cloud build

Every push to `main` runs the GitHub Actions build. The workflow uploads
`FieldDataWatchFace.apk` as an Actions artifact and refreshes the `latest`
GitHub Release asset.

## Install on a Pixel Watch 3

1. Download `FieldDataWatchFace.apk` from the repository's **Releases → latest**
   page onto the Pixel phone.
2. On the watch, enable **Developer options**, then **ADB debugging** and
   **Wireless debugging**.
3. Open **Wear Installer 2** on the phone, pair it with the watch, select the
   downloaded APK as a custom APK, and install it.
4. Long-press the watch face, choose **Add watch face**, and select **Field
   Data Pixel**.

The watch face is standalone and contains no companion-phone code.
