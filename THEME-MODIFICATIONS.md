# Lyreon theme modifications

This source snapshot defaults to the Midnight Black theme with electric-blue accents.

## Changes
- Default theme mode is `BLACK` (pure-black background suitable for AMOLED displays).
- Default accent is `#168CFF` (electric blue).
- Dynamic Material You colors are disabled by default so the wallpaper does not override the chosen palette.
- Artwork-derived accent colors are disabled by default so album covers do not change the blue accent.
- Settings defaults and the default accent swatch were updated to match.

Music playback, navigation, download, database, and repository logic were not intentionally changed.

## Build
The repository intentionally does not include `gradle-wrapper.jar`. Build with JDK 21, Android SDK platform 36/build-tools 36.0.0, and Gradle 9.6.1 installed:

```bash
gradle :app:assembleDebug
```

The debug APK is written to `app/build/outputs/apk/debug/`.
