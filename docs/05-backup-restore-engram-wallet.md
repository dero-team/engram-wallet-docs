# Backup and Restore the Engram Wallet (Step-by-Step)

Backup and recovery are the two steps most self-custody users skip — right until they need them. This article walks through both, using [Engram Wallet](https://engramwallet.com/) on Windows, macOS and Linux. The official, live references are the [backup guide](https://engramwallet.com/guides/backup-engram-wallet) and the [restore guide](https://engramwallet.com/guides/restore-engram-wallet).

## What you need to back up

Two independent artefacts can recover an Engram wallet:

1. **The seed phrase.** Generated once, when the wallet is created. It is the master secret.
2. **The Datashard backup file.** An encrypted copy of the wallet database, exportable from the **My Account** module. The Datashard is protected with your wallet password and can restore account metadata (names, balances history, messages) that a bare seed cannot.

Keep both. If you only keep the seed, you can still recover funds, but you lose local metadata. If you only keep the Datashard, you are dependent on a single encrypted file.

## Back up with the seed phrase

1. Open Engram and unlock the wallet with your password.
2. Open **My Account** and choose **View Seed Phrase**.
3. Re-enter the wallet password to confirm.
4. Write the phrase on paper. Do not screenshot. Do not email. Do not type it into cloud notes.
5. Store the paper in at least two physical locations that are not both your home office.

The [security architecture](https://engramwallet.com/security) and the [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe) page document why the seed phrase must stay offline.

## Back up with a Datashard

1. Open **My Account** and choose **Export Datashard**.
2. Save the file to an external location — an encrypted USB drive is ideal.
3. Make at least one additional copy on a second medium.
4. Store the Datashard separately from your seed phrase.

The official [backup guide](https://engramwallet.com/guides/backup-engram-wallet) includes screenshots for every step.

## Where not to store your backups

- Cloud drives (Dropbox, iCloud, Google Drive) — unless the backup is wrapped in a second layer of encryption and the password is separate.
- Email drafts and inboxes.
- Password managers that sync without end-to-end encryption.
- Photographs or screenshots on your phone.

These are the common failure modes. The [safety check](https://engramwallet.com/is-engram-wallet-safe) and the [official Dero wallet page](https://engramwallet.com/dero-wallet) explain why each route leaks funds.

## Restore from seed phrase

If your device fails, your wallet is deleted, or you migrate to a new machine, restore is straightforward:

1. Install Engram on the new device using the [install guide](https://engramwallet.com/guides/install-engram-wallet) — download links are on the [Windows](https://engramwallet.com/download/windows), [macOS](https://engramwallet.com/download/mac) and [Linux](https://engramwallet.com/download/linux) pages of [engramwallet.com/download](https://engramwallet.com/download).
2. Choose **Restore wallet**.
3. Enter your seed phrase in order, exactly as recorded.
4. Set a fresh wallet password. This password encrypts the new local wallet file with AES-256.
5. Wait while Engram rescans the chain.

## Restore from a Datashard

1. Install Engram (see above).
2. Choose **Import Datashard**.
3. Point the dialog to your saved backup file.
4. Enter the wallet password that protected the Datashard.
5. The wallet reopens with metadata intact.

The [restore guide](https://engramwallet.com/guides/restore-engram-wallet) is the step-by-step reference.

## Dry-run: test your backup before you need it

Never trust a backup you have not tested. Run this dry-run every few months:

1. On a secondary machine, install Engram from the [guides index](https://engramwallet.com/guides).
2. Restore using the seed phrase.
3. Confirm that the first receive address matches the original.
4. Delete the test wallet file (not the seed phrase).

If the addresses match, your seed copy is correct. If they do not, re-record the phrase now — not after a disk failure.

## Platform-specific notes

- **Windows.** Store the seed phrase off-line and never place it in OneDrive. See the [Windows install guide](https://engramwallet.com/download/windows).
- **macOS.** Time Machine will capture the wallet file if it lives in your home folder. Exclude the wallet directory, or rely on explicit Datashard exports. The [macOS download page](https://engramwallet.com/download/mac) has the current path.
- **Linux.** Back up the wallet directory with `tar` and encrypt the archive with GPG before copying it anywhere. Details on the [Linux download page](https://engramwallet.com/download/linux).

## If you lose your seed phrase

If you lose the phrase and the Datashard password, the funds are unrecoverable — including by the Dero Foundation. This is the direct consequence of self-custody. The [FAQ](https://engramwallet.com/#faq), the [DERO coin page](https://engramwallet.com/dero-coin), and the [review](https://engramwallet.com/reviews/engram-wallet) all explain why there is no admin override.

## Migration scenarios

- **Old machine to new machine.** Restore from seed or Datashard.
- **Stargate to Engram.** Follow the migration in [Engram vs Stargate](https://engramwallet.com/guides/engram-vs-stargate-wallet).
- **CLI wallet to Engram.** Follow the migration in [Engram vs the Dero CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet).
- **Exchange to Engram.** Walk through the [DERO coin guide](https://engramwallet.com/dero-coin) and the [official Dero wallet page](https://engramwallet.com/dero-wallet).

## Related articles

- [Engram Wallet Security Architecture](04-engram-wallet-security-architecture.md)
- [How to Download and Install Engram Wallet](02-download-install-engram-wallet.md)
- [Moving from Exchanges to Self-Custody](12-exchanges-to-self-custody.md)
- [Is Engram Wallet Safe and Legit?](08-is-engram-wallet-safe-2026.md)
