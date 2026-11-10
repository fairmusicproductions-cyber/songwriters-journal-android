# SongwritersJournal — Android offline build kit

This repository builds a **debug APK** that packages all HTML, JS, CSS and icons into the Android application. GitHub is used only to build and download the APK, not to run it.

## Build on GitHub
1. Create a **new repository** for this Android build (do not overwrite the existing website repository).
2. Upload the **contents** of this folder, keeping `.github/workflows/android-debug-apk.yml` in its exact path. GitHub's web upload may not reliably upload hidden `.github` folders; use GitHub Desktop or git, or create the workflow via GitHub's Actions editor.
3. Open **Actions → Build Android APK → Run workflow**, or push to `main`.
4. After the build succeeds, download the artifact from the workflow run, unzip it and transfer `app-debug.apk` to your Android phone.
5. On Android, approve installation from the trusted file source when prompted, then install.

## Data safety
The Android app has **separate storage** from the Chrome/PWA website. Existing entries, voice recordings and saved ideas **do not migrate automatically**. Export from the website and import into the Android app before relying on it. Do not uninstall or clear the browser version until backups have been restored and verified.

## Distribution
This produces a debug-signed testing APK, not a production release. For public distribution use a securely stored private release signing key, release build, app icon configuration, versioning and device testing. Do not share debug builds as final public releases.

## Offline
App assets are bundled locally, so the interface and its built-in features do not require GitHub or internet. Recording, backup/import, and persistent storage still need on-device testing. This build has not been compiled or installed in this environment.
