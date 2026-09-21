# DAEDALUS Studio 1.7.6

## Highlights

- **Fixed startup crash** — `folder:pick` / `files:pick` IPC handlers were registered twice (once in `main/index.ts`, once in `systemAccess.ts`), causing "handler already registered" errors on launch. Ownership now lives solely in `systemAccess.ts`.
- **Fixed fullscreen / zoom / titlebar wiring** — window controls now respond correctly.
- **Added `toggle-fullscreen` action** to the window-controls API.

## Verification

- ui-contract: 19/19 passing
- agent-teams harness: all flows passing

## Downloads

| File | Purpose |
| --- | --- |
| `DAEDALUS Studio Setup 1.7.6.exe` | Recommended — NSIS installer with shortcuts and uninstaller |
| `DAEDALUS Studio 1.7.6.exe` | Portable — single executable, no installation |

Integrity: verify with `SHA256SUMS.txt` (`sha256sum -c SHA256SUMS.txt` or `Get-FileHash` on Windows).

## Notes

- Windows x64, Electron 31.7.7.
- Auto-update metadata (`latest.yml`, `.blockmap`) is included for electron-updater differential downloads.
