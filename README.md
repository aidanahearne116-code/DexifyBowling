# DexifyBowling APK kit

An Android wrapper (a WebView) around the DexifyBowling web game, plus a GitHub
Actions workflow that builds the APK for you in the cloud.

## Build the APK with GitHub (no Android Studio needed)
1. Create a new repository on github.com (for example "DexifyBowling").
2. Upload everything in this folder to it, including the hidden `.github` folder.
3. Open the repository's **Actions** tab. The "Build APK" workflow runs on its own
   (or choose it and press **Run workflow**). It takes about 3 to 6 minutes.
4. Open the finished run and download **DexifyBowling-apk** from the Artifacts
   section. Unzip it to get `DexifyBowling-debug.apk`.
5. Copy the APK to your Android phone, tap it, and allow "Install unknown apps"
   when asked.

## Updating the game
Replace `app/src/main/assets/index.html` in the repository with a new version.
The workflow rebuilds the APK automatically.

## Notes
- The game is DexifyBowlingMobile: touch controls only, 16:9, and the app is locked to landscape.
- Android 8.0 or newer. APKs do not install on iPhones.
- This is a debug-signed APK, fine for installing on your own devices. Publishing
  to Google Play needs a release-signed build.
- The Fredoka and Nunito fonts load from Google Fonts, so offline the game falls
  back to system fonts.
