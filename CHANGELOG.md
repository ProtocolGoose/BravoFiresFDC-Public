# Bravo Fires FDC Changelog

All notable public release changes for Bravo Fires FDC should be recorded here.

## v3.0.4-beta

- Added the expected online manifest URL(s) directly inside the Update Check unavailable window.
- Added Open Manifest URL so the primary raw GitHub manifest path can be tested directly.
- Added Copy Manifest URL(s) for troubleshooting GitHub path, branch, or repo visibility issues.
- Added manifest source display to successful/no-update update check windows when available.
- Corrected the changelog heading for v3.0.2-beta.
- Preserved the v3.0.3 Windows build script fix.
- No calculation or layout behavior changed.

## v3.0.3-beta

- Fixed the Windows build script so it calls PyInstaller through the active Python interpreter.
- Replaced the bare `pyinstaller` command with `python -m PyInstaller` to avoid PATH issues.
- Added error checks after pip setup, PyInstaller installation, and the PyInstaller build command.
- Added a final executable existence check before reporting Build complete.
- Prevented false successful build messages when PyInstaller fails to launch.
- No app layout, update-check, or calculation behavior changed.

## v3.0.2-beta

- Improved manual update check behavior when the online GitHub manifest is missing or unreachable.
- Replaced the raw 404 warning with a tester-friendly Update Check window.
- Shows the current app version and local packaged manifest version when online checks fail.
- Explains likely causes such as unpublished manifest, branch mismatch, GitHub outage, or local connection issues.
- Keeps startup update checks silent unless a newer online version is detected.
- No calculation or layout behavior changed.

## v3.0.1-beta

- Added a dedicated Updates / Changelog panel to the Help window.
- Added visible Check for Updates and View Changelog buttons inside Help.
- Preserved the v3.0-beta update manifest and changelog foundation.

## v3.0-beta

- Added `CHANGELOG.md` as the project change record source.
- Added `update_manifest.json` for GitHub-based update discovery.
- Added Help > Check for Updates.
- Added Help > View Changelog.
- Added silent startup update checking.
- Added update prompt with current/latest version, changelog summary, and release/download links.
- Preserved v2.1.3-beta responsive layout behavior.
- Preserved confirmed calculation behavior.

## v2.1.3-beta

- Added responsive Fire Solution card rendering for narrow module widths.
- Prevented output card values from clipping into icons by using compact card drawing when needed.
- Allowed output cards to reflow to 2x2 or 1-column layouts when enough module height is available.
- Added responsive Mission Inputs field wrapping for narrow module widths.
- Preserved user-saved module layouts during window resizing.
- Preserved confirmed calculation behavior.
