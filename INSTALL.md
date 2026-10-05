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

For an **Apple silicon** Mac (M1 and newer), download the **.dmg** from the
latest release, open it, and drag **Lyre Studio** into **Applications**. Launch
Lyre from Applications. The 0.1.4 Mac download is Developer ID signed, notarized,
and stapled.

A **.zip** is also available. No Intel Mac package is currently published.
The 0.1.4 release includes the macOS update feed; older preview releases may
require a manual download.

## iOS and Android

Phone clients are in testing. Distribution links will appear in the
[availability guide](https://lyrestudio.net/docs/release-status.html#ios)
when a public or testing channel is available.

## Command-line interface

Install the [Lyre Studio CLI](https://www.npmjs.com/package/@lyrestudio/cli)
with Node.js **22.12 or newer**:

```sh
npm install --global @lyrestudio/cli@beta
lyre --version
lyre --help
```

To select this release explicitly, install
`@lyrestudio/cli@0.11.0-beta.3`. The npm CLI and desktop app have separate
version numbers; this CLI accompanies desktop **0.1.6**. The `lyre-foundation` and
`paseo` executable aliases remain available.

For a standalone host:

```sh
lyre daemon start
lyre status
lyre daemon stop
```

Repeat the npm install command to update the CLI. Keep your existing Lyre profile
and project folders. Use `lyre --help` for commands and the
[provider guide](https://lyrestudio.net/docs/providers.html) for account setup.

The initial npm release is verified on **Windows x64 with Node.js 24**, including
the Windows image-input and process helpers. macOS native helpers and installed
macOS/Linux qualification are pending.
Keep custom daemon home paths short: the Windows image-file helper does not
support full image paths of 260 characters or more.

## Your first project

Open a project folder in Lyre, connect a coding provider or local model, and set up
the project's preview command. Your host needs the dependencies and development
tools that the project uses. Local-model hardware requirements depend on the model
and model runner you choose.

Local projects and local-network workflows work without a Lyre cloud account.
Keep your host awake and connected when accessing it from another device.
[Follow the setup guide](https://lyrestudio.net/docs/quickstart.html).

## Updating

**macOS, Windows installer, and Linux AppImage:** builds with updates enabled check the
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
`arm64` identifies the Apple silicon Mac build.

Use the release's labeled download links. The **.yml** and **.blockmap** files are
for the updater. GitHub's **Source code (zip/tar.gz)** links contain this public
repository's documentation, not the Lyre application.

**SHA256SUMS.txt** covers the Windows and Linux packages.
**SHA256SUMS-macos.txt** covers the Mac packages. Use the manifest attached to the
same release as your download. To compare a saved file against its entry, use
PowerShell's `Get-FileHash -Algorithm SHA256` on Windows, `shasum -a 256` on
macOS, or `sha256sum` on Linux. Matching a checksum confirms the download's
bytes match the published value; it does not replace platform signing checks.

[Report an installation problem](https://github.com/LyreStudio/lyre-releases/issues/new?template=bug_report.yml).
