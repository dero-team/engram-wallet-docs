# Engram Wallet Review: Hands-On with the Official Dero Desktop Wallet

[Engram Wallet](https://engramwallet.com/) is the Dero Network's official non-custodial desktop client. After installing it on Windows, macOS and Linux and using each of its eight modules, this review covers what the wallet gets right, where it needs care from the user, and who it is the best fit for. The live, maintained review is at [engramwallet.com/reviews/engram-wallet](https://engramwallet.com/reviews/engram-wallet).

## The short verdict

Engram is the wallet to use if you hold DERO. It is the only actively maintained GUI from the Dero Foundation, it ships features no other client has (Cyberdeck, Asset Explorer, on-chain Messages), and the security model is straightforward: keys are generated locally and protected with AES-256. For a plain-text safety check, read [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe).

## First impressions

Installation is standard across platforms. Builds for [Windows](https://engramwallet.com/download/windows), [macOS](https://engramwallet.com/download/mac) and [Linux](https://engramwallet.com/download/linux) are all published on [engramwallet.com/download](https://engramwallet.com/download). The [install guide](https://engramwallet.com/guides/install-engram-wallet) is short; the onboarding asks for a wallet name, a password, and shows the seed phrase.

The UI is clean and keyboard-friendly. Fyne rendering looks identical across platforms, which matters when you are walking friends through recovery on a different OS.

## Security posture

Engram scores well on the four core questions any wallet review should answer:

1. **Custody model.** Non-custodial. Keys never leave the device. See the [security page](https://engramwallet.com/security).
2. **Encryption.** Local wallet files are encrypted with AES-256, gated by a user password.
3. **Telemetry.** None. No analytics, no accounts, no emails collected — confirmed by the [privacy policy](https://engramwallet.com/privacy).
4. **Distribution.** Signed builds shipped from [engramwallet.com](https://engramwallet.com/) and Dero Foundation GitHub only. Fake sites are addressed in the [safety check](https://engramwallet.com/is-engram-wallet-safe).

## The eight modules in practice

Engram organises features into eight modules, each accessible from the main nav.

- **Identity.** Register a Dero name as a DNS-like alias for your address. Good for repeated recipients.
- **My Account.** Seed phrase viewing, Datashard backup, password change. This is where you run the [backup guide](https://engramwallet.com/guides/backup-engram-wallet).
- **Messages.** Encrypted 128-byte payloads sent on-chain without a relay server.
- **Transfers.** Queued multi-address transactions with a batch signing step.
- **Asset Explorer.** Trustless smart contract and token browser using Gnomon indexing.
- **Services.** Payment IDs and merchant descriptions for point-of-sale flows.
- **Cyberdeck.** Secure RPC endpoint for local dApps, with per-method permissions.
- **Datapad.** Encrypted notes stored inside the wallet — handy for API keys and contract addresses.

A deeper per-module breakdown lives in the [technical documentation](https://engramwallet.com/documentation).

## Who it is for

Engram is the right wallet for:

- **DERO holders** who need a visual client on a desktop they control.
- **Developers** who prefer Cyberdeck's permissioned RPC over running raw `dero-wallet-cli` — see [Engram vs the CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet).
- **Former Stargate users** who need the migration path in [Engram vs Stargate](https://engramwallet.com/guides/engram-vs-stargate-wallet).
- **Exchange users** moving to self-custody — follow the [DERO coin guide](https://engramwallet.com/dero-coin) and the [self-custody migration walkthrough](12-exchanges-to-self-custody.md).

## Things that require user discipline

Engram does not and cannot protect against lost seed phrases. You have to:

- Write your seed phrase on paper and store it offline.
- Export a Datashard backup using the [backup guide](https://engramwallet.com/guides/backup-engram-wallet).
- Test recovery before you need it with the [restore guide](https://engramwallet.com/guides/restore-engram-wallet).
- Download only from [engramwallet.com/download](https://engramwallet.com/download).

## Performance and cross-platform parity

Chain rescans after a fresh install are the slowest operation. On Linux and macOS the app is snappy; on Windows, first launch occasionally prompts SmartScreen, which the [safety check](https://engramwallet.com/is-engram-wallet-safe) addresses. Long-running sessions sit idle without leaking memory. The underlying Go runtime has been stable across tests.

## What Engram does not have

- A mobile app — this is desktop-only. The [about page](https://engramwallet.com/about) explains the rationale.
- Third-party coin support. Engram is a dedicated Dero client by design.
- Custodial or cloud-sync features. That is the whole point.

## Final take

If you hold DERO, install Engram. The wallet gives you every primitive you need — encrypted backup, identity registration, encrypted messaging, merchant tooling, developer RPC — without asking for anything in return. Start with the [homepage](https://engramwallet.com/), move through the [guides index](https://engramwallet.com/guides), and confirm you downloaded the genuine build via [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe).

## Related articles

- [Engram Wallet: The Complete Guide](01-engram-wallet-complete-guide.md)
- [Engram Wallet Security Architecture](04-engram-wallet-security-architecture.md)
- [Inside the Eight Engram Modules](10-engram-wallet-modules.md)
- [Engram vs the Dero CLI Wallet](07-engram-vs-cli-wallet.md)
