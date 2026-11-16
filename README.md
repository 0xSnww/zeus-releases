# Zeus

Zeus is a full Chromium browser fork with a compact native interface inspired by Search and tab layouts adapted from Helium. It runs on Apple Silicon Macs and on 64-bit Windows.

## Download and install

### macOS

Download the **Zeus-*-arm64-*.zip** app archive from the [latest release](https://github.com/0xSnww/zeus-releases/releases/latest), extract it, and move **Zeus.app** into **Applications** before opening it. Requires an Apple Silicon Mac and macOS 13 or newer.

These early releases are self-signed and **not notarized by Apple**. If macOS blocks the first opening, use **System Settings > Privacy & Security > Open Anyway** for the Zeus download you selected. No Apple Developer membership is required to use Zeus.

### Windows

Download the newest **Zeus-*-win-x64-*.exe** installer from the [releases page](https://github.com/0xSnww/zeus-releases/releases) (Windows releases are tagged `zeus-win-N`) and run it. Requires 64-bit Windows 10 or newer. Zeus installs for your user only, without administrator rights, into `%LOCALAPPDATA%\Zeus`, and does not touch an installed Chrome or Chromium.

The installer is **not code-signed**, so Windows SmartScreen may warn on first run; choose **More info > Run anyway**. Before running it, you can compare its SHA-256 with the `SHA256SUMS.txt` file in the same release:

```powershell
Get-FileHash .\Zeus-0.1.7-win-x64-8.exe -Algorithm SHA256
```

## Updates

### macOS

Zeus checks for updates while running. You can also choose **Zeus > Check for Updates…**. Updates and the feed carry Sparkle Ed25519 signatures. Choose **Install and Relaunch** when ready.

The app update keeps browser data in the same **Zeus-Release** profile folder. This download does not include anyone else's browser profile.

### Windows

Zeus checks for updates while running, and from **Check for Updates…** in the app menu. It asks before downloading. The update list in [`update/`](update) is signed with an Ed25519 key, and Zeus installs a download only if it matches the size and SHA-256 in that signed list. You can keep browsing while it installs; Zeus then offers to relaunch. Your profile in `%LOCALAPPDATA%\Zeus\User Data` is kept.

Windows releases from 0.1.7 (build 8) onward update this way. Zeus 0.1.6 for Windows had no updater: install a newer release over it by hand once.

## Source and licenses

Each release includes its corresponding **Zeus-Source-*.zip** bundle with the pinned Chromium revision, Zeus changes, build scripts, and third-party notices. Chromium uses its BSD license; Helium-specific portions retain GPL-3.0; uBlock Origin retains its upstream license. Sparkle uses its BSD license and additional notices bundled with the Mac app.

This repository hosts release files, the Windows update list, and download instructions. Building Zeus is only needed when producing a new release; installing or updating a published release needs no source checkout or compiler.
