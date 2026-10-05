# YTBackgroundOnly

A lightweight iOS tweak for YouTube that enables continuous background playback and bypasses the annoying "Continue watching?" / "Are you there?" interruption dialogs.

[![Build Tweak](https://github.com/hooray804/YTBackgroundOnly/actions/workflows/build.yml/badge.svg)](https://github.com/hooray804/YTBackgroundOnly/actions/workflows/build.yml)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)
![Platform](https://img.shields.io/badge/Platform-iOS-lightgrey.svg)

---

## ✨ Features

- **Background Audio Playback:** Listen to your favorite videos and music while using other apps or with your device locked.
- **Bypass "Are you there?" Prompts:** Prevents YouTube from pausing long playback sessions and asking if you are still watching.
- **Ultra Lightweight:** Pure Objective-C / Logos runtime hooks without complex UI overhead or unnecessary modifications.
- **Multiple Injection Support:** Compatible with Rootless Jailbreak, TrollStore, LiveContainer, SideStore, and Feather.

---

## 📥 Installation

Download the latest `.deb` or `.dylib` from the [GitHub Actions Artifacts](https://github.com/hooray804/YTBackgroundOnly/actions) or Releases page.

### 1. Sideloading (Feather / SideStore / Sideloadly / TrollStore)
- Inject `YTBackgroundOnly.dylib` (or the `.deb` package) directly into your decrypted YouTube `.ipa`.
- For **LiveContainer**, simply add `YTBackgroundOnly.dylib` under the app's Tweak / Dynamic Library settings.

### 2. Jailbroken Devices (Rootless)
- Open the `.deb` file in your preferred package manager (Sileo, Zebra) and install.
- Respring or restart the YouTube app.

---

## 🛠️ Building from Source

### Prerequisites
- macOS or Linux with [Theos](https://theos.dev/) installed.
- iOS SDK (iOS 14.0 or higher recommended).

### Local Build

```bash
# Clone the repository
git clone [https://github.com/hooray804/YTBackgroundOnly.git](https://github.com/hooray804/YTBackgroundOnly.git)
cd YTBackgroundOnly

# Build Rootless .deb package
make clean package THEOS_PACKAGE_SCHEME=rootless FINALPACKAGE=1

# Build standalone .dylib for sideloading
make clean FINALPACKAGE=1

```

The compiled binary will be located in `.theos/obj/` or `packages/`.

---

## 📜 Credits & Acknowledgments

* [YouMod](https://github.com/Tonwalter888/YouMod) for inspiration and reference.
* [Theos](https://theos.dev/) development team.

---

## 📄 License

This project uses GPLv3 license. See [LICENSE](LICENSE) for more details.
