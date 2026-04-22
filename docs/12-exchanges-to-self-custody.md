# Moving from Exchanges to Self-Custody with Engram Wallet

Leaving DERO on a centralized exchange is holding a claim on the exchange, not the coins. Self-custody with [Engram Wallet](https://engramwallet.com/) moves ownership back to you. This article is the practical migration path: install, back up, withdraw, confirm, clean up. The live reference for the wallet itself is at [engramwallet.com](https://engramwallet.com/).

## Why self-custody

Centralised exchange accounts expose holders to four known failure modes:

1. **Hacks** of custodial hot wallets.
2. **Withdrawal freezes** during regulatory or market events.
3. **Delistings** that force rushed moves.
4. **Insolvency** that turns coins into bankruptcy claims.

Self-custody removes every one of them. The trade-off is you are now responsible for your seed phrase. Read the [security architecture](https://engramwallet.com/security) and the [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe) page for a full write-up of the threat model.

## Why Engram specifically

Because DERO uses ring signatures and homomorphic encryption, a generic multi-coin wallet cannot decode balances or represent state. You need a client built for Dero — see the reasoning in [the Dero Network explained](11-dero-network-explained.md). The [official Dero wallet page](https://engramwallet.com/dero-wallet) lists every option; Engram is the Dero Foundation's recommended choice.

## Pre-migration checklist

Before touching the exchange withdrawal flow, make sure you have:

- A clean, trusted computer — no unknown browser extensions, no pirated software.
- Paper and a pen for the seed phrase (not a phone screenshot, not a cloud note).
- An encrypted USB drive or similar offline medium for the Datashard backup.

Do not rush. You can always run a small test transfer first.

## Step 1 — Install Engram

Download the installer from [engramwallet.com/download](https://engramwallet.com/download). The platform-specific pages are [Windows](https://engramwallet.com/download/windows), [macOS](https://engramwallet.com/download/mac) and [Linux](https://engramwallet.com/download/linux). Run the installer and follow the [official install guide](https://engramwallet.com/guides/install-engram-wallet).

## Step 2 — Create a wallet

1. Launch Engram.
2. Choose **Create new wallet**.
3. Pick a strong, unique password. This password, together with AES-256, protects the wallet file at rest.
4. Engram displays the seed phrase. Write it on paper. Store at least two copies in separate physical locations.
5. Confirm the phrase.

## Step 3 — Back up before you deposit

Most users wait until "after they have something to back up" — by which time their funds are already at risk. Run the [backup guide](https://engramwallet.com/guides/backup-engram-wallet) first:

1. Open **My Account > Export Datashard**.
2. Save the encrypted file to your external medium.
3. Verify you can read it back.

If you cannot find the backup, rotate a new wallet. Do not deposit.

## Step 4 — Rehearse recovery

Still before you deposit: on a secondary machine, run the [restore guide](https://engramwallet.com/guides/restore-engram-wallet) using your seed phrase. Confirm the first receive address matches the original. If it does, your backup is real. Delete the test wallet file; keep the seed phrase.

## Step 5 — Copy your receive address

In the original Engram wallet on your main machine:

1. Unlock with your password.
2. Open **Transfers** or **Identity** (if you want to register a Dero name first).
3. Copy the wallet address.

## Step 6 — Withdraw from the exchange

1. Log into the exchange.
2. Initiate a DERO withdrawal.
3. Paste the Engram receive address — triple-check the first and last characters.
4. Send a small test amount, e.g. 1 DERO.
5. Wait for the transaction to appear in Engram's Transfers view.

## Step 7 — Withdraw the remainder

Once the test transaction confirms, withdraw the rest of your balance. Do not split a withdrawal across multiple addresses unless you have a specific reason — it complicates bookkeeping without improving privacy on Dero, which is already private by default. See [the Dero Network explained](11-dero-network-explained.md) for the cryptographic reasoning.

## Step 8 — Close or idle the exchange account

Once all DERO has settled in Engram, you can:

- Disable withdrawal permissions on the exchange if you still use fiat there.
- Remove the exchange account from your password manager's "crypto" folder.
- Leave a zero balance. Do not delete the account yet — you may need it for future fiat on/off ramps.

## Ongoing security discipline

- Verify every new Engram release against the checksum published on [engramwallet.com/download](https://engramwallet.com/download).
- Never enter your seed phrase into a website. Ever. The [safety check](https://engramwallet.com/is-engram-wallet-safe) lists common phishing patterns.
- Re-rehearse recovery every few months.
- Keep the [guides index](https://engramwallet.com/guides) bookmarked for the canonical how-tos.

## Migrating from other wallets

If you are not on an exchange but instead on another Dero wallet:

- **Stargate users** — follow [Engram vs Stargate](https://engramwallet.com/guides/engram-vs-stargate-wallet).
- **CLI users** — read [Engram vs the CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet) and simply restore your seed into Engram.
- **Web wallet users** — export your seed and restore into Engram using the [restore guide](https://engramwallet.com/guides/restore-engram-wallet). Retire the web wallet afterwards.

## Final checks

After a week of successful use, you can answer the three questions that matter:

1. **Do you still have the seed phrase?** Stored offline, in two locations.
2. **Do you still have the Datashard backup?** Stored on an offline medium.
3. **Can you still unlock the wallet?** Your password still works.

If any answer is "no", fix it today. For deeper background, read the [review](https://engramwallet.com/reviews/engram-wallet), the [about page](https://engramwallet.com/about), the [privacy policy](https://engramwallet.com/privacy) and the [terms of use](https://engramwallet.com/terms).

## Related articles

- [How to Store DERO Coin Safely](03-store-dero-coin-safely.md)
- [How to Download and Install Engram Wallet](02-download-install-engram-wallet.md)
- [Backup and Restore the Engram Wallet](05-backup-restore-engram-wallet.md)
- [Is Engram Wallet Safe and Legit?](08-is-engram-wallet-safe-2026.md)
