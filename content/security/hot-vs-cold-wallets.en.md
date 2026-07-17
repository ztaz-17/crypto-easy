---
weight: 1
title: "Hot vs Cold Wallets: Which One to Choose"
description: "The difference between hot and cold crypto wallets — MetaMask, Trust Wallet, Ledger, Trezor. When to use which and how to keep your coins safe."
category: "security"
translationKey: "hot-vs-cold-wallets"
slug: "hot-vs-cold-wallets"
keywords:
  - hot wallet
  - cold wallet
  - hardware wallet
  - Ledger
  - Trezor
  - crypto storage
  - security
prev: ""
next: "/en/security/common-mistakes"
---

## Hot vs Cold Wallets: Which One to Choose

---

Imagine: you bought Bitcoin on an exchange. The money left your account, and a balance appeared on the platform.

**And here comes the main question: where do you store it now?**

Leave it on the exchange? Scary — exchanges get hacked, go bankrupt, freeze withdrawals.
Move it to a wallet? But which one?

In crypto, there are two fundamentally different approaches to storage:

>- **hot wallets** — always online, convenient, but vulnerable;
>- **cold wallets** — offline, maximum security, but less convenient.

In this article, we'll cover:

>- how they differ;
>- when to use which;
>- and why most people should have **both**.

---

## Hot Wallets: Always Connected

### What Is It

A **hot wallet** is a program that's constantly connected to the internet.

Your keys are stored on your device (phone, computer) and used to sign transactions in real time.

### Examples

| Wallet            | Type              | Key Feature                           |
|-------------------|-------------------|---------------------------------------|
| **MetaMask**      | Browser extension | Most popular for Ethereum and EVM networks |
| **Trust Wallet**  | Mobile app        | Convenient, multi-currency, built-in DApp browser |
| **Exodus**        | Desktop / Mobile  | Beautiful interface, built-in exchange |
| **Phantom**       | Browser / Mobile  | Optimized for Solana                  |
| **Coinbase Wallet**| Mobile / Extension| Integrated with exchange, non-custodial |

👉 All these wallets are **non-custodial**: the keys are stored with you, not the company.

### How They Work

1. You install the app or extension.
2. The wallet generates a **[seed phrase](/en/glossary/#seed-phrase)** (12 or 24 words).
3. Private keys are created from the seed phrase.
4. Every time you send crypto, the wallet signs the transaction **right on your device**.
5. The signed transaction is sent to the network.

All of this happens in seconds. Convenient? Very.

### Pros of Hot Wallets

- fast transactions;
- convenient access from phone or computer;
- integration with DApps, DeFi, NFTs;
- free (except network fees);
- great for daily use.

### Cons of Hot Wallets

- **keys are stored on a device connected to the internet**;
- if a virus, phishing, or malware gets in — your money can be stolen;
- if your phone breaks — recovery requires the seed phrase;
- require caution when using.

---

## Cold Wallets: Offline Security

### What Is It

A **cold wallet** is a physical device (or piece of paper) where your keys **never touch the internet**.

The most popular option is a **hardware wallet**.

### Examples

| Device              | Key Feature                            |
|---------------------|----------------------------------------|
| **Ledger Nano S Plus** | Affordable, reliable, supports 100+ tokens |
| **Ledger Nano X**   | Bluetooth, can connect to your phone   |
| **Trezor Model One** | First hardware wallet, open-source    |
| **Trezor Model T**  | Touchscreen, more convenient           |
| **KeepKey**         | Large screen, integration with ShapeShift |
| **SafePal**         | Affordable Ledger alternative, Air-Gapped (no cables) |

### How They Work

1. You buy the device (e.g., Ledger).
2. On first boot, it generates keys **inside itself**, without going online.
3. The device shows you a seed phrase — you write it down on paper.
4. To send a transaction:
   - you create it in the app (Ledger Live);
   - connect the device via USB;
   - confirm on the **physical button of the device**;
   - the signed transaction goes to the network.

Key point:

> **the private key never leaves the device!**

Even if your computer is infected with a virus, the attacker cannot steal the key.

### Pros of Cold Wallets

- maximum security;
- keys never touch the internet;
- protection against viruses, phishing, keyloggers;
- can be safely connected to an infected computer;
- supports many cryptocurrencies.

### Cons of Cold Wallets

- **cost money** (from $50 to $200+);
- less convenient for frequent transactions;
- need to carry with you (if you need to send crypto);
- can be physically lost;
- require careful storage of the seed phrase.

---

## Hot vs Cold: Comparison Table

| Criteria                 | Hot Wallet                            | Cold Wallet                            |
|--------------------------|---------------------------------------|----------------------------------------|
| **Internet connection**  | Always online                         | Offline (connects only to sign)        |
| **Security**             | Medium (depends on device)            | High (keys never leave the device)     |
| **Convenience**          | High (fast transactions)              | Medium (need to connect device)        |
| **Cost**                 | Free                                  | $50–$200                               |
| **Virus protection**     | Low                                   | High                                   |
| **For daily spending**   | ✅ Great                              | ❌ Inconvenient                        |
| **For long-term storage**| ❌ Risky                              | ✅ Ideal                               |
| **DeFi / NFT**           | ✅ Easy                               | ⚠️ Possible but more complex          |
| **Risk of key loss**     | Higher (virus, phishing)              | Lower (but device can be lost)         |
| **Recovery**             | Via seed phrase                       | Via seed phrase (need new device)      |

---

## When to Use What

The rule is simple:

>- **Hot wallet** — for money you spend.
>- **Cold wallet** — for money you save.

### Scenario 1: "Everyday Wallet"

You:

- buy coffee with crypto;
- send money to friends;
- use DeFi apps.

👉 You need a **hot wallet** (MetaMask, Trust Wallet). Keep a small amount there — what you're willing to lose in case of a hack.

### Scenario 2: "Long-Term Savings"

You:

- bought Bitcoin and don't plan to sell for 2–3 years;
- keep savings in stablecoins;
- are afraid the exchange will get hacked.

👉 You need a **cold wallet** (Ledger, Trezor). Keep 80–90% of your assets there.

### Scenario 3: "The Golden Middle" (Recommended)

Most experienced users do this:

> **90% of assets on cold wallet. 10% on hot wallet for operations.**

- withdraw from exchange → to Ledger;
- when you need to do something → move some to MetaMask;
- done → send the rest back to cold storage.

---

## Common Questions

### Which is more secure: Ledger or Trezor?

Both are reliable. Ledger uses a secure chip (like bank cards). Trezor is open-source — the code can be verified.

👉 The difference is in ecosystem and price. Choose based on convenience.

### Can I use a hot wallet for large amounts?

You can. But you shouldn't.

Any program that's always online is a target. A phishing link, a fake extension, a virus — and your money is gone.

> **Keep on hot wallet only what you can afford to lose.**

### What if my phone gets stolen?

Hot wallet on phone: if there's no screen lock, the attacker can transfer your funds.

Solution: use a **PIN code**, **biometrics**, and keep your seed phrase separate from your phone.

### Can I recover a cold wallet without the device?

Yes. The seed phrase is universal.

- lost your Ledger → buy a new one → enter the seed phrase → access restored.
- you can even recover it in MetaMask (enter the same seed phrase).

👉 That's why **the seed phrase IS your money**.

### What if my Ledger breaks?

No problem. The device is just a "key." The coins themselves are stored on the blockchain.

Buy a new Ledger (or any other BIP39-compatible wallet) and restore access using your seed phrase.

---

## Conclusion

The main principle in crypto:

> **Not your keys, not your coins.**

But keeping your keys online is risky. Keeping them only offline is inconvenient.

So the solution is simple:

- install **MetaMask** or **Trust Wallet** — for quick operations;
- buy a **Ledger** or **Trezor** — for savings;
- split your assets: **10% hot, 90% cold**.

It's not an "either/or." It's **both**.

---

## FAQ

### What should a beginner choose?
Start with a hot wallet (MetaMask, Trust Wallet). When you've accumulated an amount you'd hate to lose — buy a Ledger.

### Is a paper wallet a cold wallet?
Yes. But it's easy to lose, tear, or get wet. Hardware wallets are more reliable for most people.

### Can I trust exchange hot wallets?
Only if it's a non-custodial wallet (e.g., Coinbase Wallet). Custodial ones (Binance, Bybit) are not wallets — just exchange accounts.

### What if I lose my cold wallet seed phrase?
Nothing. Without the seed phrase, access to your coins is lost forever. Store it securely, preferably two copies in different places.

### Are there wallets that combine both approaches?
Some hardware wallets (Ledger Nano X with Bluetooth) can connect to your phone and sign transactions quickly. But it's still a cold wallet — the keys are inside the device.
