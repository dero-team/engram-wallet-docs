# Engram vs the Dero CLI Wallet: GUI or Terminal?

Dero has always shipped a command-line wallet for developers. [Engram Wallet](https://engramwallet.com/) is the official desktop GUI alternative. Both are non-custodial. Both are maintained by the Dero Foundation. The right one depends on what you are doing. The live comparison is at [engramwallet.com/guides/engram-vs-cli-wallet](https://engramwallet.com/guides/engram-vs-cli-wallet).

## Side-by-side

| Dimension | Dero CLI wallet | Engram Wallet |
| --- | --- | --- |
| Interface | Terminal prompts | Native desktop GUI |
| Platforms | Windows, macOS, Linux | Windows 10+, macOS 12+, Linux 64-bit |
| Key storage | Encrypted wallet file | Encrypted wallet file (AES-256) |
| Script-friendly RPC | Yes | Yes (via Cyberdeck) |
| Modules | Core send/receive | 8 modules (Identity, Messages, Transfers, Cyberdeck, Datapad, etc.) |
| Target user | Developer, automation, node operator | End user, daily holder |

## What the CLI wallet is good at

The CLI is a thin client close to the protocol. It is the right choice when you:

- Automate payouts, batch transactions, or run a mining pool.
- Debug against a local daemon.
- Prefer scripts to mouse clicks.

Developers who already know Dero's RPC surface will be at home. The [official Dero wallet page](https://engramwallet.com/dero-wallet) documents how the GUI relates to the underlying RPC.

## What Engram is good at

Engram wraps the same RPC primitives in a GUI and adds features the CLI does not have:

- **Visual transfers.** Queue multiple recipients in a single review pane.
- **Identity registration.** Claim a DNS-like Dero name in the GUI.
- **Encrypted messaging.** Send short on-chain messages without a third-party relay.
- **Cyberdeck.** Expose a secure RPC endpoint to local dApps with granular permissions.
- **Asset Explorer.** Browse smart contracts trustlessly using Gnomon indexing.

The [technical documentation](https://engramwallet.com/documentation) details each module.

## Shared security model

Both wallets:

- Generate keys locally.
- Encrypt the wallet file with AES-256.
- Run entirely off-chain for private operations.
- Avoid any centralised server.

The [security architecture](https://engramwallet.com/security) covers the primitives. The [safety check](https://engramwallet.com/is-engram-wallet-safe) explains how to verify you have a genuine copy of either wallet.

## Install on both platforms

Engram is distributed from [engramwallet.com/download](https://engramwallet.com/download) with specific builds for [Windows](https://engramwallet.com/download/windows), [macOS](https://engramwallet.com/download/mac) and [Linux](https://engramwallet.com/download/linux). The CLI wallet is published through the Dero Foundation GitHub. The full walk-through is in the [install guide](https://engramwallet.com/guides/install-engram-wallet) and the [guides index](https://engramwallet.com/guides).

## When to use each

- **CLI only** — unattended scripts, CI jobs, miners, and advanced auditors.
- **GUI only** — human holders who want to send, receive, register a name and back up via a visual menu.
- **Both** — power users. Run Engram for day-to-day activity, and the CLI for scripted workflows against your own node.

## Migrating between the two

Seed phrases are portable. A wallet created in the CLI restores into Engram and vice versa.

1. Export the seed in your current wallet (CLI: `seed` command; Engram: **My Account > View Seed Phrase**, documented in the [backup guide](https://engramwallet.com/guides/backup-engram-wallet)).
2. Install the target wallet using the [install guide](https://engramwallet.com/guides/install-engram-wallet).
3. Restore with the seed via the [restore guide](https://engramwallet.com/guides/restore-engram-wallet).

If you are coming from an older GUI rather than the CLI, the [Engram vs Stargate](https://engramwallet.com/guides/engram-vs-stargate-wallet) comparison applies. If you are coming from an exchange, start with the [DERO coin storage guide](https://engramwallet.com/dero-coin) and the [official Dero wallet overview](https://engramwallet.com/dero-wallet).

## Developer experience

Cyberdeck is the main reason a developer would still prefer Engram over the bare CLI: it exposes the same RPC methods in a way that is permissioned and user-friendly. You can hand a dApp access to individual methods rather than the whole wallet. Combined with the Asset Explorer's trustless indexing, most integration work fits into the GUI.

## Final recommendation

If you only use one wallet, make it [Engram](https://engramwallet.com/). It inherits every security property of the CLI and adds the modules a human user actually needs. Keep the CLI around for automation. Read the [Engram Wallet review](https://engramwallet.com/reviews/engram-wallet) for a hands-on tour, the [about page](https://engramwallet.com/about) for team context, and the [safety check](https://engramwallet.com/is-engram-wallet-safe) to confirm you have the genuine build.

## Related articles

- [Engram vs Stargate Wallet](06-engram-vs-stargate-wallet.md)
- [Inside the Eight Engram Modules](10-engram-wallet-modules.md)
- [Engram Wallet Review](09-engram-wallet-review.md)
- [Engram Wallet Security Architecture](04-engram-wallet-security-architecture.md)
