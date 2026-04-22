# How to Store DERO Coin Safely: A Non-Custodial Wallet Walkthrough

Holding [DERO coin](https://engramwallet.com/dero-coin) on an exchange means an exchange can freeze, lose or confiscate it. Self-custody in a non-custodial wallet removes that risk. This article explains how DERO works under the hood, why generic wallets cannot store it, and how to move your balance into [Engram Wallet](https://engramwallet.com/) — the official Dero desktop wallet.

## What DERO is and why storage is different

DERO is the native coin of the Dero Network, a privacy-first layer-1 blockchain. Unlike transparent chains, Dero transactions encrypt both the amounts and the state of smart contracts. It combines ring signatures with homomorphic encryption so balances are never visible on-chain. This is great for privacy but rules out multi-coin wallets that expect transparent UTXO or account models.

To transact DERO you need a client that understands Dero's native cryptography. The most robust option is the [official Dero wallet](https://engramwallet.com/dero-wallet), Engram, which is written in the same Go codebase as the chain itself. A compact reference is the [DERO coin page](https://engramwallet.com/dero-coin).

## Why centralized exchanges are not storage

Exchanges hold the keys to the DERO you "own" on their platform. Legally, you own a claim on the exchange, not the coins. This leads to four recurring failures:

1. **Withdrawal freezes** during market events or compliance sweeps.
2. **Delistings** that force you to move with little notice.
3. **Hacks** that drain custodial hot wallets.
4. **Insolvency** that converts your coins into a bankruptcy claim.

Non-custodial storage skips all four. The [Engram Wallet security architecture](https://engramwallet.com/security) and the [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe) page document how the wallet removes those intermediaries.

## Self-custody options for DERO

| Option | Custody | Interface | Best for |
| --- | --- | --- | --- |
| Engram (recommended) | Self | Desktop GUI | Everyday use |
| Dero CLI | Self | Terminal | Developers |
| Stargate (legacy) | Self | Desktop GUI | Migrating away |
| Exchange account | Custodial | Web/app | Trading only, not storage |

Detailed comparisons live in [Engram vs the CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet) and [Engram vs Stargate](https://engramwallet.com/guides/engram-vs-stargate-wallet). In short, Engram wins on three axes: it is maintained by the Dero Foundation, it is the only wallet updated in lockstep with the chain, and it has the friendliest UI.

## Step-by-step: move DERO into Engram

1. **Download the wallet** from [engramwallet.com/download](https://engramwallet.com/download). Pick [Windows](https://engramwallet.com/download/windows), [macOS](https://engramwallet.com/download/mac) or [Linux](https://engramwallet.com/download/linux).
2. **Install and create a wallet.** Follow the [install guide](https://engramwallet.com/guides/install-engram-wallet). Set a strong password — AES-256 protects your wallet file locally.
3. **Write down the seed phrase.** This is the only way to recover funds. Do not photograph it.
4. **Back up.** The [backup guide](https://engramwallet.com/guides/backup-engram-wallet) produces a Datashard file you can store on an encrypted USB stick.
5. **Copy your receive address.** Open the **Identity** or **Transfers** module.
6. **Withdraw from the exchange.** Send a small test amount first. When it arrives, send the rest.
7. **Confirm arrival** via the Transfers tab. You now control the keys.

## Daily use: send, receive, store

- **Receive DERO.** Share either your wallet address or a registered Dero name from the Identity module.
- **Send DERO.** Open Transfers, paste the recipient address, and approve with your wallet password.
- **Hold DERO.** The balance stays encrypted on disk — no online wallet, no server exposure. The [Engram review](https://engramwallet.com/reviews/engram-wallet) walks through each module.

## Recovery planning

Any self-custody plan must include recovery. Without a seed phrase and backup, funds are lost permanently — no company can restore them. The [restore guide](https://engramwallet.com/guides/restore-engram-wallet) covers:

- Re-importing from seed phrase on a new device.
- Importing a Datashard backup file.
- Swapping wallet passwords.

Pair it with the [security architecture](https://engramwallet.com/security) and the [guides index](https://engramwallet.com/guides) to build a personal disaster-recovery plan.

## Is storing DERO in Engram safe?

Engram is open source, audited, and distributed only from [engramwallet.com](https://engramwallet.com/) and the Dero Foundation's GitHub. The [2026 safety check](https://engramwallet.com/is-engram-wallet-safe), the [review](https://engramwallet.com/reviews/engram-wallet), and the [about page](https://engramwallet.com/about) all back up the same answer: yes, it is safe — provided you protect your seed phrase, follow the [backup guide](https://engramwallet.com/guides/backup-engram-wallet), and only download from official sources.

## Related articles

- [Engram Wallet: The Complete Guide](01-engram-wallet-complete-guide.md)
- [How to Download and Install Engram Wallet](02-download-install-engram-wallet.md)
- [The Dero Network Explained](11-dero-network-explained.md)
- [Moving from Exchanges to Self-Custody with Engram Wallet](12-exchanges-to-self-custody.md)
