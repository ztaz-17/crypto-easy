---
weight: 210
title: "What Happens When You Send Crypto"
description: "Behind the scenes of a crypto transaction: creation, signing, broadcast, mempool, confirmation. What actually happens under the hood from click to completion."
category: "how-it-works"
translationKey: "what-happens-when-you-send-crypto"
slug: "what-happens-when-you-send-crypto"
keywords:
  - crypto transaction
  - how crypto works
  - blockchain transaction
  - transaction signing
  - mining
  - confirmation
  - broadcasting
---

## What Happens When You Send Crypto

---

You open your wallet, type in the recipient's address, enter the amount — and hit "Send."

Did the money go? Not yet.

A message appears on your screen: "Transaction sent. Waiting for confirmation..."

And that's where the real action begins.

What happens next is an intricate dance between your wallet, thousands of computers around the world, and the math that keeps the system honest.

> In this article, we'll break down every stage: from the moment you click "Send" to the coins landing in the recipient's wallet.

Let's take a look at what really happens when you send crypto.

---

## Stage 1: Creating the Transaction

It all starts with your wallet gathering data. It builds a digital "package" — a transaction. Inside this package:

- **from** — your public address;
- **to** — the recipient's address;
- **amount** — how much you're sending;
- **fee** — what you're paying the network for processing.

The transaction hasn't been sent yet. It's just a draft — a bundle of data that only exists on your device.

### What's important to know

Your wallet doesn't "pull" money from some account. Instead, it looks through the entire history of previous transactions that ever came to your address and picks out unspent balances.

Think of it like having several different bills in your pocket, and you choose which one to pay with. In crypto, those "bills" are records on the blockchain.

> For more on how addresses and keys work, check the glossary: [public address](/en/glossary/#public-address), [private key](/en/glossary/#private-key).

---

## Stage 2: Signing the Transaction

Now for the most important part.

Your wallet takes the transaction data and signs it with your **private key**. It's like putting your personal digital stamp on it — one that can't be forged.

### Why signatures can't be faked

Your private key is a long random string of characters. Only you know it. The network only knows your public address — a derivative of that key.

When you sign a transaction:

1. Your wallet applies a mathematical formula to the transaction data and your key.
2. The result is a **digital signature** — a unique string of characters.
3. Any network participant can verify this signature using your public address.
4. But nobody can reverse-engineer your private key from the signature.

> **Important:** your private key is never sent anywhere. It stays on your device. The network verifies the signature without ever seeing the key itself.

If anyone tries to change the amount in a signed transaction — the signature becomes invalid. The network rejects it immediately.

That's the magic: you prove you own the funds without revealing your secret.

---

## Stage 3: Broadcasting Across the Network

The transaction is signed. Now it needs to reach the network.

Your wallet sends the transaction to one or more network nodes — **nodes**. A node is a computer running a full blockchain client. It stores the entire transaction history and checks new ones.

### What a node checks

When a node receives your transaction, it verifies:

- the signature is correct;
- you have enough funds;
- you're not trying to spend the same coins twice (double-spending).

If everything checks out — the node adds the transaction to the **mempool** (short for memory pool). This is the holding area for unconfirmed transactions.

### The mempool — a waiting room

Think of a train station. Your transaction is a passenger waiting to board a train (a block). There are lots of passengers, the train leaves only once every 10 minutes (in Bitcoin's case), and seats are limited.

Who gets on the train? The ones who paid for a ticket — that is, the fee. The higher the fee, the sooner your transaction gets picked for a block.

> If the fee is too low, your transaction could wait hours or even days. At any given time, the mempool can hold tens of thousands of unconfirmed transactions.

After verification, the node **relays** (broadcasts) the transaction to its neighbors. They relay it to theirs. In seconds, the transaction spreads across the globe.

---

## Stage 4: Confirmation in a Block

The transaction is in the mempool. Now it needs to be confirmed by a **miner** (in Bitcoin) or a **validator** (in Ethereum and other PoS networks).

### How miners choose transactions

Miners collect transactions from the mempool and package them into a block. Priority depends on the fee — the higher the fee, the higher the priority.

Once the block is assembled, the miner starts solving a mathematical puzzle (Proof of Work) to seal the block. This requires massive computing power. Whoever solves it first gets:

- the block reward (newly minted coins);
- all the fees from the included transactions.

As soon as a block is found, the miner broadcasts it to all nodes. The nodes verify the block and, if everything's correct, add it to their chain.

### How long to wait for confirmation

For Bitcoin, one confirmation means your transaction made it into a block. But people usually wait for several confirmations (the more, the safer):

| Network | Block time | How many to wait |
|---------|-----------|-----------------|
| Bitcoin | ~10 minutes | 3 blocks (~30 min) |
| Ethereum | ~12 seconds | 12–30 blocks (~2–6 min) |
| Solana | ~400 ms | 1 block (instant) |

> Why not just one confirmation? Because in theory, a miner could produce an alternative block (a fork). The more blocks come after yours, the harder it is to reverse the transaction. After 6 confirmations on Bitcoin, a reversal is practically impossible.

---

## Summary table: stages of a transaction

Here's the complete journey a transaction makes from clicking "Send" to final confirmation:

| Stage | What happens | Who's involved | Time |
|-------|-------------|---------------|------|
| 1. Creation | Wallet prepares the data: from, to, amount | Your wallet | Instant |
| 2. Signing | Transaction is signed with your private key | Your wallet | Instant |
| 3. Broadcasting | Transaction is sent to nodes, lands in the mempool | Nodes, mempool | Seconds–minutes |
| 4. Confirmation | Miner/validator adds the transaction to a block | Miners/validators | Minutes–hours |
| 5. Finalization | Block is added to the chain, transaction is complete | All network nodes | A few more blocks |

---

## What about fees?

The fee is payment for a spot in a block. It has two parts:

- **base fee** — the baseline rate set by the network;
- **priority fee** — what you voluntarily add to speed things up.

In Bitcoin, the fee isn't based on the amount you're sending — it's based on the **transaction size in bytes**. The more complex the transaction (lots of inputs/outputs), the "heavier" and more expensive it is.

In Ethereum, the fee depends on the operation's complexity (gas). A simple transfer costs about 21,000 gas. Interacting with a smart contract can cost hundreds of thousands.

> Learn more: [network fee](/en/glossary/#network-fee), [gas](/en/glossary/#gas).

---

## What does the recipient see?

The recipient can see the transaction as soon as it's broadcast — even before confirmation.

Their wallet may show a "Pending" status. The coins haven't arrived yet, but it's clear a transfer is on its way.

After the first confirmation, the balance updates. Exchanges and services typically credit funds after a certain number of confirmations — for safety.

---

## What can go wrong?

### Stuck transaction

If the fee is too low, miners may ignore your transaction. It stays in the mempool and waits.

On Bitcoin, such transactions can sit there for days. On Ethereum, there's a Replace-by-Fee mechanism — you can resend the same transaction with a higher fee.

### Rejected transaction

If the network is congested and your fee is minimal, the transaction may get "evicted" from the mempool and returned unspent. Your money doesn't disappear — it goes back to your address.

### Canceled transaction

You can't cancel a signed and sent transaction. That's the nature of the blockchain — the record is immutable. If you sent to the wrong address, only the recipient can return the coins.

> Always double-check the address before sending. At minimum, the first 4 and last 4 characters.

---

## Conclusion

When you hit "Send," a whole chain of events kicks off:

1. **Creation** — your wallet prepares the data.
2. **Signing** — your private key proves it's your money.
3. **Broadcasting** — the transaction zips across the network into the mempool.
4. **Confirmation** — a miner includes it in a block.
5. **Finalization** — the block becomes a permanent part of the blockchain.

This entire system works without banks, without middlemen, without a single central authority. Just math, thousands of independent computers, and your private key.

> Crypto isn't about magic. It's about math — the kind that gives you control over your own money.

---

## FAQ

### Can I cancel a transaction after sending it?
No. Once a transaction is signed and sent to the network, it cannot be canceled. Only the recipient can send the funds back. Always verify the address.

### Why do some transactions go through in minutes while others take hours?
It all comes down to the fee and network congestion. During peak times, miners pick transactions with the highest fees. If yours is low — you wait.

### What happens if I send coins to a nonexistent address?
Most likely, the network will reject the transaction. But if the address exists and simply belongs to nobody (or to someone else), the coins will go there with no way to recover them.

### What is double-spending?
It's an attempt to send the same coins to two different recipients. The blockchain prevents this through consensus: the first confirmed transaction is considered valid, and the second one is rejected.

### How can I check the status of my transaction?
Use a blockchain explorer. For Bitcoin — [mempool.space](https://mempool.space), for Ethereum — [etherscan.io](https://etherscan.io). Paste your transaction hash, and you'll see everything: from the mempool to the final confirmation.
