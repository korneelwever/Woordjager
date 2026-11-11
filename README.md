# Woordjager

A small offline-first Dutch spelling game for kids in primary school (basisschool). The app has a word bank with English meanings, Dutch example sentences, and spelling hints. Daily practice presents up to 10 words, prioritising words the learner previously missed.

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
- The word bank is still being expanded. The current group 6 additions are based on CED-Groep's E6 spelling practice lists: [Oefenwoorden voor tussentoetsen E6](https://bestanden.cedgroep.nl/production/Webwinkel/Downloads/SLL-Oefenwoorden-voor-tussentoetsen-E6.pdf). The source lists define the spelling categories and candidate words; they are not a complete assessment of suitability for every child.
- Some word difficulty varies by school and spelling method. Ask the teacher for recent test words to align future sets with classwork.
- Progress is stored in local browser/app storage. Clearing app data will reset it.
