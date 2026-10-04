# ESN App Store — Android + iOS

This is the native-mobile version of the premium ESN App Store.

## What it uses
- Capacitor 8.5.2
- One HTML/CSS/JS codebase in `www/`
- Native Android wrapper
- Native iOS wrapper
- GitHub Actions builds
- ESN app icon + splash assets

App ID: `com.esnetwork.appstore`

## Android
Run the **Build Android APK** GitHub Action.
The build artifact is:

`ESN-App-Store-Android.apk`

This debug APK can be installed on Android devices after allowing installs from the browser/file app used to open it.

## iOS
Run the **Build iOS App** GitHub Action.
It outputs:
- `ESN-App-Store-iOS-Simulator.zip`
- `ESN-App-Store-Xcode-Project.zip`

The simulator build does not require Apple signing.

### Installing on a real iPhone
Apple requires the application to be code-signed for a physical iPhone. The Xcode project produced by the workflow is ready for signing, but an installable device IPA requires an Apple signing identity/provisioning profile.

## Editing the store
- Store interface: `www/index.html`
- App catalog: `www/apps.json`
- Native configuration: `capacitor.config.json`
- Branding: `assets/`

## GitHub
Upload this entire project to a GitHub repository. Both workflows are already included under `.github/workflows/`.
