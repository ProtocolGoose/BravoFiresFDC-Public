# Bravo Fires FDC Public Release Channel

This repository is the public release and update channel for **Bravo Fires FDC**, an Arma Reforger companion application.

The source code for Bravo Fires FDC is not stored in this repository. This repository hosts only public-facing release material such as:

- update metadata
- changelog entries
- release notes
- downloadable release packages through GitHub Releases
- legal notices
- third-party notices

## Current release candidate

The current release candidate is **v4.1.3-beta**.

This C# / Avalonia release fixes 8-digit grid/keypad handling. 8-digit grids are now treated as already-refined grid positions, while KP remains available for 6-digit grid workflows only.

## Update manifests

The C# / Avalonia desktop application checks:

```text
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/releases/latest.json
```

A legacy root manifest is also kept for older v3.x Python builds:

```text
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/update_manifest.json
```

## Release assets

Release ZIPs should be attached to GitHub Releases. For v4.1.3-beta, the expected release asset is:

```text
https://github.com/GooseProtocol/BravoFiresFDC-Public/releases/download/v4.1.3-beta/BravoFiresFDC_v4_1_3_beta.zip
```

Before publishing, update `releases/latest.json` and `update_manifest.json` with the real SHA256 hash of the uploaded release ZIP.

## Public legal documents

Current legal documents are maintained in Google Docs until the project website is available:

- EULA: https://docs.google.com/document/d/1O5138qMW55mkR-I7GH4-uhajQKlGnTtPGfH1uVvLUko/edit?usp=sharing
- Terms of Service: https://docs.google.com/document/d/114uWecdznbvZxOsLGkLFWk-UxoIXdAZ_z0ak6yxQIpk/edit?usp=sharing
- Privacy Policy: https://docs.google.com/document/d/1pSEcPeTZI6Zj37UngS5YnY17-lKwd8ywlSi1f7pFohk/edit?usp=sharing

## Important notice

Bravo Fires FDC is a standalone companion tool for Arma Reforger gameplay. It does not connect to Arma Reforger, inject into the game, read game memory, or control the game.

Bravo Fires FDC is an independent project and is not affiliated with, endorsed by, or sponsored by Bohemia Interactive or any real-world military organization.

## Source code

The source code is proprietary and is not distributed through this public repository.
