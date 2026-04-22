# Engram vs Stargate Wallet: Why Dero Users Are Switching

Stargate was the previous generation of Dero GUI wallet. It served the community well, but active maintenance has moved to [Engram Wallet](https://engramwallet.com/), the current official desktop client. If you are still running Stargate, this is your migration path. The live comparison lives at [engramwallet.com/guides/engram-vs-stargate-wallet](https://engramwallet.com/guides/engram-vs-stargate-wallet).

## At a glance

| Feature | Stargate | Engram |
| --- | --- | --- |
| Maintained by the Dero Foundation | Legacy | Actively maintained |
| AES-256 local key encryption | Yes | Yes |
| Native support for current Dero RPC | Partial | Full |
| Modern desktop UI (Fyne) | No | Yes |
| Cyberdeck secure RPC for dApps | No | Yes |
| Integrated messaging and services | No | Yes |

Engram is not a rebranded Stargate — it is a ground-up rewrite in pure Go, released as the new flagship for the [Dero Network](https://engramwallet.com/dero-coin).

## Why the switch happened

Stargate's codebase predates several Dero protocol upgrades. Keeping it current meant porting each upgrade twice — once into the Dero chain, once into the wallet — which eventually became impractical. The Dero Foundation consolidated on Engram for three reasons:

1. **Single-language stack.** Both the chain and Engram are written in Go. Protocol changes reach the wallet in days, not months. See the [about page](https://engramwallet.com/about).
2. **Modern UI toolkit.** Engram uses Fyne for a consistent look across Windows, macOS and Linux. The [official Dero wallet page](https://engramwallet.com/dero-wallet) shows the new interface.
3. **Expanded feature set.** Engram ships modules Stargate never had: [Cyberdeck RPC, Messages, Services, Asset Explorer](https://engramwallet.com/documentation).

## Security parity and where Engram goes further

Both wallets use AES-256 encrypted local wallet files. Both are non-custodial. Engram adds:

- A stricter distribution channel — official builds only from [engramwallet.com/download](https://engramwallet.com/download).
- Published checksums and signed installers for [Windows](https://engramwallet.com/download/windows), [macOS](https://engramwallet.com/download/mac) and [Linux](https://engramwallet.com/download/linux).
- A well-documented [security architecture](https://engramwallet.com/security) and a [scam and safety check](https://engramwallet.com/is-engram-wallet-safe).

## How to migrate

Your seed phrase is portable. Moving from Stargate to Engram is a one-time restore:

1. **Back up Stargate.** Export the seed phrase from Stargate's account menu. Keep it offline. See the [backup principles](https://engramwallet.com/guides/backup-engram-wallet).
2. **Install Engram.** Grab the installer from the [download page](https://engramwallet.com/download) and follow the [install guide](https://engramwallet.com/guides/install-engram-wallet).
3. **Restore with the seed.** Launch Engram, choose **Restore wallet**, enter the phrase. The [restore guide](https://engramwallet.com/guides/restore-engram-wallet) shows every screen.
4. **Confirm balance.** Wait for the chain rescan. Check that the balance matches what Stargate showed.
5. **Retire Stargate.** Uninstall it after a week, once you are confident Engram is stable.

## What you gain after migrating

- **Cyberdeck.** Serve a secure RPC endpoint for dApps and local tooling.
- **Messages.** Send 128-byte encrypted messages on-chain.
- **Services.** Built-in payment IDs for point-of-sale flows.
- **Asset Explorer.** Browse Dero smart contracts trustlessly via Gnomon.
- **Datapad.** Store sensitive notes in an encrypted local pad.

The full module tour is on the [documentation page](https://engramwallet.com/documentation) and in the in-depth [review](https://engramwallet.com/reviews/engram-wallet).

## Is Engram safe?

Yes. Engram is the official Dero wallet. It is built by the Dero Foundation, open source, and distributed only from the [official channels](https://engramwallet.com/download). The full due-diligence write-up is on the [safety check page](https://engramwallet.com/is-engram-wallet-safe). If you are moving from an exchange rather than Stargate, the [DERO coin guide](https://engramwallet.com/dero-coin) and the [self-custody walkthrough](12-exchanges-to-self-custody.md) cover the extra steps.

## Common questions

**Do I need a new seed phrase after migrating?**
No. Your Stargate seed phrase continues to control the same Dero account.

**Can I run Stargate and Engram side by side?**
Temporarily, yes. Long term, consolidate on Engram since Stargate no longer receives protocol updates. The [guides index](https://engramwallet.com/guides) has the full post-migration checklist.

**What about developers?**
If you scripted against Stargate's RPC, the new Cyberdeck module has a more flexible API. Compare it against the terminal workflow in [Engram vs the Dero CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet).

## Related articles

- [Engram Wallet: The Complete Guide](01-engram-wallet-complete-guide.md)
- [Engram vs the Dero CLI Wallet](07-engram-vs-cli-wallet.md)
- [Backup and Restore the Engram Wallet](05-backup-restore-engram-wallet.md)
- [Inside the Eight Engram Modules](10-engram-wallet-modules.md)
