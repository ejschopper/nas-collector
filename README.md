# NAS Collector

A local Windows application for discovering, previewing, selecting, and safely collecting large JPEG artwork files from local folders, mapped drives, and SMB/UNC shares.

## Current status

**v4.0 Local Test — pre-release.** The application has not yet completed acceptance testing on a Windows workstation or a production NAS.

## Features

- Configurable local, mapped-drive, and UNC source paths
- Recursive discovery of configurable matching folders (default: `Final Images`)
- Project explorer and selective JPG/JPEG collection
- On-demand thumbnails, ICC-aware sRGB previews, and a local cache
- Dry-run mode and staged file transfers with optional SHA-256 verification
- Local disposable test workspace and acceptance checklist
- Python local web UI, PowerShell transfer engine

## Run locally

On Windows, install Python and the optional Pillow dependency, then run `START.cmd` from the application folder. For thumbnail support, use `INSTALL-THUMBNAILS.cmd`. Start with the local test workspace and dry-run enabled.

**Never use the production NAS for initial testing.** Verify file selection, destination structure, copy integrity, and retry behavior against disposable local fixtures first.

## Repository initialization

This repository is being initialized. The v4.0 application source files must still be imported from the previously prepared local-test build before the repository is runnable. This README does not imply that application source has already been committed.

## Security and data

Do not commit artwork, production JPEGs, thumbnails, local SQLite indexes, credentials, logs, local configuration, or any proprietary capture data. Original source files must remain read-only.

## Planned milestones

1. Import and review the v4.0 source
2. Run Windows acceptance tests and fix defects
3. Benchmark representative 50–200 MB+ Photoshop Standard JPEGs
4. Add CI and release packaging
