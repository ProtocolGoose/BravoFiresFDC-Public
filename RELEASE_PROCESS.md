# Public Release Process

This repository is the public update and release channel for Bravo Fires FDC.

## Repo role

- Keep source code private in the private development repository.
- Publish only release metadata, changelogs, legal notices, and packaged builds here.

## Standard release flow

1. Build the release package from the private source repository.
2. Update `CHANGELOG.md` in this public repository.
3. Update `update_manifest.json` with the new version, summary, URLs, and release date.
4. Create a GitHub Release in this public repository.
5. Attach the official ZIP and/or EXE package to the release.
6. Confirm the raw manifest opens correctly:

```text
https://raw.githubusercontent.com/ProtocolGoose/BravoFiresFDC-Public/main/update_manifest.json
```

7. Test Bravo Fires FDC > Help > Check for Updates.

## Version tag format

Use tags like:

```text
v3.0.5-beta
v3.1.0-beta
v3.1.0-stable
```
