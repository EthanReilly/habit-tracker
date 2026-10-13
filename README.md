# Atomic Habits Tracker

A daily habit tracker based on *Atomic Habits*: build good habits, break bad ones, with a four-law plan for each,
a 14-day record, streaks, a "never miss twice" nudge, a History tab and a library of templates.

The app is plain HTML, CSS and JavaScript in `www/`, packaged for Android with [Capacitor](https://capacitorjs.com).
Habits are saved on the phone and everything works offline.

## Install on your phone

1. Open the **Actions** tab and check the latest "Build Android APK" run is green (or run it with **Run workflow**).
2. Open the **Releases** page on your Android phone and download `atomic-habits.apk` from the "latest" release.
3. Open the file. Android will ask you to allow installs from your browser the first time. Allow it, then install.

This is a debug build for personal use, so it is not signed for the Play Store.

## Change the app

- Edit `www/index.html`. It holds the markup, styles and script.
- Push to `main`. GitHub builds a new APK and replaces the "latest" release.

To build on your own computer you need Node 22, Java 21 and the Android SDK:

```sh
npm ci
npx cap sync android
cd android && ./gradlew assembleDebug
```

The APK is written to `android/app/build/outputs/apk/debug/app-debug.apk`.

## Icons and splash screen

The source images are in `assets/`. After changing them, run `npm run assets` and commit the result.
