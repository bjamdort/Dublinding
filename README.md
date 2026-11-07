# Dublin, Decoded 🍀

A self-guided Dublin walking tour Android app. Eight historical stops from Generator Dublin in Smithfield to Trinity College, map, GPS-triggered fact cards and saved progress.

## Download the APK (once the project is pushed)

1. Open [GitHub Actions — Build installable APK](https://github.com/bjamdort/Dublinding/actions/workflows/build-apk.yml).
2. Open the most recent successful workflow run (or click **Run workflow**).
3. Scroll to **Artifacts** and download **Dublin-Decoded-Android-APK**.
4. Unzip the artifact and install `app-debug.apk` on your Android phone. You may need to allow installing from that file manager/browser.

The workflow runs automatically on pushes to `main`, and can also be run manually. It uses JDK 17, Android SDK 35 and Gradle 8.9 to build the debug-signed APK.

## Features

- Eight stops: Smithfield chimney, Four Courts, Christ Church Cathedral, Dublin Castle, Temple Bar, Ha'penny Bridge, General Post Office and Trinity College.
- Walking route overlay and OpenStreetMap map tiles (requires internet).
- Foreground GPS proximity popups while the app stays open.
- Manual story cards and visit progress saved locally.
- Open walking directions in Google Maps.

## Build locally

Open the repository in Android Studio (JDK 17, SDK 35) and choose **Build APK(s)**. Or use `gradle assembleDebug` on a workstation with the Android SDK; APK output is `app/build/outputs/apk/debug/app-debug.apk`.

The APK is a native WebView wrapper with bundled tour HTML. Location access is requested only for the live tour and does not run in the background. Online map tiles, CDN libraries, and walking-route data need an internet connection. The APK is debug-signed for testing/personal installation, not a Play Store release. Check GPS behavior on your Android phone before relying on notifications.