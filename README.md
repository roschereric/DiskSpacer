# DiskSpacer

A native macOS disk usage analyzer: a navigable sunburst with a synced list, color by file type, and safe deletion (Collector → Review → Trash → Undo).

This repository only hosts releases. The source code is private. All rights reserved.

## Download

Get the latest `.dmg` from [Releases](https://github.com/roschereric/DiskSpacer/releases/latest).

- macOS 14 or later, Apple Silicon or Intel (universal binary).
- Read-only scan, no network access, no telemetry. Deleted items go to the Trash.

## Install

1. Open the `.dmg` and drag **DiskSpacer** to **Applications**.
2. The build is ad-hoc signed (not notarized), so macOS blocks the first launch. Open it once, then go to **System Settings → Privacy & Security** and click **Open Anyway**. Or, in Terminal:

   ```
   xattr -dr com.apple.quarantine /Applications/DiskSpacer.app
   ```

3. For a complete scan, grant **Full Disk Access** (System Settings → Privacy & Security → Full Disk Access). The app shows how.

## Verify the download

```
shasum -a 256 DiskSpacer-*.dmg
```

Compare the result with the `.sha256` file attached to the release.
