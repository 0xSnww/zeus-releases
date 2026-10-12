# Zeus for macOS

Zeus is a full Chromium browser fork for Apple Silicon Macs, with a compact native interface inspired by Search and tab layouts adapted from Helium.

## Download and install

Download the **Zeus-*-arm64-*.zip** app archive from the [latest release](https://github.com/0xSnww/zeus-releases/releases/latest), extract it, and move **Zeus.app** into **Applications** before opening it. Requires an Apple Silicon Mac and macOS 13 or newer.

These early releases are self-signed and **not notarized by Apple**. If macOS blocks the first opening, use **System Settings > Privacy & Security > Open Anyway** for the Zeus download you selected. No Apple Developer membership is required to use Zeus.

## Updates

Zeus checks for updates while running. You can also choose **Zeus > Check for Updates…**. Updates and the feed carry Sparkle Ed25519 signatures. Choose **Install and Relaunch** when ready.

The app update keeps browser data in the same **Zeus-Release** profile folder. This download does not include anyone else's browser profile.

## Source and licenses

Each release includes its corresponding **Zeus-Source-*.zip** bundle with the pinned Chromium revision, Zeus changes, build scripts, and third-party notices. Chromium uses its BSD license; Helium-specific portions retain GPL-3.0; uBlock Origin retains its upstream license. Sparkle uses its BSD license and additional notices bundled with the app.

This repository hosts release files and download instructions. Building Zeus is only needed when producing a new release; installing or updating a published release needs no source checkout or compiler.
