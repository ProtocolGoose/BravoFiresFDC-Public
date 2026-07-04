# Bravo Fires FDC Public Release Process

This repository hosts public update metadata and release materials only. The source repository remains private.

## For each release

1. Build the Windows release package from the private source repository.
2. Copy the updated public files into this repository:
   - `update_manifest.json`
   - `CHANGELOG.md`
   - `LICENSE.md`
   - `EULA.md`
   - `PRIVACY_POLICY.md`
   - `TERMS_OF_SERVICE.md`
   - `THIRD_PARTY_NOTICES.md`
3. Commit and push the public files to `main`.
4. Create a GitHub Release using the matching version tag.
5. Attach the release ZIP or EXE package to the GitHub Release.
6. Confirm this URL opens JSON:

```text
https://raw.githubusercontent.com/ProtocolGoose/BravoFiresFDC-Public/main/update_manifest.json
```

## Legal URLs currently used by the app

- EULA: https://docs.google.com/document/d/1O5138qMW55mkR-I7GH4-uhajQKlGnTtPGfH1uVvLUko/edit?usp=sharing
- Terms of Service: https://docs.google.com/document/d/114uWecdznbvZxOsLGkLFWk-UxoIXdAZ_z0ak6yxQIpk/edit?usp=sharing
- Privacy Policy: https://docs.google.com/document/d/1pSEcPeTZI6Zj37UngS5YnY17-lKwd8ywlSi1f7pFohk/edit?usp=sharing

## Later v3.1+ goal

Automate release packaging and Discord changelog posting using GitHub Actions from the private source repository.
