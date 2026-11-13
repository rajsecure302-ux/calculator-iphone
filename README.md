# Calculator — iPhone Style

A clean, fast calculator with the familiar iPhone look. Works fully offline.

- **No ads. No tracking. No sign-in. No internet permission.**
- iPhone-style keypad: circular keys, orange operators, wide zero key
- Expression line so you always see what you are calculating (`8.5 + 2 =`)
- Real iOS percent behaviour (`50 + 10%` → `55`, `200 × 10%` → `20`)
- Repeated equals repeats the last operation (`2 + 3 = =` → `8`)
- AC/C auto-switching, `+/-`, division-by-zero guard, haptic feedback
- APK is under 50 KB, `minSdk 24` (Android 7+), `targetSdk 35`

## Download

Grab the signed APK from the [latest release](../../releases/latest):
`Calculator-1.0.apk` — installed like any normal app (allow "install unknown apps" for your browser/file manager).

## What is in this repo

| Path | Description |
|---|---|
| `web/index.html` | The whole calculator UI (HTML/CSS/JS, single file) |
| `android/MainActivity.java` | WebView wrapper activity (edge-to-edge safe, haptics, back handling) |
| `android/AndroidManifest.xml` | Manifest: `VIBRATE` permission only, no internet |
| `privacy.html` | Privacy policy (also served via GitHub Pages) |
| `screenshots/` | Phone screenshots (1080×1920) |
| `icon-512.png`, `feature-graphic.png` | Store graphics |
| `Calculator-1.0.apk` | Release-signed APK (also attached to the release) |

## Privacy policy

Published at: **https://rajsecure302-ux.github.io/calculator-iphone/privacy.html**

The app collects nothing, has no analytics, no ads, and holds no internet permission — the
policy page is the only web content related to it.

## Build

The APK is a thin WebView wrapper around `web/index.html`. Open the `android/` sources in
Android Studio (new project, empty activity, `minSdk 24`, `targetSdk 35`), drop
`web/index.html` into `assets/`, build a release bundle. Any standard toolchain works; the
committed APK was signed with a private upload key (not in this repo).

## License

MIT — do whatever you like with the code. The name "iPhone" is used descriptively only;
this project is not affiliated with Apple.
