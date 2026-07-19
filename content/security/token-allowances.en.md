---
weight: 30
title: "Token Allowances: What They Are and Why They're Dangerous"
description: "What token allowances are, why unlimited approvals are dangerous, and how to revoke them using Etherscan or Revoke.cash to protect your crypto wallet."
category: "security"
translationKey: "token-allowances"
slug: "token-allowances-explained"
keywords:
  - token allowance
  - token approval
  - revoke approval
  - smart contract risk
  - Ethereum approval
  - ERC20 approval
---

## Token Allowances: What They Are and Why They're Dangerous

---

**"Confirm access to your USDT"** — you've probably seen this message when connecting your wallet to a new DeFi service, DEX (Uniswap, PancakeSwap), or NFT marketplace.

Many people click "Confirm" without even reading it. And that can cost you every single token in your wallet.

In this article, we'll cover:

>- what token allowances are;
>- why **unlimited approvals** are one of the biggest security holes out there;
>- how to check which dApps have access to your tokens;
>- how to revoke an approval if you've accidentally given one.

---

## What Is a Token Allowance

### How ERC-20 Tokens Work

To understand allowances, you first need to understand how tokens actually work.

The **ERC-20** standard (and its cousins BEP-20, TRC-20, etc.) is a smart contract with two key functions:

- `transfer(from, to, amount)` — moves tokens;
- `approve(spender, amount)` — lets another address spend your tokens.

With a normal transfer, you sign the transaction yourself. But when you interact with a DeFi app, the contract needs to **pull** tokens from you on its own.

Here's how it works under the hood:

1. You call `approve(DEX_contract, 1000 USDT)`;
2. Now the DEX contract can call `transferFrom(your_address, pool, 1000 USDT)`;
3. The swap happens without you having to sign every step.

👉 **That's a token allowance** — you give a smart contract permission to move your tokens.

---

### A Real-World Analogy

Imagine you give your neighbor the keys to your apartment so they can feed your cat while you're away.

A token allowance is the same thing, just virtual. You let a contract take a specific amount of tokens (or all of them) and do whatever it wants with them.

---

## Why It's Dangerous

### Unlimited Allowances

The biggest problem: most dApps don't ask for a **limited** approval — they ask for an unlimited one:

```
approve(DEX, MAX_UINT_256)
```

`MAX_UINT_256` is the largest number in Ethereum (2²⁵⁶ − 1). Practically infinite.

Why do dApps do this?

- **convenience** — no need to confirm every single trade;
- **cheaper** — one `approve` transaction instead of several;
- **it's the de facto standard** in DeFi.

But the price of that convenience is **your tokens being held hostage**.

---

### What Could Go Wrong

If a contract you gave unlimited approval to:

- **gets hacked** — the attacker can drain every last token;
- **gets upgraded** — the contract owners can add a function that takes everything;
- **turns out to be malicious** — your funds vanish instantly.

Real-world examples:

| Event             | Losses           | Cause                                    |
|-------------------|------------------|------------------------------------------|
| Poly Network Hack | $610 million     | Cross-chain bridge exploit               |
| BadgerDAO         | $120 million     | Phishing approve on a malicious contract |
| Curve Finance Hack| $570,000         | DNS-based allowance manipulation         |

> **Important:** an attacker doesn't need your seed phrase or private key. All they need is for you to have signed an `approve` on a malicious contract at some point — and that's it, your tokens are theirs.

---

### You Don't Remember Who You Gave Access To

If you're active in DeFi, over the months and years you'll pile up a dozen or more allowances: Uniswap, OpenSea, 1inch, some random test dApps you've already forgotten about.

Here's the question: do you actually remember which contracts you've approved?

If you said "no" — you're not alone. And that's totally normal. But **those "forgotten" allowances are exactly what hackers go after**.

---

## How to Check Which dApps Have Access to Your Tokens

### Etherscan

The most straightforward way:

1. open [Etherscan.io](https://etherscan.io);
2. paste your wallet address;
3. go to the **"Token Approvals"** tab (or just "Approvals");
4. you'll see a list of contracts and how much they're allowed to spend.

For BSC, use [BscScan.com](https://bscscan.com) — the interface is the same.

---

### Revoke.cash

A more convenient option is [Revoke.cash](https://revoke.cash):

1. connect your wallet (MetaMask, WalletConnect);
2. the site will show **all your active approvals** across every network;
3. for each approval you'll see: the contract, the token, and the limit.

The service doesn't store your data and doesn't charge a fee — you simply sign the revoke transactions through your own wallet.

---

### Other Tools

- **Zapper.xyz** — dashboard with an "Approvals" section;
- **DeBank.com** — shows approvals in your wallet profile;
- **Rabby Wallet** — built-in approval detector;
- **Token Approval Checker** — a simple checker for a single token.

---

## How to Revoke an Approval

### Via Revoke.cash

1. open [Revoke.cash](https://revoke.cash);
2. select the network (Ethereum, Arbitrum, Optimism, BSC, etc.);
3. click **"Revoke"** next to the approval you want to remove;
4. confirm the transaction in your wallet.

Done. The contract can no longer spend your tokens.

---

### Via Etherscan

1. find the token whose approval you want to revoke;
2. open the token's contract on Etherscan;
3. go to **"Contract" → "Write Contract"**;
4. connect your wallet;
5. find the `approve` function and set:
   - `spender` — the address of the contract you approved;
   - `amount` — **0** (resets the allowance);
6. sign the transaction.

👉 **Tip:** use Revoke.cash — it's simpler and safer (less chance of messing up an address).

---

### Important Things to Know When Revoking

- each `approve` to 0 is a **gas transaction** — you'll have to pay the fee;
- if you revoke an approval for a DEX you actively trade on, you'll have to approve again the next time you make a swap;
- after revoking, your tokens stay in your wallet — nothing gets lost.

---

## Best Practices: How to Stay Safe

### Approve Only What You Need

Instead of an unlimited approval, specify the **exact amount** you're about to swap or use.

Most wallets and dApps let you change the amount in the confirmation window:

- **MetaMask:** before signing the `approve`, tap on the amount and enter a **specific number**;
- **Rabby Wallet:** automatically suggests a limited approval.

👉 **Always check how much you're letting a contract spend.**

---

### Use a Separate Wallet for DeFi

Create a "hot" wallet that holds:

- only the amount you're willing to risk;
- no more than 5–20% of your total portfolio.

Keep your main funds on a **cold wallet** (Ledger, Trezor) or in a separate address that dApps don't have access to.

---

### Check Your Approvals Regularly

Make it a habit to do this once a month:

1. go to [Revoke.cash](https://revoke.cash);
2. check which contracts have access;
3. revoke anything you're not actively using.

If you haven't touched a dApp in 3+ months — revoke the approval.

---

### Be Cautious With New dApps

Before you give an approval:

- check the contract on [DexScreener](https://dexscreener.com) or [Dune Analytics](https://dune.com);
- see how long the project has been around;
- look for a smart contract audit;
- search [Twitter](https://x.com) for other users' feedback.

If a dApp asks you to approve **all your tokens** right away and won't let you trade without it — that's a **red flag**.

---

### Takeaways

Token allowances are a core DeFi mechanic — without them, swaps, liquidity pools, and NFT marketplaces wouldn't work.

But they're also **the most popular attack vector**:

>- unlimited approvals are the norm, not the exception;
>- forgotten allowances are a ticking time bomb;
>- one wrong "Confirm" click, and all your tokens go straight to an attacker.

The safety rules are simple:

>- approve only the amount you need;
>- use a separate wallet for DeFi;
>- check your approvals once a month on [Revoke.cash](https://revoke.cash);
>- don't sign `approve` without looking.

**Crypto gives you control over your money. But that control needs to be exercised — not handed out left and right.**

---

## FAQ

### What's a token allowance in plain English?
It's permission you give a smart contract to spend your tokens. Think of it like handing over the keys to your safe — the contract can take as much as you've allowed.

### Why is unlimited approval dangerous?
If the contract gets hacked or turns out to be malicious, the attacker can drain **all** your tokens with a single click.

### How do I revoke an approval?
The easiest way is through [Revoke.cash](https://revoke.cash) — connect your wallet and hit "Revoke" for any approvals you don't need.

### Do I need to revoke approval after every trade?
Not necessarily — but if you don't plan to use that dApp anymore, it's a good idea to revoke it.

### Will I lose my tokens when I revoke an approval?
No. The tokens stay right in your wallet. Revoking just takes away the contract's permission to move them.
