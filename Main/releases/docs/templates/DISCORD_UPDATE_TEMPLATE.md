# Discord Update Announcement Template

**Bravo Fires FDC v4.1.3-beta is available for testing.**

This update fixes 8-digit grid/keypad handling in the C# / Avalonia branch. 8-digit grids now ignore KP because the grid already includes keypad-level precision. KP remains available for 6-digit grid workflows.

**Highlights**
- 8-digit grids no longer receive an extra KP offset.
- KP fields disable when 8-digit grids are detected.
- v4.1 floating module workspace is preserved.
- Update checker UI polish is preserved.

**Download**
https://github.com/GooseProtocol/BravoFiresFDC-Public/releases/tag/v4.1.3-beta

**Testing focus**
Please test 6-digit grid + KP, 8-digit grid without KP, and 8-digit grid with any KP accidentally entered to confirm KP is ignored for 8-digit grids.
