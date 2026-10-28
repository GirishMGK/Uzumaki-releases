# Uzumaki — Downloads

Uzumaki is a set of audit analytics tools for Windows (Loan Analytics, JE
Audit, Statutory Extractor, Tally, GST Returns Downloader, Payroll
Validation, Audit Sampling and more). This repository holds its **built
releases only** — no source code. It is public so the app can download its
own updates without any credentials.

## Download

From the [**latest release**](../../releases/tag/latest):

| File | Use it for |
|---|---|
| `Uzumaki-Setup.exe` | **Normal install** — installs Uzumaki with a Start-menu shortcut |
| `Uzumaki.exe` | Portable — runs from any folder without installing |
| `*.sha256` | Checksums, to confirm a download is intact |
| `CHANGELOG.md` | What's new in each version (also shown in the app under About) |

The installer (`Uzumaki-Setup.exe`) is published from version 1.0.0 onwards.

## Updates

Once installed, Uzumaki checks for updates when it starts and from its About
page, and verifies every download against its checksum before installing it.
The previous version is kept, and Uzumaki goes back to it by itself if an
update fails to start.

- **Stable** — the [`latest`](../../releases/tag/latest) release. What everyone
  gets by default.
- **Beta** — the [`beta`](../../releases/tag/beta) release: the newest build,
  before it becomes stable. Choose the beta channel in the app's About page to
  receive it.
- **Every stable version** is also kept under its own number (e.g. `v1.0.0`)
  on the [Releases](../../releases) page, so an earlier version can be
  reinstalled.

## Check a download (optional)

In PowerShell, in the folder you downloaded to:

```powershell
Get-FileHash .\Uzumaki-Setup.exe -Algorithm SHA256
```

The hash shown must match the one in `Uzumaki-Setup.exe.sha256`
(`Uzumaki.exe.sha256` for the portable exe).

## If Windows blocks it

The exe isn't code-signed yet, so Windows may warn about it:

- **"Windows protected your PC" (SmartScreen):** click **More info → Run
  anyway**. Or right-click the file → **Properties** → tick **Unblock** → OK.
- **"Smart App Control blocked an app that may be unsafe"** (no "Run anyway"
  button): this stricter Windows 11 feature has no bypass in the dialog. It
  can be turned off under Windows Security → App & browser control → Smart
  App Control settings — but on many Windows 11 versions it can't be turned
  back on without reinstalling Windows, so treat that as a one-way decision.
  Code-signing, once in place, removes both warnings.
