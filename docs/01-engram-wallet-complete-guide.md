# Engram Wallet: The Complete Guide to the Official Non-Custodial Dero Wallet

[Engram Wallet](https://engramwallet.com/) is the official desktop wallet for the Dero Network. It is non-custodial, AES-256 encrypted, and free to download for Windows, macOS and Linux. This guide covers what the wallet is, who builds it, what it can do, and how to get started.

## What is Engram Wallet?

Engram is a native desktop cryptocurrency wallet developed by the Dero Foundation. It is the flagship client of the Dero Network — a privacy-first layer-1 blockchain with the world's first fully encrypted smart contracts. Every private key is generated locally and encrypted with AES-256 before it ever touches disk. Keys never sync to a server. No account is created, no email is collected, no identity check is performed.

If you are evaluating wallets for DERO, start with the [official Dero wallet page](https://engramwallet.com/dero-wallet) and the [Engram Wallet homepage](https://engramwallet.com/). The [about page](https://engramwallet.com/about) covers the project's history and the team behind it.

## Who builds Engram

Engram is built in pure Go by the Dero Foundation — the same team that maintains the Dero blockchain itself. Because both the chain and the wallet share a language and a maintainer, new protocol features (ring signatures, homomorphic encryption changes, smart-contract formats) reach Engram quickly. The codebase is open source and has been in active development since 2023.

## Why a dedicated Dero wallet matters

Most "multi-coin" wallets do not natively support Dero. The chain uses encrypted balances, ring signatures for sender obfuscation, and a homomorphic transaction model that general-purpose wallets simply cannot reconstruct. Engram was designed around those primitives from the first line of code, so features such as registered names, the Asset Explorer and Cyberdeck RPC work out of the box. Read the [technical documentation](https://engramwallet.com/documentation) for a feature-by-feature breakdown.

## What you can do inside Engram

Engram ships with eight modules, each covering a common self-custody task:

- **Identity** — register a human-readable name on-chain, similar to a DNS record.
- **My Account** — manage your password, Datashard backups and key protection.
- **Messages** — send encrypted 128-byte messages on-chain without a third-party server.
- **Transfers** — queue and batch multi-address transactions before signing.
- **Asset Explorer** — browse smart contracts and tokens trustlessly via Gnomon indexing.
- **Services** — generate payment IDs and point-of-sale descriptions.
- **Cyberdeck** — expose a secure RPC endpoint for decentralized applications.
- **Datapad** — keep encrypted private notes inside the wallet.

A deeper module-by-module tour lives in the [Engram Wallet review](https://engramwallet.com/reviews/engram-wallet) and in the [technical documentation](https://engramwallet.com/documentation).

## Security model at a glance

- Private keys are generated on-device and encrypted with AES-256.
- The wallet file is password-protected and never uploaded.
- There is no central server, no cloud sync, no account recovery.
- The project ships with no telemetry.

The [security architecture page](https://engramwallet.com/security) documents the cryptographic primitives, the wallet file format, and the threat model in detail. If you have seen phishing copies or fake installers and want to verify you have the real software, the [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe) checklist explains how to confirm you are downloading the genuine release.

## Supported platforms

Engram is a native application, not a browser extension. It runs on:

- Windows 10 or later — [Windows installer](https://engramwallet.com/download/windows)
- macOS 12 or later — [macOS installer](https://engramwallet.com/download/mac)
- 64-bit Linux distributions — [Linux build](https://engramwallet.com/download/linux)

All builds are published on the [main download page](https://engramwallet.com/download). The recommended starting point for a new user is the [guides index](https://engramwallet.com/guides) followed by the [install guide](https://engramwallet.com/guides/install-engram-wallet).

## First steps

1. Download Engram from [engramwallet.com/download](https://engramwallet.com/download).
2. Install it using the [step-by-step install guide](https://engramwallet.com/guides/install-engram-wallet).
3. Create a new wallet, write down your seed phrase, and store it offline.
4. Back up immediately following the [backup guide](https://engramwallet.com/guides/backup-engram-wallet).
5. Practice recovery on a throwaway wallet using the [restore guide](https://engramwallet.com/guides/restore-engram-wallet).

## Engram vs other Dero wallets

If you are coming from another Dero wallet, two comparison pages cover the most common migrations:

- [Engram vs Stargate Wallet](https://engramwallet.com/guides/engram-vs-stargate-wallet) — for users of the older Stargate GUI.
- [Engram vs the Dero CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet) — for developers who still use the terminal client.

If you hold DERO on a centralized exchange, the [DERO coin guide](https://engramwallet.com/dero-coin) explains why self-custody matters and how to move your balance into Engram safely.

## Is Engram Wallet legit?

Yes. Engram is the official Dero wallet. The only genuine distribution sources are [engramwallet.com](https://engramwallet.com/) and the Dero Foundation's GitHub organisation. The wallet is free, open source, and carries no fees or subscriptions. For a full due-diligence write-up, see the [2026 safety review](https://engramwallet.com/is-engram-wallet-safe) and the [long-form Engram Wallet review](https://engramwallet.com/reviews/engram-wallet).

## Related articles

- [How to Download and Install Engram Wallet on Windows, macOS and Linux](02-download-install-engram-wallet.md)
- [Engram Wallet Security Architecture: AES-256 Keys and Self-Custody Explained](04-engram-wallet-security-architecture.md)
- [Inside the Eight Engram Modules](10-engram-wallet-modules.md)
- [The Dero Network Explained](11-dero-network-explained.md)
