---
title: Installing Draftline
description: Which package to take on Windows, macOS and Linux, and how updates work.
published: true
date: 2026-09-18T00:00:00.000Z
tags: getting-started, install
editor: markdown
dateCreated: 2026-09-18T00:00:00.000Z
---

# Installing Draftline

Every release carries packages for all three platforms, with checksums.

## Windows

Take **`Draftline-<version>-windows-amd64-setup.exe`** — an installer that
puts Draftline in Program Files, adds Start Menu and desktop shortcuts,
registers `.draftline` files so you can double-click them, and installs the
WebView2 runtime if your machine does not have it.

If you would rather not install anything, **`-windows-amd64-portable.zip`**
is the bare program. It runs from anywhere, including a USB stick, and
registers file associations for your user on first launch.

## macOS

**`Draftline-<version>-macos-universal.dmg`**, for both Intel and Apple
Silicon. Open it and drag Draftline to Applications.

Unless the build was signed with a Developer ID, macOS will say it cannot
check the app for malicious software. Right-click Draftline in Applications
and choose **Open**, then confirm — after that it launches normally.

## Linux

Which package depends on your distribution rather than your preference:

| | |
|---|---|
| **`.deb`** | Debian, Ubuntu 22.04+, Mint, Pop!_OS — `sudo apt install ./Draftline-*.deb` |
| **`.rpm`** | Fedora 36+, RHEL 9+, openSUSE — `sudo dnf install ./Draftline-*.rpm` |
| **`.AppImage`** | Arch, Alpine, NixOS and anything else with WebKitGTK 4.1 |

Take the `.deb` or `.rpm` where you can. They pull in their own dependencies
and register the desktop entry, the icon and the `.draftline` association
system-wide; the AppImage registers nothing.

The AppImage does not start on Ubuntu 22.04. On Debian and Ubuntu family take
the `.deb`; on Red Hat family take the `.rpm`.

## Updates

Draftline checks for a new version on its own and tells you when one exists.
Nothing downloads until you say so, and what it downloads is verified against
the release checksum before it opens — a package that does not match is
discarded rather than run.

The check reports the version only. It sends nothing about you or your books.

## Verifying a download

Every release includes `SHA256SUMS.txt`. To check a file by hand:

```
# Windows PowerShell
Get-FileHash .\Draftline-*-windows-amd64-setup.exe -Algorithm SHA256

# macOS and Linux
shasum -a 256 Draftline-*
```

Compare the result with the line for that file in `SHA256SUMS.txt`.
