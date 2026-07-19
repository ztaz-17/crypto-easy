---
weight: 230
title: "Block Confirmations: What a Block Is and Why You Have to Wait"
description: "What is a block in blockchain, how confirmations work, and why you should wait before considering a transaction final. Security explained for beginners."
category: "how-it-works"
translationKey: "block-confirmations"
slug: "block-confirmations"
keywords:
  - block confirmation
  - blockchain block
  - transaction confirmation
  - Bitcoin confirmation
  - block time
  - 6 confirmations
---

## Block Confirmations: What a Block Is and Why You Have to Wait

---

You send some crypto. The screen says, "Transaction sent." But instead of seeing the deposit — you get: "Waiting for confirmation..."

A minute passes. Then another. Then a third.

And the coins still haven't arrived.

Why can't we just send things instantly? They're digital money, after all!

The answer lies in how the [blockchain](/en/glossary/#blockchain) itself works. Your transaction doesn't fly directly from [wallet](/en/glossary/#wallet) to wallet. First it has to land inside a **[block](/en/glossary/#block)** — and only then does it become part of the history.

> In this article we'll cover: what a block is, why confirmations are needed, how many you should wait for, and when a transaction can be considered safe.

---

## What Is a Block in a Blockchain

A [blockchain](/en/glossary/#blockchain) is a chain of [blocks](/en/glossary/#block). It sounds like a tautology, but that's literally what it is.

A **[block](/en/glossary/#block)** is a container that bundles transactions together. Think of it as a page in a ledger. Several transfers are written on a single page. When the page is full, it gets added to the book and a new one starts.

In a [blockchain](/en/glossary/#blockchain):

- each block contains a **set of transactions** (anywhere from a handful to thousands);
- blocks come one after another in sequence;
- every new block references the one before it (hence "chain").

What's inside a block:

| What's inside | Example |
|---------------|---------|
| **Block header** | Previous block's hash, timestamp, difficulty, nonce |
| **Transaction list** | All transfers included in this block |
| **Metadata** | Block size, version, transaction count |

If someone tries to change a single transaction in an old block — that block's hash changes, and the entire chain that follows becomes invalid. This is what makes a blockchain **immutable**.

> More on hashes and cryptography: [hash function](/en/glossary/#hash-function).

---

## Who Creates Blocks

Different blockchains create blocks in different ways, but the idea is the same: **someone has to gather transactions, package them into a block, and propose it to the network.**

### Bitcoin: Miners (Proof of Work)

Miners collect transactions from the mempool into a block and start solving a mathematical puzzle. The first one to find a solution gets the right to add their block to the chain and claim the reward.

This process requires enormous computing power. That's why a new block in Bitcoin appears on average once every **10 minutes**.

### Ethereum: Validators (Proof of Stake)

After switching to [Proof of Stake](/en/glossary/#proof-of-stake), blocks in Ethereum are created by **validators** — participants who have staked at least 32 ETH. They don't "mine" — they simply confirm blocks.

A new block in Ethereum appears roughly every **~12 seconds**.

### Solana and Other Fast Networks

Solana uses a combination of Proof of History and [Proof of Stake](/en/glossary/#proof-of-stake). Blocks here appear every **~400 milliseconds**. A transaction is confirmed almost instantly.

> More on consensus: [Proof of Work](/en/glossary/#proof-of-work), [Proof of Stake](/en/glossary/#proof-of-stake).

---

## Why You Have to Wait for Confirmations

Now to the main question: why can't coins be credited right away?

### The Double-Spend Problem

Imagine you have 1 BTC. You send it to Alice — and at the same time the same 1 BTC to Bob. If transactions were credited instantly, both could go through. The network would be confused about who actually got the coins.

The blockchain solves this like so:

1. The transaction is sent to the network.
2. It lands in the mempool (a temporary queue).
3. A miner/validator includes it in a block.
4. Once included — a double spend becomes impossible.

> Until a transaction is in a block, it isn't considered final.

### Why Multiple Confirmations

One confirmation means your transaction made it into a block. But one confirmation alone isn't reliable enough.

Why? Because theoretically, a miner could create a **[fork](/en/glossary/#fork)** — an alternative block with a different transaction. If that fork ends up longer than the main chain, the original transaction gets reversed.

The more blocks come after yours — the harder it is to undo the transaction. Each additional block is like another layer of concrete poured on top of the previous one.

| Number of confirmations | Reliability |
|-------------------------|-------------|
| 0 | Transaction in the mempool — may not get confirmed |
| 1 | Landed in a block, but reversal is possible via a [fork](/en/glossary/#fork) |
| 3 | Reliable enough for small amounts |
| 6 | **Very reliable** — the standard for Bitcoin |
| 12+ | Maximum security |

---

## How Many Confirmations Are Needed

The number of required confirmations depends on the transfer amount and the network.

### Bitcoin: 6 Confirmations

For Bitcoin, **6 confirmations** is the standard. That means waiting about an hour.

Why 6 specifically? Mathematical modeling shows that the probability of a transaction being reversed after 6 blocks approaches zero. Even if an attacker controls 10% of the network's hashrate, the chance of a successful attack after 6 blocks is less than 0.1%.

For small transfers (like a cup of coffee), 1–3 confirmations are enough. For large amounts — go with all 6.

### Ethereum: 12–30 Confirmations

Ethereum is faster: a block every ~12 seconds. But because of the finality mechanism, the standard number of confirmations is **12–30 blocks** (~2–6 minutes).

After 32 blocks (a so-called checkpoint) a transaction is considered final — it can't be reversed, even theoretically.

### Table: Confirmation Time for Different Networks

| Network | Block time | Standard confirmations | Total wait time |
|---------|------------|------------------------|-----------------|
| Bitcoin | ~10 min | 6 | ~60 min |
| Bitcoin Cash | ~10 min | 3 | ~30 min |
| Ethereum | ~12 sec | 12–30 | ~2–6 min |
| Litecoin | ~2.5 min | 6 | ~15 min |
| Solana | ~400 ms | 1 | Instant |
| TRON | ~3 sec | 19 | ~1 min |
| BNB Chain | ~3 sec | 15 | ~45 sec |
| Dogecoin | ~1 min | 5 | ~5 min |

> **Important:** exchanges and services set their own confirmation requirements. Binance might credit a deposit after 1 Bitcoin confirmation, while Coinbase waits for 3. That's their security policy.

---

## What the User Sees at Each Stage

Let's look at a transaction through the user's eyes:

| Status | What's happening | Sender sees | Receiver sees |
|--------|-----------------|-------------|---------------|
| **Pending** | Transaction is in the mempool, waiting to be included in a block | "Sent" | Nothing |
| **1 confirmation** | Transaction is in a block | "Confirmed (1/6)" | "Awaiting credit" |
| **3 confirmations** | Safe for small amounts | "Confirmed (3/6)" | "Awaiting credit" |
| **6 confirmations** | Full security for Bitcoin | "Completed" | "Credited" |

Note: the receiver can see an unconfirmed transaction via a block explorer (e.g., [mempool.space](https://mempool.space) for Bitcoin). But their [wallet](/en/glossary/#wallet) will still show a zero balance until enough confirmations stack up.

---

## A Real Story

I once bought a phone online and paid with Bitcoin. The seller asked me to wait for **3 confirmations** — "just to be safe."

I sent the bitcoins. The transaction made it into the first block after 8 minutes. The second — another 12 minutes later. And the third... got stuck.

The network was congested: more than 100,000 unconfirmed transactions were sitting in the mempool. My fee was average — miners were picking whoever paid more.

The third block only showed up 47 minutes later.

**The bottom line:** I waited 3 days for the phone, and 67 minutes for the transaction confirmation. The seller only shipped the phone after 3 confirmations.

> Ever since then, I always set my fee a little above average when time matters. Saving $1 isn't worth an hour of waiting.

---

## Can You Speed Up a Confirmation?

Yes, in some cases you can.

### 1. Pick the Right Fee

The higher the fee, the faster miners will pick up your transaction. Before sending, check the current network load:

- Bitcoin: [mempool.space](https://mempool.space)
- Ethereum: [etherscan.io/gastracker](https://etherscan.io/gastracker)

### 2. Use Replace-by-Fee (RBF)

Bitcoin supports RBF — a mechanism that lets you replace an unconfirmed transaction with the same one but with a higher fee. Enable this option in your [wallet](/en/glossary/#wallet) beforehand.

### 3. Choose Fast Networks

If you don't have to use Bitcoin or Ethereum, try:

- **Litecoin** — a block every 2.5 minutes;
- **Solana** — instant confirmations;
- **Lightning Network** — Bitcoin's satellite layer, confirmation in seconds.

> Speed doesn't always mean security. Fast networks use a different consensus mechanism, and the number of confirmations still matters there — blocks just come more frequently.

---

## Summary

Transaction confirmations aren't a bug or sluggish network behavior. They are a **fundamental protection** against double spending and fraud.

**In short:**

- A **block** is a container for transactions. Each new block references the one before it.
- A **confirmation** means your transaction was included in a block. One confirmation = one block after your transaction.
- **The more confirmations, the safer.** 6 for Bitcoin, 12–30 for Ethereum.
- **Wait time depends on the network:** from 400 ms (Solana) to an hour (Bitcoin).
- **You can speed things up:** choose a fee, use RBF, or pick a faster network.

[Cryptocurrency](/en/glossary/#cryptocurrency) is a trade-off between speed and security. The more reliable the network, the longer you wait. But once a transaction is finally confirmed — it becomes part of a history that no one can rewrite.

> As the saying goes: "Not your keys, not your coins." Let's add: "Not confirmed, not your transaction."

---

## FAQ

### How long do I have to wait for a Bitcoin transaction?

Typically 10–60 minutes. It all depends on the fee and network load. The first confirmation usually arrives in 10–30 minutes, 6 confirmations take about an hour.

### Can I cancel a transaction before it's confirmed?

If the transaction is still in the mempool — you can try replacing it via RBF (if your wallet supports it). If it's already in a block — no. If several blocks have passed — reversal is practically impossible.

### Why does a deposit arrive at an exchange faster than expected?

Exchanges often credit funds after 1–2 confirmations without waiting for all 6. That's the exchange's risk, not yours. But they may only let you withdraw those funds once the full number of confirmations has been reached.

### What is an orphan block?

It's a block that was mined at the same time as another and didn't make it into the main chain. Transactions from such a block go back to the mempool and wait for the next confirmation.

### How many confirmations does USDT need?

It depends on the network: for ERC-20 (Ethereum) — 12–30, for TRC-20 (TRON) — 19, for BEP-20 (BNB Chain) — 15.

### How do I check the number of confirmations?

Use a block explorer. For Bitcoin — [mempool.space](https://mempool.space), for Ethereum — [etherscan.io](https://etherscan.io). Just paste your transaction hash.

### Does the transfer amount affect speed?

No. The fee doesn't depend on the amount. A $1 transaction and a $1,000,000 transaction with the same fee will be confirmed at the same time.
