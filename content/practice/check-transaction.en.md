---
weight: 6
title: "How to Check a Transaction in the Blockchain"
description: "How to check a crypto transaction using Etherscan and blockchain explorers. Learn about transaction status, confirmations, gas fees, and contract interactions."
category: "practice"
translationKey: "check-transaction"
slug: "check-transaction-in-blockchain"
keywords:
  - Etherscan
  - blockchain explorer
  - check transaction
  - transaction status
  - TxID
  - wallet tracking
prev: "/en/practice/first-transaction-without-mistakes"
next: "/en/exchanges"
---

## How to Check a Transaction in the Blockchain: Everything You Need to Know

---

You sent some crypto. The money left your wallet. But did it actually reach the recipient?

In the banking world, you just wait for an SMS or a push notification. In crypto, things are way more transparent:

> **Every transaction is a public record that anyone can verify.**

And you don't need bank support or access to someone else's account. All you need is one tool — a **blockchain explorer**.

In this article we'll cover:
- how to find any transaction by its ID;
- what the Success, Pending, and Failed statuses mean;
- how to read the details: block, fee, from where to where;
- which explorers work for different networks;
- how to set up wallet monitoring.

---

## What Is a Blockchain Explorer and Why Do You Need It

A **blockchain explorer** is like "Google for the blockchain." A public website that shows everything happening in the network:

- every transaction;
- every wallet and its balance;
- every block and its contents.

Unlike a bank where you only see your own activity, in the blockchain **everything is visible**. The data is just encoded into addresses — no link to your identity.

You need an explorer when:

| Situation | Why check it |
|-----------|--------------|
| You sent money, the recipient says "didn't get it" | Show the TxID — proof of sending |
| A transaction is stuck | Check the status and number of confirmations |
| You want to verify an address is correct | Look at the wallet's history and balance |
| A scammer sent a fake transfer | Check whether the transaction actually exists on the blockchain |

---

## Etherscan: The Main Ethereum Explorer

**Etherscan** ([etherscan.io](https://etherscan.io)) is the most popular blockchain explorer. It works for the Ethereum network and all ERC-20 standard tokens.

### Transaction Hash (TxID)

Let's walk through a random example. I found an interesting transaction — we'll use it to break down all the details:  
`TxID: 0x6f6fd3e8018516ff5e60bfcc2c4fd01be74a877f6b4fac1705651623ad7d70cd`

1. Go to [etherscan.io](https://etherscan.io).
2. **Paste the TxID** into the search bar (top center of the page).
3. Hit Enter.

Within a second you'll see the full transaction details.

Think of it as a "receipt number." Copy it and send it to the recipient — it's official proof of the transfer.

### What Etherscan Shows

Here's what you'll see on the transaction page:

#### Status

| Status | What it means |
|--------|---------------|
| ✅ **Success** | Transaction executed, funds credited |
| ⏳ **Pending** | Waiting — not yet included in a block |
| ❌ **Failed** | Error — transaction didn't go through (gas fee burned) |

> **Important:** Failed ≠ lost money. If the transaction failed, the funds return to the sender (minus the gas fee).

#### Block

The block number the transaction was included in.  
For example:  
`Block: `**`25093288`**` 22 Block Confirmations`

The more blocks **confirmed**, the safer the transaction:

| Network | Minimum confirmations for safety |
|---------|----------------------------------|
| Bitcoin | 3–6 |
| Ethereum | 12–32 |
| Solana | 1 (very fast finalization) |

#### From / To

- **From** — the sender's address.  
`From: 0x56Eddb7aa87536c09CCc2793473599fD21A8b17F (Binance 17)`
- **To** — the recipient's address (or contract address).  
`To: 0x42008C6392F552fcFF9abbf310E4421eEd22fAF9`

> \* *Binance 17* — **Etherscan** identified the wallet address as belonging to the Binance exchange. This info isn't on the blockchain itself, but the site's analytics make that connection.

Click on any address — you'll see its full history and balance.

#### Value

The transfer amount: `0 ETH ($0.00)` because it was a token transfer (ERC-20): `6,000,000.25342 ($5,997,252.25) Tether USD (USDT)`.

#### Transaction Fee (Gas Fee)

The fee paid for the transaction. Shows two numbers:

- **Transaction Fee** — how much gas was actually used;  
`Transaction Fee: 0.000063066067464358 ETH ($0.14)`
- **Gas Price** — the price per unit of gas (in Gwei);  
`Gas Price: 1.367404598 Gwei (0.000000001367404598 ETH)`

There you go. Sent $6,000,000 and paid $0.14 in fees.

#### Gas Limit

The maximum gas you were willing to pay and how much was actually used.  
`Gas Limit & Usage by Txn: 220,436 | 46,121 (20.92%)`

---

## List of Explorers

Every blockchain network has its own explorer. Here are the most popular ones:

### Ethereum (ERC-20)

- **Etherscan** — [etherscan.io](https://etherscan.io) — the main Ethereum explorer.
- **Etherscan for Sepolia testnet** — [sepolia.etherscan.io](https://sepolia.etherscan.io) (handy for practice).

### BNB Chain (BEP-20)

- **BscScan** — [bscscan.com](https://bscscan.com) — the full Etherscan equivalent for Binance Smart Chain.  
The interface is almost identical — same statuses, blocks, fees.

### Solana

- **Solscan** — [solscan.io](https://solscan.io) — the main explorer for Solana.

Solana quirk: transactions confirm in **milliseconds**. The Pending status is practically non-existent here.

### TRON (TRC-20)

- **Tronscan** — [tronscan.org](https://tronscan.org) — the official Tron network explorer.  
Popular for USDT — many people use Tron because of low fees.

### Bitcoin

- **Blockchain.com** — [blockchain.com/explorer](https://www.blockchain.com/explorer) — the most well-known BTC explorer.
- **Mempool.space** — [mempool.space](https://mempool.space) — advanced explorer with transaction queue visualization (mempool).

### Universal Search

- Bitcoin and Litecoin — [bitaps.com](https://bitaps.com/) — an alternative explorer.

---

## How to Monitor a Wallet: Alerts and Notifications

You don't have to check every transaction manually. Explorers can notify you about wallet activity.

### Setup on Etherscan

1. Register on [etherscan.io](https://etherscan.io) (free).
2. Go to **"Watch List"** → **"Add Address"**.
3. Paste the wallet address you want to track.
4. Set up notifications:
   - **Email** — get an email on any incoming/outgoing transaction;
   - **Telegram** — via the Etherscan Alert Bot.

### Similar Features in Other Explorers

- **BscScan** — same Watch List system, email notifications.
- **Solscan** — click **"Subscribe"** on the address page.
- **Tronscan** — the **"Follow"** button on the wallet page.

### Third-Party Monitoring Services

- **Dextools** ([dextools.io](https://dextools.io)) — track transactions by token and liquidity pool.
- **Nansen** ([nansen.ai](https://nansen.ai)) — professional wallet analytics tool (paid).
- **Telegram bots** — tons of bots track "whales" and large transactions in real time.

> Tip: if you're expecting an important transfer, set up an alert in the explorer. You'll get notified **before** the recipient even says "it arrived."

---

## How to Check a Transaction on an Exchange (CEX)

If you're moving crypto **from an exchange** to an external wallet or vice versa, the process is slightly different:

1. Find the **TxID** in the exchange's transaction history (usually under "History" → "Deposits/Withdrawals").
2. Copy the TxID.
3. Open the explorer for the right network and paste the TxID.

> **Important:** Exchanges often show their own internal TxID for in-house transfers. If you were sending **between users on the same exchange** — there's no blockchain transaction, it's just a database entry on the exchange's side.

### How to Tell an Internal Transfer from a Blockchain Transaction

| Transfer type | Has a TxID? | Can you check in an explorer? |
|---------------|-------------|-------------------------------|
| Inside the exchange (User A → User B on Binance) | Yes, but internal | ❌ No |
| From exchange to external wallet | Yes, a real TxID | ✅ Yes |
| From wallet to exchange | Yes | ✅ Yes |

---

## What to Do If a Transaction Gets Stuck

**Pending** status can last anywhere from a few seconds to several days. Here's what's happening and what you can do.

### Why Transactions Get Stuck

- **Low gas fee.** In networks like Ethereum, miners process the highest-fee transactions first. If you set the gas too low — the transaction sits in the queue.
- **Network congestion.** During hype moments (e.g. a popular NFT drop), the queue can get massive.
- **Node issues.** Rare, but sometimes a specific validator slows things down.

### What You Can Do

1. **Wait.** If the network isn't critically congested, the transaction will go through — just slowly.
2. **Speed it up (Replace-by-Fee).** Some wallets (MetaMask, Trust Wallet) have a **"Speed Up"** option — you resend the same transaction with a higher fee.
3. **Cancel.** If your wallet supports **"Cancel"**, you can replace the stuck transaction with an empty one using a higher gas fee.

> **If the transaction is still Pending after 24 hours** — it will most likely "fall off" (never make it into a block), and the funds will return.

### When to Panic (Spoiler: Almost Never)

| Status | Should you worry? |
|--------|-------------------|
| Pending (up to 30 min) | No, that's normal |
| Pending (1–6 hours) | Worth checking the gas and network |
| Pending (over 24 hours) | Transaction likely won't go through — funds will return |
| Success | ✅ Consider the transfer complete |
| Failed | ❌ Funds returned (minus gas fee) |

---

## Checklist: What to Check After Sending

When you've sent crypto, run through this list:

| # | Step | What to look for |
|---|------|------------------|
| 1 | Copy the TxID from your wallet | Make sure it's not an empty string |
| 2 | Open an explorer (Etherscan, etc.) | Paste the TxID into the search |
| 3 | Check the status | ✅ Success = done |
| 4 | Verify the amount (Value) | Does it match what you sent? |
| 5 | Check the recipient address (To) | Did you send it to the right place? |
| 6 | Look at the number of confirmations | The more — the safer |
| 7 | Send the TxID to the recipient | This is proof of the transfer |

---

## Frequently Asked Questions

### Can I check a transaction without a TxID?

Yes, if you know the **sender or recipient address**. Paste the address into the explorer's search — you'll see **all its transactions** and can find the right one by amount, date, or hash.

### How do I verify whether a scammer sent a real transfer?

Scammers often send screenshots or PDFs with "proof" of a transfer. The only way to check:

1. Ask for the TxID.
2. Paste it into an explorer.
3. If there's no transaction — it's fake.

### What are confirmations?

Each new block added after the block containing your transaction gives **+1 confirmation**. The more confirmations, the harder it is to reverse the transaction.
- For small amounts: 1–3 confirmations are enough.
- For large amounts: 6+ confirmations.
- For Bitcoin, exchanges usually wait for 3–6 confirmations.

### Why was the fee charged even though the transaction failed?

Gas is payment for **computation**, not for success. If a transaction failed (e.g., insufficient token balance), the miner still executed the code and earned the fee. The funds **return** to your wallet, but the gas is burned.

### Can I cancel a transaction that's already been sent?

No. If a transaction is confirmed (Success), it's **permanently** recorded on the blockchain. No one — not the developer, not a miner, not a government — can undo it.

---

## Summary

Checking a transaction on the blockchain is a superpower that traditional finance doesn't give you:

- You can see **every** operation publicly and transparently.
- You don't need to call support or wait for a reply.
- The TxID is legally meaningful proof of a transfer.
- You can track any wallet in real time.

Just remember three things:

1. **TxID = receipt number.** Save it after every send.
2. **Explorers are free.** Etherscan, BscScan, Solscan, Tronscan — any of them at your fingertips.
3. **Success status = money arrived.** If the status is Success, nothing else matters.

Crypto gives you **full control and full transparency**. Checking a transaction is the first step to feeling confident in this world.
