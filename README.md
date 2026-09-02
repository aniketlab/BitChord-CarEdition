<div align="center">

<br/>
<br/>

<img src="Logo.png" alt="BitChord app icon" width="200" />

# BitChord (Car Edition)

### Aesthetic YouTube Music Client - Ported for Android Car Head Units

<br/>

[![License](https://img.shields.io/github/license/kushagrasinghx/BitChord?style=for-the-badge&labelColor=0d1117)](https://github.com/kushagrasinghx/BitChord/blob/main/LICENSE)

<br/>

[**Credits**](#credits) · [**Download & Install**](#download) · [**Features**](#features) · [**Changelog**](#changelog)

</div>

> [!IMPORTANT]
> **Credits & Acknowledgement:** This project is a modified port of the original **BitChord** application. Full credit for the core application, original design, and source code goes to the original developer: **[Kushagra Singh (kushagrasinghx)](https://github.com/kushagrasinghx/BitChord)**. We sincerely thank them for making this fantastic project open-source.

---

<div align="center">

<h1><a id="target-device"></a>Target Device: Nakamichi NAM5360 Pro</h1>

*This port was specifically built for the **Nakamichi NAM5360 Pro** and similar Android Head Units that face compatibility issues with standard mobile applications.*

**Device Specifications:**
- **OS:** Android NK13.0 (32-bit OS on 64-bit chip)
- **Processor:** A55, 2.0GHz
- **RAM / Storage:** 4GB / 64GB
- **Display:** 9 Inch, 1280 x 720 (Landscape)
- **Audio:** 32-Band EQ, 4.1 Channel Pre-output

*If you have this head unit or any similar car stereo (often locked to 32-bit or missing standard phone hardware), this Car Edition is made for you!*

</div>

---

<div align="center">

<h1><a id="changelog"></a>What's New in Car Edition?</h1>

This version has been specifically modified to install and run smoothly on Android car stereos which often fail to install regular phone apps:
- **Added 32-bit Architecture Support (`armeabi-v7a`):** Many car stereos (like Nakamichi) run on 32-bit Android despite having 64-bit capable processors (to save RAM). The original app was strictly 64-bit.
- **Removed Strict Hardware Requirements:** Bypassed requirements for Telephony, Camera, GPS, etc., which often block app installation on car head units.
- **Removed Portrait Lock:** The app is now allowed to run on Landscape tablet screens (like 1280x720 9-inch car displays).

</div>

---

<div align="center">

<img src="Banner.png" alt="BitChord banner" width="100%" />

<h1><a id="features"></a>Features</h1>

<table>
  <tr>
    <td width="50%" valign="top">

#### Playback
- **Search, browse and play** anything available on YouTube Music.
- **Hi-Res lossless audio** — FLAC/ALAC from a configured module source, with YouTube Music as fallback.
- **Gapless playback with true crossfade**, adjustable 0–12s.
- **Automix [Beta]** — DJ-style transitions with beat-matching and tempo-stretching.
- **Offline downloads** — save tracks with embedded metadata.
- **Local music library** integration.
- **Background playback** via a proper foreground media session.

#### Experience
- **Animated album canvas** — motion artwork on the now-playing screen.
- **Word-synced lyrics** — word/syllable-level highlighting from multiple sources.
- **Dynamic, artwork-driven theming** — Material palette extracted from album art.
- **Frosted-glass UI** — Telegram-style translucent bars via Haze, Material 3 theming.

    </td>
    <td width="50%" valign="top">

#### Connectivity & Accounts
- **Sign in with your Google account** for personalized content.
- **Discord Rich Presence** — in-app login, live track/artist/album and progress.
- **Scrobbling** to Last.fm and ListenBrainz.
- **Pluggable sources** — add, edit, test and health-check module sources.

#### Controls & Tweaks
- **Per-network audio quality** — separate quality ceilings for Wi-Fi and mobile data.
- **Playback speed control** (0.5×–2.0×) and **skip silence**.
- **Sleep timer** — fixed presets or "stop after this track".
- **System equalizer** integration.
- **Stats for nerds** — codec, bit depth, sample rate, and more on the now-playing screen.

    </td>
  </tr>
</table>

</div>

---

<div align="center">

<h1><a id="download"></a>Download & Installation for Car Stereos</h1>

1. Grab the latest signed APK from the [Releases](#) page of this repository.
2. Copy the `.apk` file to a **USB Pen Drive**.
3. Plug the USB into your Car's USB port.
4. Open the **File Manager** app on your car screen, locate the `.apk` file, and tap to install. *(Make sure "Install unknown apps" is allowed in settings)*.

</div>

---

<div align="center">

<h1><a id="support"></a>Support the Original Developer</h1>

BitChord is free and always will be. Please consider supporting the original developer **Kushagra Singh** for his hard work:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/kushagrasinghx)
[![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/kuxhagrasingh)

</div>

---

<div align="center">

<h1><a id="license"></a>License</h1>

This project is licensed under the **GNU General Public License v3.0 (GPLv3)**. See the [LICENSE](LICENSE) file for details.

</div>
