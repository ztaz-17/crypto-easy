---
weight: 240
title: "Why Transactions Get Stuck and What to Do About It"
description: "Why crypto transactions get stuck and what to do. Low fees, network congestion, RBF, and CPFP — how to speed up a stuck transaction explained clearly."
category: "how-it-works"
translationKey: "why-transactions-stuck"
slug: "why-transactions-get-stuck"
keywords:
  - stuck transaction
  - pending transaction
  - replace-by-fee
  - RBF
  - transaction acceleration
  - Bitcoin stuck
  - Ethereum stuck
---

## Why Transactions Get Stuck and What to Do About It

---

You send some crypto. The amount is right, the address is correct, you hit send.

And on the screen — "Pending." One hour. Two. Five.

The coins are deducted, but the recipient doesn't see them. The transaction is stuck in "awaiting confirmation" limbo, and nothing happens.

Sound familiar?

> **A stuck transaction** — one of the most common issues for crypto beginners. But it's almost always fixable.

In this article, we'll cover:

> - why transactions get stuck;
> - how to tell "it's stuck" from "just wait a bit longer";
> - what you can do right now: speed up, cancel, or replace;
> - and how to avoid ending up in this situation in the future.

---

## Why Transactions Get Stuck

### 1. Fee Too Low

This is the number one reason.

Every [blockchain](/en/glossary/#blockchain) transaction is a request for a spot in a [block](/en/glossary/#block). Block space is limited. Miners (Bitcoin) or validators (Ethereum) choose which transactions to include first.

The rule is simple: **whoever pays more goes first.**

If you set your fee below the current market rate — your transaction sits in the mempool, waiting for the network to clear up.

Learn more about how fees are determined: [Why Sending Crypto Sometimes Costs $30](/en/learn/how-it-works/why-transaction-costs-30).

---

### 2. Network Congestion (Mempool Is Packed)

Even with a decent fee, your transaction can get stuck during peak hours.

When thousands of transactions are being sent at the same time (e.g., during a memecoin hype cycle, an [NFT](/en/glossary/#nft) mint, or a major event), the mempool gets flooded. Block size stays the same, but the number of people trying to get in is 10 times higher than usual.

At times like this, miners only pick the juiciest transactions — everyone else waits.

> Bitcoin's mempool can hit **300,000+ unconfirmed transactions**. Ethereum's queue is smaller, but during peak hours the base fee can spike 5–10x.

---

### 3. Stuck Because of a Wallet Bug

Sometimes the problem isn't the network — it's your [wallet](/en/glossary/#wallet):

- gas was calculated incorrectly (on Ethereum — gas limit below 21,000);
- the [wallet](/en/glossary/#wallet) didn't update the transaction status;
- you're connected to an outdated or broken node.

In these cases, the transaction might show as "sent" even after it's been confirmed. Check a [blockchain](/en/glossary/#blockchain) explorer — it's probably fine.

---

### 4. A Very Low-Priority Transaction Got Evicted

If the mempool is jammed and your fee is rock bottom, some nodes may simply drop the transaction from the pool. It doesn't vanish forever — if it's never rebroadcast, it "evaporates" and the coins stay at your address.

But until you send a new transaction, your funds are effectively "frozen": the network ignores the old one, and you can't send a new one because your [wallet](/en/glossary/#wallet) thinks those coins are already gone.

---

## How to Tell If a Transaction Is Really Stuck

Before you panic, check the transaction status on a [blockchain](/en/glossary/#blockchain) explorer:

| Network | Explorer |
|---------|----------|
| Bitcoin | [mempool.space](https://mempool.space) |
| Ethereum | [etherscan.io](https://etherscan.io) |
| Solana | [solscan.io](https://solscan.io) |
| TRON | [tronscan.org](https://tronscan.org) |
| BNB Chain | [bscscan.com](https://bscscan.com) |

Paste your transaction hash (TXID) — and you'll see the status:

- **Pending / In Mempool** — the transaction is in the queue, not yet in a [block](/en/glossary/#block).
- **Confirmed / Success** — everything is fine, your wallet is just slow to update.
- **Dropped / Replaced** — the transaction was replaced or removed from the mempool.

> If the status is "Confirmed" but your wallet says "Pending" — it's a wallet issue, not a network one. Refresh or restart the app.

---

## What to Do If Your Transaction Is Stuck

You have several options. Which one to choose depends on the network, your wallet, and how patient you're feeling.

---

### 1. Replace the Transaction via RBF (Replace-by-Fee)

**Works in:** Bitcoin (and some other UTXO-based chains)  
**Requires:** a wallet that supports RBF

Replace-by-Fee is a mechanism that lets you resend the exact same transaction (same inputs) but with a higher fee. You're telling the network: "Forget the old transaction — here's the new one with a bump."

How to do it:

1. Open your wallet and find the stuck transaction.
2. Look for **"Increase fee"** or **"Replace-by-Fee"** (the name depends on your wallet).
3. Set a new fee — usually the current market rate is enough.
4. Confirm — and the new transaction replaces the old one.

**Important:** RBF has to be enabled before you send the first transaction. If you sent a transaction without the RBF flag — you can't replace it through this mechanism.

Wallets that support RBF:

- Electrum — full support;
- Bitcoin Core — yes;
- BlueWallet — yes;
- Exodus — yes;
- Trust Wallet — no (as of this writing).

> If your wallet doesn't support RBF — try option 2 or 3.

---

### 2. Use a Transaction Accelerator

**Works in:** Bitcoin (limited)

Some [mining](/en/glossary/#mining) pools offer transaction acceleration services. You submit the hash of your stuck transaction, pay a fee — and the pool includes it in the next block they mine.

Popular services:

- [Viabtc Accelerator](https://www.viabtc.com/tools/txaccelerator) — free for up to 100 transactions per hour, but doesn't guarantee inclusion;
- [BTC.com Accelerator](https://pushtx.btc.com/) — free.

**Downsides:**

- they don't always work;
- free slots fill up fast;
- paid versions cost money (often more than a normal fee).

Only use this if RBF isn't available and you can't wait any longer.

---

### 3. Cancel via Double-Spend (Child-Pays-For-Parent / CPFP)

**Works in:** Bitcoin, Ethereum, and other networks

CPFP is a mechanism where you send a **new transaction** that spends the outputs (UTXOs) of the stuck transaction. The new one carries a higher fee — miners grab both, because without the first one the second is invalid.

How to do it:

1. Find the stuck transaction in your wallet.
2. If your wallet supports CPFP — choose **"Boost with child transaction"**.
3. Set the fee for the child transaction.
4. Confirm.

**For Ethereum (MetaMask):**

1. In MetaMask, open the stuck transaction.
2. Click **"Speed up"** — the wallet resends the same transaction with a higher fee.
3. Or click **"Cancel"** — MetaMask sends a "blank" transaction (0 ETH) that overrides the old one.

> **Important:** canceling on Ethereum is also a transaction with a fee. You pay to replace the stuck one.

---

### 4. Just Wait

Yes, that's also an option.

On Bitcoin, low-fee transactions can hang for hours or even days. But sooner or later — when the network clears up or someone boosts the fee in that [block](/en/glossary/#block) — your transaction gets in.

Expected wait times:

- **Bitcoin:** from 1 hour to 3–7 days in extreme cases (if the mempool is packed and your fee is minimal).
- **Ethereum:** from 1 minute to a few hours.
- **Solana / TRON:** rarely get stuck, but if they do — up to an hour.

> If more than 3 days have passed and the transaction is still "Pending" — try any of the methods above.

---

### 5. Resend After the Transaction Drops Out of the Mempool

If the transaction was removed from the mempool (usually after 2–7 days on Bitcoin, sooner on other networks) — the coins automatically come back to your address.

You can simply send a new transaction — with a reasonable fee and during a calm period.

There's a catch, though: not all wallets correctly display the return. It might still look like your funds are "locked." Check your balance on a blockchain explorer — if the transaction is gone from the mempool, the coins are yours again.

---

## Quick Reference: What to Do in Each Situation

| Situation | Bitcoin | Ethereum | Other Networks |
|-----------|---------|----------|----------------|
| Low fee, RBF enabled | **RBF** — replace with bump | **Speed up** in MetaMask | Depends on wallet |
| Low fee, RBF disabled | **CPFP** or accelerator | **Cancel** + new transaction | Send new with higher nonce |
| Network congestion | Wait or accelerator | Wait — gas will drop | Wait |
| Transaction dropped from mempool | Resend | Resend | Resend |
| Wallet shows wrong status | Check explorer | Check explorer | Check explorer |
| Need it done now | Accelerator (paid) | Speed up with high gas | Increase fee |

---

## How to Prevent Stuck Transactions in the Future

### 1. Check the Mempool Before Sending

Before you broadcast a transaction, check network congestion:

- Bitcoin: [mempool.space](https://mempool.space)
- Ethereum: [etherscan.io/gastracker](https://etherscan.io/gastracker)

If the mempool is packed — wait an hour or two, or bump up the fee.

### 2. Set Your Fee Slightly Above Average

Advanced wallets offer three fee tiers:

- **Slow** — you save money, but the risk of getting stuck is higher;
- **Market / Normal** — a reasonable balance;
- **Fast** — you overpay, but the transaction goes through in the next block.

For most cases, pick **Market**. The difference between Slow and Market is usually $0.50–$2, but the wait time is 3–5 times shorter.

### 3. Enable RBF Beforehand

If your wallet supports RBF — **turn it on in settings before you send.** It doesn't change the fee for the first transaction, but it gives you the option to replace it if something goes wrong.

### 4. Choose the Right Network

Bitcoin and Ethereum aren't the only options. If you don't specifically need them:

- **Litecoin** — blocks every 2.5 minutes, fees are pennies;
- **Solana** — instant, near-zero cost;
- **TRON** — cheap and fast for USDT;
- **Lightning Network** — Bitcoin, but confirmation in seconds.

> Just make sure the recipient supports the network you choose.

### 5. Use Layer 2 Networks

If you're on Ethereum:

- Arbitrum;
- Optimism;
- Base;
- zkSync.

Fees are 50–100 times lower than the Ethereum mainnet, and the security is the same.

---

## A Real-Life Story

A while back I was buying a domain for 0.5 ETH. I entered the address, double-checked it, hit send. The fee was set to "Slow" — I figured I'd save $3.

15 minutes passed. The transaction was Pending.

30 minutes — Pending.

An hour — Pending.

I started to sweat: the domain could be snatched up if I didn't pay soon. I checked Etherscan — the mempool was packed (some [NFT](/en/glossary/#nft) sale was going on), and the base fee had doubled. My transaction was at the very bottom of the queue.

I had to hit "Speed up" with a $22 fee instead of the $4 I'd planned.

**Bottom line:** I got the domain, but trying to save $3 ended up costing me $18 extra. If I'd set a reasonable fee from the start, the transaction would have gone through in 2 minutes.

> Ever since, I never set the minimum fee when time matters. Saving $2 isn't worth an hour of stress.

---

## Summary

A stuck transaction is annoying, but almost always fixable.

**Key takeaways:**

- reason #1 — low fee and a congested mempool;
- first, check the status on a blockchain explorer — the transaction might already be confirmed;
- use RBF (Bitcoin) or Speed up (Ethereum) to accelerate;
- if RBF isn't available — try CPFP or an accelerator;
- as a last resort — just wait, the transaction won't disappear (coins will return);
- going forward — set a reasonable fee, watch the mempool, and enable RBF ahead of time.

Crypto isn't "send and forget." It's about understanding how the network works. And the better you understand it — the less often you'll see "Pending" on your screen.

> As the saying goes: "Not your keys, not your coins. Not confirmed, not your transaction."

---

## FAQ

### Why is my transaction stuck at Pending?

Your transaction is in the mempool but hasn't been included in a block yet. The cause is a low fee, network congestion, or both.

### How long can a transaction stay stuck?

Bitcoin — from 1 hour to 3–7 days. Ethereum — from 1 minute to several hours. Solana, TRON — rarely more than an hour.

### Can I cancel a stuck transaction?

Yes, if it hasn't been confirmed yet. On Bitcoin — via RBF (replace) or CPFP. On Ethereum — via "Cancel" in MetaMask. On other networks — by sending a transaction with a higher nonce.

### Will I lose my money if the transaction gets stuck?

No. If the transaction doesn't make it into a block, it will eventually be dropped from the mempool and the coins will return to your address. If the transaction is already in a block — the money is with the recipient (can't be canceled).

### What if my wallet doesn't support RBF?

Use CPFP (Child-Pays-For-Parent) or transaction acceleration services (Viabtc, BTC.com). Or just wait.

### How do I check if RBF is enabled in my wallet?

Open the send transaction settings. If you see "Enable RBF" or "Replace-by-Fee" — turn it on. If you don't see it, your wallet probably doesn't support it. Electrum and Bitcoin Core definitely do.

### Why does MetaMask show "Pending" even after confirmation?

This is a wallet-side issue, not a network one. Check the transaction hash on Etherscan — if the status is "Success," everything is fine. Refresh MetaMask or restart the extension.

### Can I speed up a transaction on an exchange?

Usually not. Exchanges use their own internal wallets and decide when to broadcast the transaction. If an exchange is dragging its feet on a withdrawal — contact their support.

### What if my transaction has been stuck for a week?

Check whether it's been dropped from the mempool. If yes — resend with a reasonable fee. If not — try RBF, CPFP, or an accelerator. After a week, only "dead" transactions remain in the mempool — almost no one picks them up.
