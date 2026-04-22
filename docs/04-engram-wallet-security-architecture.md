# Engram Wallet Security Architecture: AES-256 Keys and Self-Custody Explained

Crypto wallet security is either real or marketing. This article unpacks the specific primitives [Engram Wallet](https://engramwallet.com/) uses, the threat model it is designed for, and the operational steps users still need to take themselves. The live reference document is the [official security architecture page](https://engramwallet.com/security).

## Threat model

Engram is designed to protect against five classes of attacker:

1. **Remote attackers** trying to read keys off disk or from a server — mitigated because there is no server.
2. **Malicious processes** on your machine — mitigated by AES-256 encrypted wallet files and a password-gated unlock.
3. **Exchange collapses and custodial freezes** — mitigated by 100% local self-custody.
4. **Phishing and fake installers** — mitigated by single-source distribution from [engramwallet.com/download](https://engramwallet.com/download) and the Dero Foundation GitHub.
5. **Privacy leaks on-chain** — mitigated by Dero's native ring signatures and homomorphic encryption.

For a plain-English version of the same model, read the [is Engram Wallet safe?](https://engramwallet.com/is-engram-wallet-safe) page.

## Key generation and storage

When you create a new wallet, Engram generates the private key entirely on-device. The key is then:

- Encrypted with AES-256 using a key derived from your wallet password.
- Written to a local wallet file. The file never syncs, never uploads, and is never known to the Dero Foundation.
- Protected by the OS file permissions of the user account that created it.

No cloud service, email address or phone number is ever attached to the wallet. The only recoveries available are (a) your seed phrase and (b) your encrypted Datashard backup. Both live under your control.

## AES-256 in practice

AES-256 is a symmetric cipher and the de-facto standard for protecting data at rest. Engram uses it to encrypt the wallet file; the decryption key is derived from the password you set during wallet creation. Two practical implications:

- A weak password materially weakens AES-256. Use a long, unique passphrase.
- If you forget the password and lose the seed phrase, the wallet cannot be recovered. This is a direct consequence of the non-custodial design, covered in the [FAQ](https://engramwallet.com/#faq) and the [official Dero wallet page](https://engramwallet.com/dero-wallet).

## What the wallet does not store

- No email addresses, no phone numbers, no account IDs.
- No telemetry, usage analytics or session tokens.
- No cloud backups.

This is detailed in the [about page](https://engramwallet.com/about) and the [privacy policy](https://engramwallet.com/privacy).

## Open source and auditable

Engram is written in pure Go and its source code is published publicly by the Dero Foundation. Because the chain and the wallet share a language and a maintainer, protocol upgrades ship in the wallet with minimal delay. The [review](https://engramwallet.com/reviews/engram-wallet) and the [technical documentation](https://engramwallet.com/documentation) point to the specific modules you can audit.

## Supported platforms and distribution

Engram is published for Windows 10+, macOS 12+, and 64-bit Linux. Binaries are signed and distributed only from:

- [engramwallet.com/download](https://engramwallet.com/download) (all platforms).
- [engramwallet.com/download/windows](https://engramwallet.com/download/windows) for Windows.
- [engramwallet.com/download/mac](https://engramwallet.com/download/mac) for macOS.
- [engramwallet.com/download/linux](https://engramwallet.com/download/linux) for Linux.
- The Dero Foundation GitHub repositories.

Any other source is untrusted by default. See the [2026 safety check](https://engramwallet.com/is-engram-wallet-safe) for checksum verification steps.

## Operational security — what users must still do

Even the best wallet cannot protect you from bad operational security. The baseline:

- Write your seed phrase on paper and keep at least two geographically separated copies.
- Use a long, unique password you do not reuse elsewhere.
- Run the [backup guide](https://engramwallet.com/guides/backup-engram-wallet) on day one.
- Practice recovery on a throwaway wallet using the [restore guide](https://engramwallet.com/guides/restore-engram-wallet).
- Only install from the [official download page](https://engramwallet.com/download) and the [guides index](https://engramwallet.com/guides).

## Comparison to other Dero options

Security posture varies across Dero clients. The [Engram vs CLI wallet](https://engramwallet.com/guides/engram-vs-cli-wallet) and [Engram vs Stargate](https://engramwallet.com/guides/engram-vs-stargate-wallet) comparisons break down the differences. For exchange users, the [DERO coin storage guide](https://engramwallet.com/dero-coin) explains why a custodial balance is not equivalent to self-custody.

## Frequent security questions

**Does Engram store my private keys on a server?** No. Keys are generated and encrypted locally. See the [FAQ](https://engramwallet.com/#faq) and the [security page](https://engramwallet.com/security).

**Is Engram safer than centralized exchanges?** Yes. Exchanges hold keys in custodial hot wallets. Engram never has access. See the [safety check](https://engramwallet.com/is-engram-wallet-safe).

**Is the app signed?** Yes. Always verify you installed the build you downloaded from the [official download page](https://engramwallet.com/download).

**What if I lose my seed phrase?** Funds are permanently inaccessible. This is the core trade-off of self-custody and is documented on the [FAQ](https://engramwallet.com/#faq) and the [restore guide](https://engramwallet.com/guides/restore-engram-wallet).

## Related articles

- [Is Engram Wallet Safe and Legit? A 2026 Review](08-is-engram-wallet-safe-2026.md)
- [Backup and Restore the Engram Wallet](05-backup-restore-engram-wallet.md)
- [How to Download and Install Engram Wallet](02-download-install-engram-wallet.md)
- [Moving from Exchanges to Self-Custody](12-exchanges-to-self-custody.md)
