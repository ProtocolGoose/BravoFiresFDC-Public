# Bravo Fires FDC Public Release Process

This repository hosts public update metadata and release materials only. The source repository remains private.

## Important v4.x C# manifest change

The C# / Avalonia app checks:

```text
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/releases/latest.json
```

Older v3.x Python builds checked the root manifest:

```text
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/update_manifest.json
```

Keep both files updated for now:

```text
releases/latest.json     # v4.x C# / Avalonia updater
update_manifest.json     # legacy v3.x Python updater compatibility
```

## For each release

1. Build the Windows release package from the private source repository.
2. Zip the finished `dist\win-x64` output folder.
3. Name the ZIP using the version, for example:

```text
BravoFiresFDC_v4_1_3_beta.zip
```

4. Compute the SHA256 hash:

```powershell
Get-FileHash .\BravoFiresFDC_v4_1_3_beta.zip -Algorithm SHA256
```

5. Update the public repo files:
   - `releases/latest.json`
   - `update_manifest.json`
   - `CHANGELOG.md`
   - `README.md`
   - `RELEASE_PROCESS.md`, when workflow changes
   - legal/notice files, if they changed
6. Create a GitHub Release using the matching tag:

```text
v4.1.3-beta
```

7. Attach the release ZIP to the GitHub Release.
8. Confirm these URLs open JSON:

```text
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/releases/latest.json
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/update_manifest.json
```

9. In the app, click **Check Updates** and confirm:
   - Manifest Source is the public `releases/latest.json` URL.
   - Latest Version shows the published version.
   - Download Update downloads the ZIP.
   - SHA256 verification passes when a real hash is provided.
10. Post the Discord update announcement.

## Owner/repo alignment warning

The v4.1.3-beta app package points to:

```text
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/releases/latest.json
```

If your public repo is actually under a different owner, such as `ProtocolGoose`, update `AppPaths.UpdateManifestUrl` in the private C# source and rebuild the app before relying on the update checker.

## Legal URLs currently used by the app

- EULA: https://docs.google.com/document/d/1O5138qMW55mkR-I7GH4-uhajQKlGnTtPGfH1uVvLUko/edit?usp=sharing
- Terms of Service: https://docs.google.com/document/d/114uWecdznbvZxOsLGkLFWk-UxoIXdAZ_z0ak6yxQIpk/edit?usp=sharing
- Privacy Policy: https://docs.google.com/document/d/1pSEcPeTZI6Zj37UngS5YnY17-lKwd8ywlSi1f7pFohk/edit?usp=sharing

## Later goal

Add a separate updater helper executable that can close Bravo Fires FDC, replace files, and relaunch the new version. The current v4.x updater checks, downloads, and verifies only.
