# Inside the Eight Engram Modules: Identity, Messages, Cyberdeck and Datapad

One feature that sets [Engram Wallet](https://engramwallet.com/) apart from other crypto desktop wallets is the modular layout. Instead of cramming every feature into a single screen, Engram splits functionality across eight purpose-built modules. This article walks through each, what it does, and how it ties into the Dero Network. The live reference is the [technical documentation](https://engramwallet.com/documentation).

## Why modules matter

A wallet that tries to be a dashboard usually trades off clarity for density. Engram uses modules so that every flow — sending coins, registering a name, exposing an RPC endpoint — has a dedicated surface with only the controls you need. It also means module-level permissions: you can use Identity without ever touching Cyberdeck, and vice versa.

## 1. Identity

The Identity module lets you register a human-readable name on the Dero chain, functioning like a DNS record for your wallet address. Instead of sending funds to a long cryptographic string, a friend can send to `alice` or `shop.example`. Names are an on-chain primitive — they are not hosted anywhere.

Learn more on the [official Dero wallet page](https://engramwallet.com/dero-wallet), where Identity is used to receive DERO without copying raw addresses.

## 2. My Account

My Account is the security surface. It is where you:

- View or re-export the wallet seed phrase.
- Export and import Datashard backups (the [backup guide](https://engramwallet.com/guides/backup-engram-wallet) walks through this).
- Change the wallet password.
- Manage Datashard-level security.

Use this module on day one after installing from the [install guide](https://engramwallet.com/guides/install-engram-wallet).

## 3. Messages

Dero supports encrypted 128-byte messages as part of its transaction format. The Messages module surfaces this capability: you can send short encrypted notes on-chain directly to another registered Dero name or address. There is no relay server — the chain itself is the transport.

Use cases range from sending an invoice note alongside a transfer to signalling payment memos. Pair it with the Transfers module for full merchant-style flows.

## 4. Transfers

Transfers is the sending interface. Highlights:

- Queue multiple recipients in a single batch.
- Review fees and payloads before signing.
- Pair a memo or payment ID with each send.

Every transfer is gated by your wallet password so even a briefly unlocked session cannot silently drain funds. The broader storage model is covered in the [DERO coin guide](https://engramwallet.com/dero-coin) and the [Dero wallet page](https://engramwallet.com/dero-wallet).

## 5. Asset Explorer

Asset Explorer is a trustless browser for Dero smart contracts and tokens. Under the hood it uses Gnomon, the community indexer that derives state directly from the chain without relying on a central API. From a user's perspective, you can:

- Browse tokens and contracts by ID.
- Inspect metadata and on-chain state.
- Verify that a contract behaves as expected before interacting with it.

## 6. Services

Services packages the payment-ID pattern most merchants already need. You can attach a point-of-sale description to an address, generate sharable payment links, and use the wallet as a self-hosted invoicing endpoint. Combined with Messages, this covers a large chunk of the "small business" use cases other wallets outsource to third parties.

## 7. Cyberdeck

Cyberdeck is the developer and power-user module. It exposes a secure RPC endpoint that dApps and scripts can talk to. Unlike running a raw CLI wallet, Cyberdeck adds:

- Per-method permissioning so you can allow `getBalance` without granting `transfer`.
- A permission prompt flow that mirrors modern browser wallet UX.
- Automatic scoping so a rogue dApp cannot silently escalate.

If you used to rely on the terminal client, the [Engram vs the Dero CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet) comparison explains how Cyberdeck replaces most of that workflow.

## 8. Datapad

Datapad is an encrypted notepad inside the wallet. You can store:

- API keys and contract addresses you use often.
- Seed phrase hints (not the phrase itself).
- Notes about addresses and counterparties.

Because Datapad is encrypted with the same AES-256 key derivation as the wallet file, notes are protected at rest by default. The [security architecture](https://engramwallet.com/security) explains the full crypto model.

## Modules and security, together

The modular design is not just a UX choice — it shrinks the attack surface. Users who never open Cyberdeck cannot accidentally authorise a dApp. Users who never open Services cannot be tricked into signing a merchant invoice. Every module has a bounded scope. The [review](https://engramwallet.com/reviews/engram-wallet) and the [safety check](https://engramwallet.com/is-engram-wallet-safe) both treat this as a positive — it is the opposite of a single "sign anything" button.

## Where to go next

- Install Engram from [engramwallet.com/download](https://engramwallet.com/download) — platform pages for [Windows](https://engramwallet.com/download/windows), [macOS](https://engramwallet.com/download/mac), and [Linux](https://engramwallet.com/download/linux).
- Walk through the [install guide](https://engramwallet.com/guides/install-engram-wallet) and the [backup guide](https://engramwallet.com/guides/backup-engram-wallet).
- Learn the chain context in [DERO coin storage](https://engramwallet.com/dero-coin).
- Understand the team behind the wallet on the [about page](https://engramwallet.com/about).
- Catch up on comparisons in [Engram vs Stargate](https://engramwallet.com/guides/engram-vs-stargate-wallet).

## Related articles

- [Engram Wallet: The Complete Guide](01-engram-wallet-complete-guide.md)
- [Engram Wallet Review](09-engram-wallet-review.md)
- [Engram vs the Dero CLI Wallet](07-engram-vs-cli-wallet.md)
- [The Dero Network Explained](11-dero-network-explained.md)
