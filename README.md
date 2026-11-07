# Woordjager

A small offline-first Dutch spelling game for kids in primary school (basisschool). The first prototype has a curated starter bank of everyday words, English meanings, Dutch example sentences, and spelling hints.

## Play immediately
Just head to woordjager.vercel.app or, Open `index.html` in a browser. For the installable PWA experience, serve this folder over HTTPS or localhost so the service worker can cache it. On Android Chrome, use **Install app** or **Add to Home screen**.

## Build the Android APK
The Android WebView wrapper is in `android/`. This environment did not have the Android SDK/Gradle installed, so the APK itself could not be compiled here. The included GitHub Actions workflow builds a debug APK in the cloud:

1. Push this folder to a GitHub repository.
2. Open **Actions → Build Android APK → Run workflow**.
3. Download the `woordjager-debug-apk` artifact from the completed run.
4. Extract `app-debug.apk` and install it on Oscar's Android device. Android may ask permission to install apps from that source.

The debug APK is for testing, not Play Store distribution. It is offline and saves progress locally on the device.

## Notes
- The word bank is a starter set, not an official or exhaustive curriculum list.
- Some word difficulty varies by school and spelling method. Ask the teacher for recent test words to align future sets with classwork.
- Progress is stored in local browser/app storage. Clearing app data will reset it.
