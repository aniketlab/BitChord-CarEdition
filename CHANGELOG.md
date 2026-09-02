# Changelog - BitChord (Car Edition)

This port modifies the original BitChord application to make it compatible with Android Car Head Units and Tablets.

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
