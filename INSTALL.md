# Install and update Lyre Studio

[**Download the latest release**](https://github.com/LyreStudio/lyre-releases/releases/latest) ·
[Release notes](https://github.com/LyreStudio/lyre-releases/releases) ·
[Back to Lyre Studio](README.md)

## Windows

For a 64-bit Intel or AMD PC, download the file ending in **Setup-…-x64.exe**,
run it, and launch Lyre Studio. The release's **Windows installer** link selects
this file for you.

Current Windows builds are unsigned, so Windows may display a SmartScreen warning.
Check that your download came from this repository before deciding whether to run it.

For a portable installation, download the Windows **.zip**, extract the whole archive
to a folder, and launch the app from there.

## Linux

For a 64-bit Intel or AMD computer, choose one of these formats:

- **AppImage:** save the file to a folder you own. In its file properties, allow it
  to run as a program, then open it. Some distributions require AppImage/FUSE support.
- **.deb:** install with your distribution's package installer on Debian/Ubuntu-based systems.
- **.rpm:** install with your distribution's package installer on RPM-based systems.
- **.tar.gz:** extract the whole archive and launch the included app.

AppImage is the format used by Lyre's Linux in-app updater. Other packages update manually.

## macOS

The existing 0.1.1 release includes an **Apple silicon** preview DMG (M1 and newer).
It contains a signed app, but the current download is **not notarized** and macOS
Gatekeeper rejects it. A notarized Mac release is needed for the normal installation
experience. Follow [release notes](https://github.com/LyreStudio/lyre-releases/releases)
for the next qualified Mac download.

No Intel Mac download is currently published. The existing Mac preview has no
active in-app update feed.

## iOS and Android

Phone clients are in testing. Distribution links will appear in the
[availability guide](https://lyrestudio.net/docs/release-status.html#ios)
when a public or testing channel is available.

## Your first project

Open a project folder in Lyre, connect a coding provider or local model, and set up
the project's preview command. Your host needs the dependencies and development
tools that the project uses. Local-model hardware requirements depend on the model
and model runner you choose.

Local projects and local-network workflows work without a Lyre cloud account.
Keep your host awake and connected when accessing it from another device.
[Follow the setup guide](https://lyrestudio.net/docs/quickstart.html).

## Updating

**Windows installer and Linux AppImage:** builds with updates enabled check the
release feed from within Lyre. Open **Settings → About → App updates**, choose
**Check**, then use **Update** when a newer version is available. Automatic download
can be enabled there; applying the update restarts the app. Let running tasks finish
and save your work first.

**Portable ZIP, .deb, .rpm, .tar.gz, and builds without in-app updates:** download
the newer package from [Releases](https://github.com/LyreStudio/lyre-releases/releases)
and replace or upgrade the app using the same installation method. Read the release
notes before switching versions or installation types.

Lyre stores its saved app state separately from the application files. Keep that
existing profile and your project folders when updating; do not delete or reset them.
Back up valuable work before an early-access upgrade. A platform's completed upgrade
checks and any migration steps belong in that release's notes.

## Choosing files and checking downloads

Current package names begin with **Lyre-Foundation**. These are Lyre Studio downloads;
the architecture labels `x64`, `x86_64`, and `amd64` all identify 64-bit Intel/AMD builds.
`arm64` identifies the Apple silicon Mac preview.

Use the release's labeled download links. The **.yml** and **.blockmap** files are
for the updater. GitHub's **Source code (zip/tar.gz)** links contain this public
repository's documentation, not the Lyre application.

The current **SHA256SUMS.txt** covers the Windows and Linux packages. To compare a
saved file against its entry, use PowerShell's `Get-FileHash -Algorithm SHA256`
on Windows or `sha256sum` on Linux. Matching a checksum confirms the download's
bytes match the published value; it does not replace platform signing checks.

[Report an installation problem](https://github.com/LyreStudio/lyre-releases/issues/new?template=bug_report.yml).
