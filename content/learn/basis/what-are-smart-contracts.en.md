---
weight: 155
title: "Smart Contracts: What They Are and How They Work"
description: "Smart contracts explained simply: what are smart contracts, where they are used, how they work on Ethereum, and what the risks are"
category: "basis"
translationKey: "what-are-smart-contracts"
slug: "what-are-smart-contracts"
keywords:
  - smart contracts
  - Ethereum
  - DeFi
  - dApps
  - decentralized applications
  - blockchain programming
  - Solidity
  - crypto basics
---

## What Is a Smart Contract?

A smart contract is a program that lives on the blockchain and runs **automatically** — no humans needed. You set the rules, and they execute without courts, lawyers, or middlemen.

Think of a vending machine. You drop in a coin, press a button, and get a soda. Nobody checks your ID, nobody signs a contract. The machine just runs its program.

A smart contract works the same way — but instead of soda, it handles money, tokens, and digital assets.

> **Short version:** A regular contract = paper + signature + court.  
> A smart contract = code + blockchain + automatic execution.

## How a Smart Contract Works — A Simple Example

Say you want to bet a friend $100 that it will rain tomorrow.

**The usual way:**  
You agree verbally. Tomorrow someone loses but "forgets" to pay. You go to court — it takes months. In the end you spend more on lawyers than you won.

**With a smart contract:**  
1. You both send $100 to the smart contract's address.
2. Tomorrow the contract checks weather data (through an **oracle** — a mechanism that delivers real-world data to the blockchain).
3. If it rained — the contract sends all $200 to whoever bet on rain. If not — to the other person.
4. Nobody can change their mind or refuse to pay. The code executes automatically.

This is a simplified example, but the idea is the same: **smart contracts replace trust with code**.

## Where Are Smart Contracts Used?

Smart contracts are the backbone of the entire crypto industry beyond simple transfers. Here's where they actually work:

### DeFi (Decentralized Finance)

The most widespread use. DeFi protocols are collections of smart contracts that replace banks:

- **Currency exchange** — you swap USDT for ETH on Uniswap without a middleman. The contract finds the rate and executes the trade.
- **Loans** — you send ETH as collateral, the contract lends you USDC. If the collateral drops in price — the contract automatically sells it (liquidation).
- **Yield farming** — you lock tokens in a liquidity pool, the contract accrues interest every second.

In traditional finance, all this is handled by people: managers, tellers, lawyers. In DeFi — smart contracts.

### NFTs (Non-Fungible Tokens)

Every NFT is a record in a smart contract. When you buy an NFT, the contract:
1. Checks you have enough funds
2. Transfers payment to the seller
3. Records you as the new owner
4. Pays royalties to the creator (a percentage of resale)

### DAOs (Decentralized Autonomous Organizations)

Smart contracts manage the organization's treasury without a CEO. Members vote with tokens, and the contract automatically executes the decision:

- "Voted to allocate 10,000 USDT for marketing" → the contract sends the funds
- "Voted to change the interest rate" → the contract adjusts protocol parameters

### Tokens

When you create a new token (USDT, UNI, SHIB, or any other), it's not magic — it's a smart contract following the ERC-20 (on Ethereum) or BEP-20 (on BSC) standard. The contract stores all holders' balances and authorizes transfers.

> Fact: the most popular smart contract is USDT Tether. It processes billions of dollars every day.

## Smart Contracts on Ethereum

Ethereum was the first platform to make smart contracts mainstream. Bitcoin only lets you send coins. Ethereum lets you program any rules.

**Ethereum's key idea:** not just "Alice sent Bob 5 ETH," but "IF the condition is met, THEN execute the action."

Ethereum smart contracts are written in **Solidity**, which looks similar to JavaScript but runs on the blockchain. Anyone can read a contract's code — all smart contracts are open source by default.

### Gas: Why Every Operation Costs Money

Every smart contract action requires computing resources. All computers in the network (nodes) must execute the code and verify the result. You pay for this with **gas** — a fee in ETH.

A complex operation (like a Uniswap swap) costs more than a simple one (sending ETH). The more people use the network, the higher the gas.

## Advantages of Smart Contracts

**Transparency** — the contract's code is visible to everyone. You can check what will happen to your money before you send it.

**Immutability** — once published on the blockchain, the contract cannot be changed. Nobody can add rules retroactively.

**No middlemen** — no banks, lawyers, or notaries needed. The contract executes the conditions itself.

**24/7 Availability** — the contract runs around the clock, no weekends or breaks. Nobody can say "come back tomorrow" or "the teller is on lunch."

**Automation** — payments, interest accrual, revenue distribution — everything can run automatically.

## Risks of Smart Contracts

Smart contracts aren't perfect. Here are the main risks:

### Bugs in Code

Humans write code — humans make mistakes. If a contract has a bug, a hacker can exploit it.

**Example:** the 2016 DAO hack. A hacker found a vulnerability in the code and drained 3.6 million ETH (~$50 million at the time). This forced Ethereum to hard fork — splitting into Ethereum and Ethereum Classic.

There are thousands of such cases. Protocols get hacked for millions of dollars every month — almost always due to bugs in smart contracts.

### Immutability — A Double-Edged Sword

If you made a mistake in the contract, you can't just "ask to fix it." The contract lives its own life. That's why contracts undergo **audits** — code reviews by security experts — before launch.

### Oracles — The Weak Link

A smart contract can't check the Bitcoin price or the weather on its own. This data comes from **oracles** — external services. If an oracle sends wrong data (or gets hacked), the contract executes based on false information.

### Frontrunning

When you send a smart contract transaction, it enters the mempool (the queue of unconfirmed transactions). Bots can spot it, pay higher gas, and execute their own transaction before yours. This is called frontrunning — and it's legal.

## How to Check a Smart Contract Before Using It

1. **Look for an audit** — reputable protocols publish audits by firms like Trail of Bits, OpenZeppelin, or Certik. No audit? Don't send money.
2. **Check the contract's age** — if a contract is a month old, has millions in TVL, and no audit — that's a red flag.
3. **Read the code** — if you can, check the code on Etherscan. If not, stick with projects the community trusts.
4. **Check approvals** — when you sign a smart contract transaction, you often give it permission to spend your tokens. Use [token allowances](/en/security/token-allowances-explained/) — revoke permissions from contracts you no longer use.

## The Future of Smart Contracts

Smart contracts aren't just a crypto gimmick. They're a new form of digital agreement that's gradually entering the real world:

- **Insurance** — a contract automatically pays compensation when your flight is delayed.
- **Real estate** — smart contracts can handle property sales without a notary.
- **Royalties** — musicians get paid automatically every time their track is played.
- **Voting** — contracts can provide transparent vote counting without fraud.

Most of these applications are still experimental. But the technology is advancing, and in 5-10 years smart contracts could be as ordinary as email.

## Key Takeaways

- A smart contract is a program on the blockchain that runs without human intervention
- They power DeFi, NFTs, DAOs, and tokens
- Ethereum is the main platform for smart contracts
- The biggest risk is bugs in code and vulnerabilities
- Always check audits and approvals before using any dApp (decentralized application)
