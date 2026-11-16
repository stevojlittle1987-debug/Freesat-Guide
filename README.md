# Freesat Guide — Diagnostic 0.1

This is the first diagnostic build for the Kickpi KP1 (Android 14) and Homatics USB-C DVB-S2X tuner.

## What it checks
- Device model and Android version.
- Android TV inputs visible to an ordinary installed app.
- Whether the public Android Tuner SDK class is present.
- Whether the firmware reports a Tuner HAL version.
- Public tuner methods mentioning frontends.

It does **not** scan, tune, record, or interrupt Homatics Live TV.

## Build without a Windows PC
1. Create a new empty GitHub repository named `FreesatGuide`.
2. Upload the contents of this ZIP to the repository root. Make sure `.github/workflows/build.yml` is included; GitHub's upload interface may require creating the folders first or uploading the files via the web editor.
3. Open the repository's **Actions** tab.
4. Select **Build Freesat Guide diagnostic APK**.
5. Choose **Run workflow**. Alternatively, uploading files to the `main` branch should trigger a build.
6. When the run finishes, open it and download the artifact named `FreesatGuide-Diagnostic-APK`.
7. Extract the ZIP artifact. It contains `app-debug.apk`.
8. Copy the APK to the Kickpi KP1 and install it. You may need to allow installation from the file manager you use.

## Return the diagnostic results
Open **Freesat Guide Diagnostic** on the Kickpi and send a photo/screenshot of the report. The key information is the Android TV Inputs list, Tuner SDK class result, and Tuner HAL version.

## Important
A successful Homatics Live TV tuner scan proves that the manufacturer's application can use the tuner. It does not prove that a separately installed app has permission or a supported API to access it. The diagnostic helps establish the next step before we build scanning and playback.
