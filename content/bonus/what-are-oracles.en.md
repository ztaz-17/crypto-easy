---
weight: 2
title: "What Are Oracles in Crypto"
description: "Oracles — how smart contracts learn the real price of Bitcoin. Chainlink, price feeds, real-world data"
category: "bonus"
translationKey: "what-are-oracles"
slug: "what-are-oracles"
keywords:
  - oracle
  - Chainlink
  - smart contract data
  - price feed
  - off-chain data
prev: "/en/bonus/what-is-dao"
next: "/en/bonus/staking-vs-farming"
---

## What Are Oracles: How Smart Contracts See the Real World

---

Picture a robot sitting in a sealed room with no windows.

It's smart. It follows instructions perfectly. But it has no idea what's happening outside — the weather, the dollar exchange rate, who won the game.

> **A smart contract is exactly that kind of robot.**

It lives inside a blockchain and can only interact with what's already on-chain. Data from the outside world — prices, exchange rates, sports results — is off-limits.

So how do you get a smart contract to tell you the price of Bitcoin right now?

---

## The Problem: Blockchain Is Cut Off From External Data

### Why blockchain can't see the real world

Blockchain is a closed system.

Every node stores an identical copy of the data. To keep things honest, all nodes have to reach **a single agreement (consensus)**.

But how can nodes agree on what's happening outside the network?

For example:
- Bitcoin price on Binance — $60,000;
- Bitcoin price on Coinbase — $60,100;
- on some small exchange — $59,500.

> **Which price is the right one? And who decides?**

The blockchain can't answer that on its own. It needs a helper.

---

### Example: rain insurance

Say there's a smart contract that pays out insurance if it rains in Moscow tomorrow.

Problem:
- the smart contract can't look out the window;
- it can't check a weather website;
- it has no idea whether it's actually raining.

Without external data, that contract is useless.

---

## The Solution: Oracles — the Bridge Between Blockchain and the World

### What is an oracle

An **oracle** is a service that delivers data from the outside world into a blockchain.

In simple terms:
> **An oracle brings a smart contract the information it can't get on its own.**

Oracles can deliver:
- **asset prices** — BTC/USD, ETH/USD;
- **weather** — temperature, precipitation;
- **sports results** — who won the match;
- **events** — whether a payment went through, whether a date has arrived;
- **random numbers** — for lotteries and games.

---

### How it works

1. The smart contract requests data (e.g., "what's the ETH price right now?");
2. The oracle fetches data from an external source (exchange, API);
3. The oracle delivers the data to the blockchain;
4. The smart contract uses that data to execute its logic.

---

### Types of oracles

| Type | Description | Example |
|------|-------------|---------|
| **Software** | Collects data from the internet | Prices, weather, APIs |
| **Hardware** | Reads data from physical sensors | Temperature, GPS, RFID |
| **Inbound** | Brings data into the blockchain | Currency exchange rate |
| **Outbound** | Sends data from the blockchain out | Transaction notification |
| **Centralized** | Single data source | Simple, but unreliable |
| **Decentralized** | Multiple sources | Reliable, but more complex |

---

### The trust problem

Here's the big question:

> **If a smart contract trusts a single oracle — what's the point of a blockchain?**

If the oracle is a single point of failure, it can:
- provide incorrect data (error);
- provide false data (attack);
- simply go offline.

The solution — **decentralized oracles**.

Instead of one data source, a network of independent nodes is used. Each node collects data on its own. If most nodes confirm the same value — the data is considered trustworthy.

---

## Chainlink: The Most Popular Oracle

### What is Chainlink

**Chainlink** is the largest decentralized oracle network.

Instead of a single server, Chainlink uses hundreds of independent nodes that:
- collect data from multiple exchanges and APIs;
- cross-check results with each other;
- deliver agreed-upon data to the blockchain.

> Chainlink supports dozens of blockchains and thousands of smart contracts.

---

### Price Feeds: ready-made price channels

Chainlink's most popular service is **Price Feeds**.

These are ready-made data sources that already live on the blockchain.

For example, a smart contract can simply call the **ETH/USD Price Feed** address and get the current price. No need to set up an oracle yourself — everything is ready to go.

---

### How Chainlink protects data

Chainlink uses multiple layers of protection:

1. **Decentralization** — data is collected by many independent nodes;
2. **Aggregation** — the final price is the median of all sources;
3. **Incentives** — nodes earn rewards for honest work and lose their deposit for cheating.

👉 Thanks to this, Chainlink is the de facto standard for DeFi applications.

---

### Real-world example: crypto-backed loans

Imagine a DeFi protocol that issues loans backed by ETH:

- 🔹 a user deposits 10 ETH as collateral;
- 🔹 the protocol fetches the ETH price from Chainlink oracle;
- 🔹 if the collateral drops below a safe level — liquidation is triggered.

Without a reliable oracle:
- wrong price → false liquidation → user loses money;
- inflated price → the protocol takes on risk.

> **An oracle is not just "data". It's protocol security.**

---

## Conclusion

Oracles are an invisible but essential part of the crypto world.

- smart contracts are **blind** — they can't see the outside world;
- oracles **give them sight** — they deliver real-world data;
- Chainlink is the most popular and battle-tested oracle provider.

Without oracles, none of these would work:
- DeFi protocols (Aave, Compound);
- stablecoins (DAI checks collateral prices);
- insurance smart contracts;
- prediction markets.

> **Oracles are the bridge between blockchain and reality. Without that bridge, DeFi is just a sandbox game.**

---

## FAQ

### How is an oracle different from a regular API?

An API is just a way to get data. An oracle doesn't just fetch data — it **delivers it into the blockchain** with guarantees of reliability.

### Can I use just one oracle?

You can, but it's risky. A centralized oracle is a single point of failure. DeFi protocols typically use decentralized networks like Chainlink.

### Do I have to pay for oracles?

Yes. A smart contract pays a fee to oracle nodes for providing data. In Chainlink's case, the fee is paid in LINK tokens.

### Can an oracle be wrong?

It can. Even decentralized oracles aren't perfect. But the more independent data sources you have — the lower the chance of error.
