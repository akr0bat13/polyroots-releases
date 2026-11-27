# Polyroots releases

> **Status: no public release has been published yet.** This repository is prepared for official installation files; it currently contains documentation only.

Official installation files for **Polyroots** (generative mathematical art and animated wallpapers for macOS and Android).

- This repository contains **only** release assets, checksums and release notes. The source code is private.
- Every release has a `SHA256SUMS.txt`. Verify before installing: `shasum -a 256 <file>` (macOS) or `sha256sum <file>` (Linux), and compare with the value in the release.
- Official macOS builds will be signed with a Developer ID certificate and notarized; official Android builds will be signed with the Polyroots release key. If a file does not match its checksum, do not install it.
- Releases are announced in the Telegram bot `@polynomial_helper_bot` (Download and Updates) and in the Polyroots app (Settings → General → Check for Updates).
- A release that has been withdrawn is removed from the bot and the app, but files you already downloaded cannot be recalled: check the version in the app.

Tags: `macos-v<version>` and `android-v<version>`. Files: `Polyroots-macOS-<version>.dmg`, `Polyroots-Android-<version>.apk`, `SHA256SUMS.txt`, `manifest.json`.
