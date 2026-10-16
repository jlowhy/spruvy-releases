# Spruvy releases

Download Spruvy for Apple Silicon macOS and the Linux x64 host from [Releases](https://github.com/jlowhy/spruvy-releases/releases).

This repository contains public release files and installation instructions. Spruvy's development repository is private. Release files contain the application code and may be inspected and redistributed subject to their bundled license notices.

## Install on a Mac

1. Download the macOS ZIP and its matching `.sha256` file.
2. Check the archive with `shasum -a 256 -c <archive-name>.sha256`.
3. Extract the ZIP and drag `Spruvy.app` into Applications. Quit an existing Spruvy before replacing it. Replacement preserves its saved data.
4. Open Spruvy. These personal builds are ad hoc signed and are not notarized. If macOS blocks opening, use System Settings > Privacy & Security > Open Anyway for the app you downloaded here.

Each archive includes installation instructions and third-party license notices. Linux host archives include their own manager and bundled Node runtime. Phone installation is separate; the nightly workflow's iOS Simulator check does not produce an installable iPhone app.

## Verify updates

Releases include checksums and an Ed25519-signed `nightly-manifest.json`. A checksum detects corruption; the signature establishes update authenticity when checked against a previously trusted public key. Never substitute a key supplied by an untrusted download.

Automatic update support is being prepared. Until it ships, download and install updates manually. Do not delete your application data when updating.
