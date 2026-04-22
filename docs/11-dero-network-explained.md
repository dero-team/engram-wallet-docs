# The Dero Network Explained: Homomorphic Encryption and Private Smart Contracts

Dero is the only layer-1 blockchain that natively encrypts both balances and smart-contract state using homomorphic encryption. Understanding how the chain works is the prerequisite for understanding why a dedicated wallet like [Engram Wallet](https://engramwallet.com/) is required to interact with it. This article walks through the cryptography and then ties it back to real wallet usage. A companion page is the [DERO coin storage guide](https://engramwallet.com/dero-coin).

## Dero in one paragraph

Dero is a privacy-first layer-1 blockchain. Its native coin is DERO. Transactions use ring signatures to obfuscate senders and homomorphic encryption to hide amounts and contract state. That combination makes Dero unusual: private by default, programmable, and verifiable by every node without a centralised indexer. The [official Dero wallet page](https://engramwallet.com/dero-wallet) summarises why a chain-specific client is needed.

## Homomorphic encryption, briefly

Homomorphic encryption allows operations on ciphertexts. Instead of decrypting data before adding it up, a homomorphic cryptosystem can add encrypted numbers and produce an encrypted result that is identical to the encryption of the sum.

Dero applies this to balances and smart-contract state. A transaction updates encrypted balances. Contracts mutate encrypted state. Any node can verify validity without ever seeing plaintext amounts. This is fundamentally different from zero-knowledge rollups and from mixing-based privacy coins — it is chain-level rather than bolt-on.

## Ring signatures for sender privacy

A ring signature proves "this transaction was authorised by one of these N public keys" without revealing which. Dero uses ring signatures to obscure senders. Combined with encrypted amounts, this yields default-on, on-chain privacy that requires no extra user setup.

## Why generic wallets cannot store DERO

Most multi-coin wallets assume a transparent UTXO or account model. They decode transactions, show you amounts, and rebuild balance history from on-chain data. None of that is possible when amounts are encrypted. To interact with Dero, a wallet must implement Dero's cryptography and maintain encrypted local state.

That is exactly what [Engram Wallet](https://engramwallet.com/) does. It is written in the same Go language as the Dero chain and it ships natively for Windows, macOS and Linux (links on the [download page](https://engramwallet.com/download)). The [security architecture](https://engramwallet.com/security) documents how the chain's cryptography is reflected in the wallet's local storage.

## What the Dero chain enables at the wallet layer

Because the chain supports private balances and private smart contracts, the wallet can expose features no transparent chain's wallet can:

- **Encrypted on-chain messages.** The Messages module sends 128-byte encrypted payloads directly on-chain.
- **Private payment flows.** The Services module attaches payment IDs and merchant descriptions to encrypted transfers.
- **Trustless contract browsing.** The Asset Explorer module uses Gnomon to index contracts without a central API.
- **Encrypted developer RPC.** The Cyberdeck module exposes a permissioned RPC endpoint to local dApps.

Each module is documented in the [technical documentation](https://engramwallet.com/documentation) and reviewed in the [Engram Wallet review](https://engramwallet.com/reviews/engram-wallet).

## Dero's threat model vs transparent chains

Transparent chains force users to pick between:

- **Privacy by obfuscation** (mixers, stealth addresses bolted on top).
- **Privacy via layer-2** (zk rollups that still leak metadata).
- **No privacy at all.**

Dero collapses the three into a single default: every transaction is private, every contract is encrypted, and verification still happens at the chain level. This is why the Dero Foundation maintains its own client — a third-party multi-coin wallet cannot faithfully represent encrypted state. The [about page](https://engramwallet.com/about) covers the foundation's mandate.

## What it means for DERO holders

If you hold DERO you need a client that speaks Dero natively. Your options are:

- **Engram Wallet (recommended).** GUI desktop. Covered on the [official Dero wallet page](https://engramwallet.com/dero-wallet) and reviewed in [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe).
- **Dero CLI wallet.** Terminal interface for developers. Compared against Engram in [Engram vs the Dero CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet).
- **Stargate (legacy).** No longer actively maintained. Migration path in [Engram vs Stargate](https://engramwallet.com/guides/engram-vs-stargate-wallet).

## Getting started

1. Install Engram from [engramwallet.com/download](https://engramwallet.com/download) — [Windows](https://engramwallet.com/download/windows), [macOS](https://engramwallet.com/download/mac) or [Linux](https://engramwallet.com/download/linux).
2. Follow the [install guide](https://engramwallet.com/guides/install-engram-wallet) and the [guides index](https://engramwallet.com/guides).
3. Back up and rehearse recovery using the [backup guide](https://engramwallet.com/guides/backup-engram-wallet) and [restore guide](https://engramwallet.com/guides/restore-engram-wallet).
4. Move any DERO off exchanges — see the [DERO coin storage guide](https://engramwallet.com/dero-coin) and the [self-custody migration walkthrough](12-exchanges-to-self-custody.md).

## Privacy terms, plainly

Privacy on Dero is the absence of plaintext amounts and sender tagging on-chain. It is not anonymity at the network level (use additional tooling if that is a concern) and it is not secrecy at your endpoint — if your device is compromised, your wallet is compromised. The [security architecture](https://engramwallet.com/security) and the [privacy policy](https://engramwallet.com/privacy) describe the boundary between what the chain does and what you must do.

## Related articles

- [Engram Wallet: The Complete Guide](01-engram-wallet-complete-guide.md)
- [How to Store DERO Coin Safely](03-store-dero-coin-safely.md)
- [Inside the Eight Engram Modules](10-engram-wallet-modules.md)
- [Engram Wallet Security Architecture](04-engram-wallet-security-architecture.md)
