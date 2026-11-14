# Freesat Guide – KICKPI KP1 diagnostic starter

This is the first development milestone. It is **not yet a live-TV replacement**.
It checks whether Android exposes the existing tuner input, scanned channels and
programme listings to an ordinary third-party application.

## Build without a Windows PC

1. Sign in to GitHub in a browser and create a new, empty repository.
2. Upload the contents of this ZIP to the repository (the `.github` folder must
   be included at the repository root).
3. Open the repository's **Actions** tab.
4. Select **Build Android APK**, then **Run workflow**.
5. When the run completes, open it and download the `FreesatGuide-debug` artifact.
6. Extract the downloaded artifact ZIP to obtain `app-debug.apk`.
7. Copy the APK to the KICKPI KP1 and install it. You may need to allow installation
   from the app used to open the APK.

If GitHub asks you to enable Actions, enable them for this repository.

## Run the test

1. Leave the Homatics tuner connected.
2. Make sure the original Live TV app has already scanned channels successfully.
3. Open **Freesat Guide** from the Apps list.
4. Wait for the report, then photograph the screen or copy its text and send it back.

Do not uninstall, disable or clear data from the original Live TV app.

## Important limitations

- The diagnostic app does not tune channels or play video yet.
- Android TV's tuner and TV-provider permissions vary by firmware.
- The Homatics Live TV app may use a private vendor interface that other apps
  cannot access. If so, we will need to identify an officially exposed integration
  route before implementing live playback.
- This starter uses Android's public `TvInputManager` and `TvContract` interfaces.
