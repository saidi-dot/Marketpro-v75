# MarketPro V75 — Android build package

This package preserves the V75 project files and includes an Android dashboard plus a GitHub Actions workflow for building a debug APK.

## Build in Android Studio
1. Open the `android/` folder as a project in Android Studio.
2. Allow Gradle sync and install the requested Android SDK if prompted.
3. Choose **Build → Build App Bundle(s) / APK(s) → Build APK(s)**.
4. For a debug build, find the APK at `android/app/build/outputs/apk/debug/app-debug.apk`.

## Build on GitHub
The `.github/workflows/android-apk.yml` workflow is included. Once the files are committed to `saidi-dot/Marketpro-v75`, open **Actions → Build MarketPro Android APK → Run workflow** (or push an Android-source change). Download the `MarketPro-V75-debug-apk` artifact from the completed run.

## Important
This is a build-ready source package, not an already-built APK. The current Android dashboard is a preview and uses demonstration metrics. Live marketing accounts, AI, payment processing, backend deployment, security checks, privacy policy and Play Store compliance are still needed before public production launch.
