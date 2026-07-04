# Bravo Fires FDC Changelog

## v3.0.5-beta

- Pointed the in-app update checker to the public `ProtocolGoose/BravoFiresFDC-Public` release channel on the `main` branch.
- Removed old private-source-repository manifest fallback URLs from the app.
- Updated EULA, Terms of Service, and Privacy Policy links to the official Google Docs documents.
- Added a one-time EULA acceptance popup before the main app opens.
- If the EULA is declined or the popup is closed, the app closes.
- Stores EULA acceptance locally per Windows user at `%APPDATA%\BravoFiresFDC\legal_acceptance.json`.
- Added Help > Legal / Notices buttons for opening the official online EULA, Terms of Service, and Privacy Policy.
- Preserved v3.0.4 update troubleshooting UI and v3.0.3 Windows build script reliability fix.
- No calculation or layout behavior changed.

## v3.0.4-beta

- Added the expected online manifest URL(s) to the Update Check unavailable window.
- Added an Open Manifest URL button for testing the primary raw GitHub manifest path directly.
- Added a Copy Manifest URL(s) button for troubleshooting GitHub path, branch, or repo visibility issues.
- Added manifest source display to successful/no-update update check windows when available.
- Corrected the changelog heading for v3.0.2-beta.
- Preserved v3.0.3-beta Windows build script reliability fixes.
- Preserved v3.0.x update-check behavior and Help window update controls.
- Preserved v2.1.3-beta responsive layout and confirmed calculation behavior.

## v3.0.3-beta

- Fixed the Windows build script so it uses `python -m PyInstaller` instead of relying on the `pyinstaller` command being available on PATH.
- Added build failure checks after pip/PyInstaller setup and after the PyInstaller build command.
- The build script now stops and reports a failure instead of printing a false Build complete message.
- Added a final check that confirms `dist\BravoFiresFDC_v3_0_3_beta.exe` actually exists.
- Preserved v3.0.2-beta update-check behavior and Help window update controls.
- Preserved v2.1.3-beta responsive layout and confirmed calculation behavior.

## v3.0.2-beta

- Improved manual update check behavior when the online GitHub manifest is missing, unpublished, or unreachable.
- Replaced the raw 404 warning with a tester-friendly Update Check window.
- Shows the current app version and local packaged manifest version when online checks fail.
- Explains likely causes such as unpublished manifest, branch mismatch, GitHub availability, or local connection issues.
- Keeps startup update checks silent unless a newer online version is detected.
- Preserved v3.0.1-beta Help window update controls.
- Preserved v3.0-beta update manifest and changelog foundation.
- Preserved v2.1.3-beta responsive layout behavior and calculation behavior.

## v3.0.1-beta

- Fixed the Help window so update controls are clearly visible.
- Added a dedicated Updates / Changelog panel at the top of Help.
- Kept Check for Updates and View Changelog available from Help.
- Preserved v3.0-beta update manifest and changelog foundation.
- Preserved v2.1.3-beta responsive layout behavior and calculation behavior.

## v3.0-beta

### Added
- Added the V3 update/changelog foundation.
- Added `CHANGELOG.md` as the project change record source.
- Added `update_manifest.json` as the local and GitHub-hosted update manifest source.
- Added **Check for Updates** support from the Help window.
- Added **View Changelog** support from the Help window.
- Added a startup update check that stays silent unless a newer version is found.
- Added update prompt window with current version, latest version, summary, and release/download links.

### Changed
- Updated public version from `v2.1.3-beta` to `v3.0-beta`.
- Updated build output to `BravoFiresFDC_v3_0_beta.exe`.
- Updated launcher and build scripts for the V3 beta package.

### Preserved
- Preserved v2.1.3-beta responsive Fire Solution and Mission Inputs behavior.
- Preserved v2.1-beta Snap ON/OFF, keypad text fields, compact inputs, and 1080p header behavior.
- Preserved confirmed calculation behavior.

### Planned for later V3.x
- GitHub Actions release packaging.
- Discord webhook changelog posting from GitHub releases.
- Optional in-app download helper / updater workflow.

## v2.1.3-beta

- Added responsive Fire Solution card rendering.
- Added responsive Mission Inputs field wrapping.
- Prevented output cards and input fields from becoming unusable on narrower layouts.
- Preserved user-saved module layouts during resizing.

## v2.1-beta

- Added Snap ON/OFF toggle in Edit Mode.
- Removed Friendly input from Mission Inputs.
- Converted Gun KP and Target KP from dropdowns to text fields.
- Compacted labels for smaller screens.

## v2.0-beta

- Improved 1080p layout usability.
- Hid Calculate and Shot Correction while Edit Mode is active.
- Compacted header and layout spacing.
