---
weight: 130
title: "Loans Without Banks: How DeFi Lending Works"
description: "How crypto loans work through DeFi without a bank: collateral, liquidation risks, and whether borrowing against your crypto is a smart move for beginners."
category: "defi"
translationKey: "crypto-loans"
slug: "crypto-loans-without-banks"
keywords:
  - DeFi loans
  - crypto lending
  - Aave
  - Compound
  - collateral
  - liquidation
  - overcollateralization
---

## DeFi Loans: How to Borrow Without a Bank or Credit History

---

Picture this: you need money fast, but the bank turns you down because of a bad credit score. Or maybe you want to take out a loan but don't feel like going through [KYC](/en/glossary/#kyc) and filling out endless forms.

In [DeFi](/en/glossary/#defi), that's not a problem.

> **A crypto loan** is money you borrow against your crypto as collateral — without a single question about your credit history.

No proof of income, no calls from the bank, no waiting for approval. The code handles everything.

In this article, we'll cover:

> - how DeFi loans work;
> - why you have to put up more collateral than you borrow;
> - what liquidation is and how to avoid it;
> - the main risks;
> - real examples: Aave, Compound, MakerDAO.

---

## How a DeFi Loan Works

In the traditional world, getting a loan looks like this:

- you prove to the bank that you can pay back the money;
- the bank checks your credit history and income;
- if everything checks out — they give you the cash.

[DeFi](/en/glossary/#defi) works completely differently:

> **you don't prove you're solvent — you put up collateral.**

The process is simple:

1. You deposit crypto (say, ETH) into a smart contract;
2. The smart contract lets you borrow a different [cryptocurrency](/en/glossary/#cryptocurrency) (like USDC);
3. You use the borrowed funds;
4. When you pay back the loan plus interest — your collateral is unlocked.

> The key difference: **a loan is issued not by a person or a company, but by code.**

Nobody asks where you work or how much you earn. Just connect your [wallet](/en/glossary/#wallet) and deposit collateral.

---

## Overcollateralization: Why You Need to Put Up More Than You Borrow

There are no debt collectors or courts in DeFi. If a borrower doesn't repay, a smart contract can't take them to court.

That's why the system works differently:

> **the collateral must be worth more than the loan amount.**

This is called **overcollateralization**.

Here's how it looks in practice:

- you want to borrow $1,000 in USDC;
- the protocol requires at least $1,500 in collateral (150%);
- you deposit $1,500 worth of ETH;
- you receive $1,000.

Why 150% exactly? It's a buffer against volatility. If ETH drops 30%, there's still enough collateral to cover the loan.

### Typical Levels

| Protocol    | Max borrow (LTV)         | Example                            |
|-------------|--------------------------|------------------------------------|
| Aave        | 50–75% of collateral    | On $100 ETH you can borrow $50–75 |
| Compound    | 50–75%                  | Similar                            |
| MakerDAO    | 66% (150% overcollateral)| On $100 ETH you can mint ~$66 DAI |

The more volatile the asset — the lower the LTV (loan-to-value), meaning the less you can borrow against it.

---

## Liquidation: When Your Collateral Drops in Value

The single most important thing to know about DeFi loans:

> **if your collateral's price falls too low — you lose it.**

This is called **liquidation**.

### How It Works

Say you deposited $1,500 worth of ETH and borrowed $1,000 USDC. Your health factor is 1.5.

If ETH's price drops:

- $1,500 → $1,300 — still safe;
- $1,300 → $1,100 — health factor is dropping;
- $1,100 → $1,050 — critical threshold.

As soon as the health factor hits 1 (or lower, depending on the protocol), an **automatic liquidation** triggers:

> the smart contract sells part of your collateral to cover the debt.

A **penalty** is added to the liquidation amount — typically 5–15% of the sum. This is the risk fee paid to liquidators (usually bots that monitor positions).

### How to Avoid Liquidation

1. **Don't borrow the max.** If you can take $75 on $100 — borrow $40–50. The smaller the debt, the bigger your safety margin.
2. **Watch the price.** On volatile days, check your health factor every few hours.
3. **Add more collateral.** If ETH drops — top up with more ETH (or [stablecoins](/en/glossary/#stablecoin)) to raise your health factor.
4. **Use alerts.** There are services that notify you when your health factor gets low (e.g., DeBank or Aave's built-in notifications).

---

## Protocol Examples

### Aave

**[Aave](https://aave.com)** — the largest DeFi lending protocol.

Highlights:

- you can borrow against more than 20 assets (ETH, USDC, DAI, WBTC, MATIC, and others);
- interest rates can be **stable** (stable rate) or **variable** (variable rate);
- **flash loans** are available — instant loans with no collateral (but they must be repaid in the same transaction);
- your position's health is shown as a health factor: >1 means it's fine, =1 means liquidation.

### Compound

**[Compound](https://compound.finance)** — one of the first DeFi protocols, launched in 2018.

Highlights:

- works similarly to Aave, but without stable rates;
- uses algorithmically adjusted interest rates;
- integrates with many [wallets](/en/glossary/#wallet) and services.

### MakerDAO

**[MakerDAO](https://makerdao.com)** — a slightly different model.

Here you don't just take out a loan — you **create the DAI stablecoin** by locking up ETH (or other assets) as collateral. It's essentially the same as a loan: you lock ETH, get DAI, and when you return the DAI plus interest — your collateral is unlocked.

> MakerDAO is the backbone of the entire DeFi ecosystem. Hundreds of protocols use DAI.

---

## DeFi Loan vs. Bank Loan: Comparison

| Criteria              | Bank Loan                            | DeFi Loan                             |
|-----------------------|--------------------------------------|---------------------------------------|
| Credit history        | Required                             | Not needed                            |
| Approval time         | Days to weeks                        | Seconds                               |
| Collateral            | Usually not needed (personal loans)  | Required (150%+ of the loan amount)   |
| Interest              | 5–30% APR (depends on credit)        | 1–15% APR (depends on supply & demand)|
| Access                | Passport, [KYC](/en/glossary/#kyc), 18+                   | Internet connection, any age          |
| Liquidation           | Court, bailiffs, defaults            | Automatic, handled by bots            |
| Geography             | Only the bank's country              | Global                                |
| Operating hours       | Business hours                       | 24/7, no days off                     |

> The main difference: a bank trusts you based on your past. DeFi trusts you based on your current collateral.

---

## Risks of DeFi Loans

DeFi loans aren't just about freedom — they come with serious risks too.

### 1. Volatility and Liquidation

[Cryptocurrency](/en/glossary/#cryptocurrency) is one of the most volatile assets in the world. ETH can drop 20–30% in a single day. If your health factor was already low — liquidation is inevitable.

> Recommendation: keep your health factor no lower than 1.5–2.0 on calm days and 2.5–3.0 on volatile ones.

### 2. Smart Contract Bugs

DeFi protocols are software. Software has bugs. If a hacker finds a vulnerability in Aave's or Compound's smart contract — all user deposits could be stolen.

> Example: the Cream Finance hack (2021) — $130 million. Even large, audited protocols aren't immune.

### 3. Oracle Problems

Oracles are services that feed price data to smart contracts (Chainlink, for example). If an oracle reports a wrong price — liquidation can happen by mistake.

> In 2022, there was an incident with the Mango Markets protocol where oracle manipulation let attackers drain $114 million from the protocol.

### 4. Inability to Repay the Loan

If you lose access to your wallet or simply don't have the funds to repay — your collateral gets liquidated. Nobody can help you, and there's no bank to restore your access.

### 5. "Junk" Collateral Assets

Some protocols let you deposit obscure [tokens](/en/glossary/#token) with low [liquidity](/en/glossary/#liquidity) as collateral. A sharp drop in such an asset can liquidate your entire position in minutes.

> Only use reliable assets with high liquidity (ETH, WBTC, USDC, DAI).

---

## When a DeFi Loan Actually Makes Sense

A DeFi loan isn't for buying a car or a house. It's a tool for:

- **getting [liquidity](/en/glossary/#liquidity)** without selling your assets (you don't want to sell ETH but need USDC);
- **arbitrage and trading** (borrow at a low rate, invest in a high-yield pool);
- **leverage** (increase your position without selling your holdings);
- **flash loans** (complex strategies executed in a single transaction).

> If you need a mortgage or a personal loan — DeFi won't help. But if you have ETH and want to get USDC against it without paying capital gains tax — it's a perfect fit.

---

## Summary

DeFi loans are a revolution in finance:

| Pros                                 | Cons                                    |
|--------------------------------------|-----------------------------------------|
| Instant approval                     | Risk of liquidation in a market crash   |
| No credit history required           | Risk of smart contract bugs             |
| Accessible from anywhere in the world| Requires active position monitoring     |
| Transparency (everything on-chain)   | Cryptocurrency volatility               |
| Interest rates often lower than banks| Loss of collateral during liquidation   |

> A DeFi loan isn't free money. It's a tool that gives you freedom — but demands responsibility.

If you decide to give it a try:

1. Start small — $50–100;
2. Use a battle-tested protocol (Aave, Compound);
3. Keep your health factor above 2.0;
4. Stay alert — watch the market.

---

## FAQ

### Can I get a DeFi loan without collateral?

Generally, no. DeFi loans require overcollateralization. The exception is **flash loans** (instant loans), but they must be repaid in the same transaction. For the average user, flash loans aren't very practical.

### What are the interest rates on DeFi loans?

It depends on supply and demand. On Aave, USDC rates can be 2–10% APR. During periods of high demand — up to 20–30%.

### What happens if I don't repay the loan?

Nobody will call or threaten you. The smart contract will simply liquidate your collateral, cover the debt, and send any remaining funds back to your wallet. But you'll lose the liquidation penalty (usually 5–15%).

### How do I know if my position is close to liquidation?

Both Aave and Compound have a **health factor** indicator. As long as it's above 1 — your position is safe. Once it drops toward 1 — it's time to add more collateral or repay part of the debt.

### Which coins can I use as collateral?

ETH, WBTC, USDC, DAI, MATIC, LINK, and many others. The more liquid the asset, the higher the LTV (the more you can borrow against it).

### Do I have to pay taxes on a DeFi loan?

In most countries — no, because a loan isn't considered income. However, if your collateral gets liquidated, that may be treated as a taxable event (a sale of the asset). Check with a local tax advisor.
