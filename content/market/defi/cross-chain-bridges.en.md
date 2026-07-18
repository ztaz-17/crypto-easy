---
weight: 6
title: "Cross-Chain Bridges: How to Move Crypto Between Networks"
description: "How cross-chain bridges work, the main risks (bridge hacks), and when it's safe to use them"
category: "defi"
translationKey: "cross-chain-bridges"
slug: "cross-chain-bridges"
keywords:
  - cross-chain bridge
  - blockchain bridge
  - Wormhole
  - bridge hack
  - network bridge
prev: "/en/market/defi/defi-risks"
next: "/en/market/defi/dex-vs-cex-which-to-choose"
---

## Cross-Chain Bridges: How to Move Crypto Between Networks

---

You bought ETH on Ethereum but want to use it on Arbitrum, where fees are lower and transactions are faster.

Or you have USDT on Tron but need them on Binance Smart Chain.

The issue: **different blockchains don't talk to each other directly**. Bitcoin doesn't know about Ethereum, and Ethereum doesn't know about Solana.

That's where **cross-chain bridges** come in — tools that let you move assets from one network to another.

In this article we'll cover:

>- how bridges work;
>- what risks come with them;
>- when you can use them without worry.

---

## How Cross-Chain Bridges Work

### The Basic Idea: Lock + Mint

Most bridges follow the same principle:

1. You send your asset (say, ETH) to the **bridge contract** on the source network.
2. The bridge **locks** that asset.
3. A wrapped version is **minted** on the destination network.

Example:

> You send 1 ETH to the bridge on Ethereum → the bridge locks 1 ETH → **1 WETH (Wrapped Ether)** appears on Polygon.

👉 You're not actually "moving" the original ETH. You're **freezing it** in one network and **getting a copy** in another.

### How Does That Copy Become Real Money Again?

When you want to go back:

1. You send WETH back to the bridge on Polygon.
2. The bridge **burns** that WETH.
3. The original ETH is unlocked on Ethereum.

This is called **lock + mint / burn + unlock**.

---

### Types of Bridges

| Type | How It Works | Examples |
|------|-------------|---------|
| **Centralized** | A company controls a multi-sig wallet | Binance Bridge, Portal (WBTC) |
| **Decentralized** | Smart contracts + validators (oracles) | Wormhole, Synapse, Stargate |
| **Official** | Built by the blockchain's own team | Arbitrum Bridge, Optimism Bridge |

---

## Why Do You Need Bridges?

### Access to Other Ecosystems

Each network is its own world with its own DeFi apps:

- **Ethereum** — the most secure, but expensive.
- **Arbitrum / Optimism** — same capabilities, cheaper (L2s).
- **Solana** — very fast and cheap.
- **BNB Chain** — popular for memecoins and gaming.
- **Tron** — the standard for USDT transfers.

👉 Bridges let you avoid being stuck in "one network forever" — you move around as needed.

### Lower Fees

Moving ETH through the official bridge to Arbitrum might cost $5–10.  
Doing the same operations directly on Ethereum — $20–100+.

For frequent transactions, the savings add up fast.

---

## The Main Risks: Why Bridges Get Hacked

Bridges are **the most attacked part of DeFi**.

The reason is simple: if a hacker gets control of the bridge, they can drain locked assets worth billions.

### Biggest Bridge Hacks

| Bridge | Network | Loss | Year |
|--------|---------|------|------|
| **Ronin Bridge** | Axie Infinity (Ronin) | **$620M** | 2022 |
| **Wormhole** | Ethereum ↔ Solana | **$325M** | 2022 |
| **Nomad** | Multi-chain | **$190M** | 2022 |
| **Harmony Bridge** | Harmony ↔ Ethereum | **$100M** | 2022 |

### How Do Bridges Get Hacked?

**1. Smart contract vulnerabilities**

The bridge code has bugs that hackers find and exploit.

Wormhole example (2022):

> A hacker found a vulnerability in the signature verification contract. They minted **120,000 WETH** without any real collateral and then bridged it out to Ethereum.

**2. Validator compromise**

Decentralized bridges rely on a group of validators (or nodes). If attackers take over the majority, they can sign off on any transaction.

Ronin example (2022):

> Hackers compromised **5 out of 9 private keys** of Ronin's validators. After that, they could authorize any withdrawal.

**3. Human error**

Configuration mistakes, outdated code, team carelessness.

Nomad example (2022):

> A bug in a contract update meant anyone could drain funds — they just had to copy another user's transaction.

---

## When Is It Safe to Use a Bridge?

### ✅ Official Bridges

The safest option is to use a bridge built by the blockchain's own team:

- **[Arbitrum Bridge](https://bridge.arbitrum.io)** — for moving between Ethereum and Arbitrum.
- **[Optimism Bridge](https://app.optimism.io/bridge)** — for Optimism.
- **[zkSync Bridge](https://bridge.zksync.io)** — for zkSync.
- **[Polygon PoS Bridge](https://portal.polygon.technology)** — for Polygon.

👉 These bridges have fewer points of failure because trust boils down to trust in the blockchain itself.

### ✅ Battle-tested Decentralized Bridges

If there's no official bridge, use well-known protocols with audited code:

- **Stargate** (LayerZero) — supports many networks, mathematically backed.
- **Synapse** — one of the oldest.
- **Across** — a fast bridge built on UMA.

### ✅ Small Test Amounts First

Safety rule:

> Send a small test amount first.  
> Confirm the funds arrived.  
> Then send the rest.

---

### ❌ What to Avoid

- **New bridges with no track record** — code hasn't been audited by professionals or the community.
- **Bridges promising "超高 yield"** — often scams.
- **Bridges to obscure networks** — the lower the TVL, the higher the risk.

---

## Common Mistake: Wrapped Tokens Aren't the Real Thing

When you bridge ETH, you don't get real ETH — you get a **representation** (wrapped token).

Important:

> **WETH on Polygon is not ETH on Ethereum.**  
> You can't send WETH to an Ethereum address and expect it to "magically turn into" ETH.

To get the original back, you need to bridge back.

Different networks — different tokens:

| Asset | Network | Contract Address (example) |
|-------|---------|---------------------------|
| USDC | Ethereum | 0xA0b8... |
| USDC.e | Avalanche | 0xB97e... |
| USDT | Tron | TR7NH... |
| USDT | BNB Chain | 0x55d3... |

👉 Always verify which token contract you're getting — use a block explorer (Etherscan, BSCScan) or a link from the official site.

---

## Comparison: Ways to Move Between Networks

| Method | Example | Speed | Fees | Trust |
|--------|---------|-------|------|-------|
| Official bridge | Arbitrum Bridge | 10–30 min | Medium | High |
| Decentralized bridge | Stargate | 1–10 min | Medium | Medium |
| Centralized bridge | Binance Bridge | Instant | Low | Low (exchange holds your funds) |
| CEX (centralized exchange) | Binance → withdraw to another network | 5–30 min | Low | Low (custodial risk) |

---

## Conclusion

Cross-chain bridges are an **essential tool** for navigating the multi-chain world.

Without them, you're stuck in one network. With them, you can use the best apps and lowest fees across any ecosystem.

But keep this in mind:

> **Bridges are the riskiest part of DeFi.**

Safety rules:

>- use **official bridges** from the blockchain teams;
>- for everything else — **battle-tested protocols** (Stargate, Synapse);
>- always send a **test amount** first;
>- **don't keep large sums sitting in a bridge** — move and withdraw immediately.

Bridges are like crosswalks.  
As long as you look both ways — you're fine.  
Let your guard down — and you could lose everything.

---

## FAQ

### Can I send ETH from Ethereum to Solana directly?

Not directly. Through a bridge (like Wormhole) — yes. You'll get WETH (Wrapped ETH) on Solana.

### What happened with the Ronin bridge?

In 2022, hackers gained control of 5 out of 9 validator keys and drained 173,600 ETH and 25.5M USDC — totaling $620M.

### Is Wormhole safe now?

After the hack ($325M), the code was patched and Jump Trading partially returned the funds. Today Wormhole is considered a major bridge, but any bridge carries risk.

### What's the difference between a bridge and a cross-chain swap?

A bridge is infrastructure (the protocol), while a cross-chain swap is an app built on top (e.g., Jupiter on Solana or THORSwap).

### Do I need to pay gas in both networks?

Yes. You pay a transaction fee on the source network and a minting fee on the destination network. Often the gas is handled automatically in one go.
