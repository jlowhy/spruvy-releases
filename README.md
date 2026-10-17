# Spruvy releases

Download the recommended build, **nightly 48**:

| Platform | Download |
| --- | --- |
| Mac · Apple Silicon · macOS 13+ | [Download Mac app](https://github.com/jlowhy/spruvy-releases/releases/download/v0.0.1-nightly.20261017.48/Spruvy-0.0.1-nightly.20261017.48-macos-arm64.zip) · [Checksum](https://github.com/jlowhy/spruvy-releases/releases/download/v0.0.1-nightly.20261017.48/Spruvy-0.0.1-nightly.20261017.48-macos-arm64.zip.sha256) |
| Linux / WSL · x64 | [Download host](https://github.com/jlowhy/spruvy-releases/releases/download/v0.0.1-nightly.20261017.48/spruvy-host-internal-linux-x64-0.0.1-nightly.20261017.48.tar.gz) · [Checksum](https://github.com/jlowhy/spruvy-releases/releases/download/v0.0.1-nightly.20261017.48/spruvy-host-internal-linux-x64-0.0.1-nightly.20261017.48.tar.gz.sha256) |

[All releases and verification files](https://github.com/jlowhy/spruvy-releases/releases).

This repository contains public release files and installation instructions. Spruvy's development repository is private. Release files contain readable application code and bundled third-party license notices.

## Install on a Mac

1. Download the macOS ZIP and its matching `.sha256` file.
2. Check the archive with `shasum -a 256 -c <archive-name>.sha256`.
3. If replacing an older Spruvy, finish local work. If this Mac is the selected host, choose **Stop host** in **Settings > Host** before quitting. Then quit Spruvy, extract the ZIP, and drag `Spruvy.app` into Applications. Replacement preserves its saved data.
4. Open Spruvy. These personal builds are ad hoc signed and are not notarized. If macOS blocks opening, use System Settings > Privacy & Security > Open Anyway for the app you downloaded here.

Each archive includes installation instructions and third-party license notices. Linux host archives include their own manager and bundled Node runtime. Phone installation is separate; these downloads contain no iOS app.

## Verify updates

Releases include checksums and an Ed25519-signed `nightly-manifest.json`. A checksum detects corruption; the signature establishes update authenticity when checked against a previously trusted public key. Never substitute a key supplied by an untrusted download.

## Update Spruvy

Install nightly 48 or later manually once. These Mac builds check for signed updates on startup and periodically while open. When an update is available, open **Settings > Software** and choose **Update and restart**. Spruvy downloads and verifies the archive, waits for active local work, replaces the app, and reopens it. Saved data and pairing are preserved. The selected remote host is updated separately.

For a managed Linux host, follow the included installation guide. The local owner can allow paired clients to request updates with `spruvy-host-internal remote-updates enable` while the host is running. Then use **Settings > Host** in a connected client to check and confirm a nightly update.

No GitHub login or token is needed in installed apps. Checks do not install updates automatically. Do not delete application data when updating.
