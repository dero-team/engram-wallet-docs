# How to Download and Install Engram Wallet on Windows, macOS and Linux

[Engram Wallet](https://engramwallet.com/) is the official Dero desktop wallet. It is free, open source and published for three operating systems. This walkthrough covers the download link you should trust, the install steps for each platform, and the first-run checklist.

## Where to download Engram Wallet

Only two sources are considered genuine:

1. The official website — [engramwallet.com/download](https://engramwallet.com/download).
2. The Dero Foundation's GitHub releases.

Do not trust installers from unofficial mirrors, Telegram bots, Discord attachments, or app stores. The [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe) page explains the signs of a phishing copy and how to verify the installer against the published checksum.

## System requirements

| Platform | Minimum version | Notes |
| --- | --- | --- |
| Windows | Windows 10 (64-bit) | [Download for Windows](https://engramwallet.com/download/windows) |
| macOS | macOS 12 (Monterey) | [Download for macOS](https://engramwallet.com/download/mac) |
| Linux | Modern 64-bit distro | [Download for Linux](https://engramwallet.com/download/linux) |

Engram is a native desktop app, not a browser extension or a web wallet. You do not need a Node.js or Python runtime, and you do not need to compile anything from source unless you want to.

## Install on Windows

1. Open [engramwallet.com/download/windows](https://engramwallet.com/download/windows) and download the signed installer.
2. Double-click the `.exe` file. If Windows SmartScreen prompts you, click **More info > Run anyway** — this is expected for new signing certificates and is documented in the [safety guide](https://engramwallet.com/is-engram-wallet-safe).
3. Follow the install prompts. The default location is fine.
4. Launch Engram from the Start menu and continue with the [new wallet tutorial in the guides index](https://engramwallet.com/guides).

## Install on macOS

1. Download the `.dmg` from [engramwallet.com/download/mac](https://engramwallet.com/download/mac).
2. Double-click the disk image and drag **Engram** into your Applications folder.
3. The first launch uses Gatekeeper. If macOS says the app is from an unidentified developer, right-click the app, choose **Open**, and confirm.
4. Create a new wallet or restore an existing one using the [restore guide](https://engramwallet.com/guides/restore-engram-wallet).

## Install on Linux

1. Grab the Linux build from [engramwallet.com/download/linux](https://engramwallet.com/download/linux). Binaries are packaged for modern 64-bit distributions.
2. Make the file executable: `chmod +x engram-linux-amd64`.
3. Run it from a terminal or double-click from your file manager.
4. Pair with the [install guide](https://engramwallet.com/guides/install-engram-wallet) for a screenshot-by-screenshot walkthrough.

## First-run checklist

After the app starts for the first time:

1. Create a new wallet. Engram generates a fresh seed and encrypts it with AES-256 using a password you choose.
2. Write the seed phrase on paper. Do not screenshot, do not email, do not cloud-back it up.
3. Store the paper offline in at least two physical locations.
4. Immediately follow the [backup guide](https://engramwallet.com/guides/backup-engram-wallet) to export a Datashard file.
5. Practice a dry-run recovery with the [restore guide](https://engramwallet.com/guides/restore-engram-wallet) on a throwaway wallet to confirm your seed phrase works.

## Verify you have the genuine build

Every release publishes a checksum. Match the SHA-256 hash of your download to the value listed on [engramwallet.com/download](https://engramwallet.com/download). If the hashes differ, delete the file and retry. The [security architecture page](https://engramwallet.com/security) and the [safety check](https://engramwallet.com/is-engram-wallet-safe) detail signing keys and distribution policy.

## Why install Engram at all?

If you hold DERO and are still relying on a centralized exchange, a browser wallet, or the terminal-only Dero CLI, moving to Engram fixes three common pain points: self-custody, usability and ongoing maintenance. Read the comparison articles for specifics:

- [Engram vs Stargate Wallet](https://engramwallet.com/guides/engram-vs-stargate-wallet) — for Stargate users.
- [Engram vs the Dero CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet) — for CLI users.
- [DERO coin storage](https://engramwallet.com/dero-coin) and the [official Dero wallet page](https://engramwallet.com/dero-wallet) — for exchange users.

## Troubleshooting quick hits

- **Antivirus flags the installer.** Crypto wallets are occasionally false-positives. Verify the checksum on the [official download page](https://engramwallet.com/download) and whitelist only that binary.
- **App won't launch on macOS.** Check the [safety review](https://engramwallet.com/is-engram-wallet-safe) for the Gatekeeper exception steps.
- **Stuck in onboarding.** The [guides index](https://engramwallet.com/guides) has individual guides for install, backup and restore.

## Related articles

- [Engram Wallet: The Complete Guide](01-engram-wallet-complete-guide.md)
- [Engram Wallet Security Architecture](04-engram-wallet-security-architecture.md)
- [Backup and Restore the Engram Wallet](05-backup-restore-engram-wallet.md)
- [Moving from Exchanges to Self-Custody with Engram Wallet](12-exchanges-to-self-custody.md)
