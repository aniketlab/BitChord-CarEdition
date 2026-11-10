# Changelog - BitChord (Car Edition)

This port modifies the original BitChord application to make it compatible with Android Car Head Units and Tablets.

## [1.5.4 (Car Edition)] - Synced with Upstream v1.9.1

### Added & Upgraded (Upstream Car-Optimized)
- **Major UI & Player Lag Fixes**: Stops Home artwork loops while scrolling/covered, optimizes Now Playing sheet redraws (`drawWithContent`), and brings back the stable classic player layout.
- **Offline Folders & Local Library Overhaul**: Added Folders tab (great for USB drives/SD cards), device playlists, "Open with" audio files, and `libffmpegJNI.so` decoding (ALAC/AC-3/E-AC-3).
- **Cached Songs Library & Unlimited Cache**: Keep played songs accessible offline while driving.
- **Content Preferences & Convert to Audio**: Toggle visibility of Home Videos, Top Picks, Recents, and Moods, plus one-tap Convert to Audio mode.
- **Full Podcast Support, Landscape Lyric Centering & Bounded Queue Startup**: Lighter RAM usage on large playlists and improved 720p landscape readability.

### Car Edition Optimizations & Bloatware Removal
- **Disabled Heavy Blending & Glass Refraction by Default**: `disableBlendEffects = true`, `glassPerformance = true`, `reduceDynamicBlur = true`, `animatedCanvas = false`, `preferMusicOnly = true`, `hideVolumeBar = true`.
- **Disabled Wear OS Watch Bundling & Background Service**: Excluded bundled `BitChordWear.apk` from assets and disabled `WearCommandService` + Settings entry.
- **Disabled Background Presence Telemetry & Seasonal Splash**: Disabled `AndroidPresence` periodic server pings and seasonal Diwali greeting popup.
- **Disabled Listen Together & In-built Equalizer UI**: Preserved Nakamichi/car hardware DSP integrity and minimized background network/CPU usage.
- **Fixed OTA Version Parser & Smart ABI Matching**: Strips `(Car Edition)` suffix in `AppUpdateChecker` so updates never self-loop, while matching `armeabi-v7a`, `arm64-v8a`, or `universal` builds accurately.

## [Car Edition 1.0]

### Added
- **32-bit Architecture Support (`armeabi-v7a`)**: Many car stereos operate on a 32-bit OS despite having 64-bit processors to conserve RAM. The original app only compiled for 64-bit (`arm64-v8a`), causing "App not installed" errors on these units. This version compiles for both 32-bit and 64-bit.
- **Explicit Screen Support**: Added `<supports-screens>` tags in the manifest to ensure the system recognizes the app supports large and extra-large screens.

### Removed / Changed
- **Portrait Orientation Lock**: Removed `android:screenOrientation="portrait"` from the `MainActivity`. Car head units are fundamentally landscape devices (e.g., 1280x720). Removing this lock prevents installation errors and allows the UI to adapt.
- **Hardware Requirements Bypassed**: Car head units often lack standard smartphone hardware like Telephony, Camera, GPS, or specific sensors, causing the Android Package Installer to reject the APK. Added explicit `<uses-feature android:required="false">` tags for:
  - Telephony
  - Camera
  - Bluetooth
  - Location / GPS / Network Location
  - WiFi
  - Microphone
  - Sensors (Accelerometer, Compass, Gyroscope)

### Credits
All core logic, design, and original development by [Kushagra Singh](https://github.com/kushagrasinghx).
