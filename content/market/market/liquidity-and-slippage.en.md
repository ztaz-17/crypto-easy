---
weight: 20
title: "What Is Liquidity and Why It Matters for Price"
description: "What liquidity means in crypto trading, how market depth and order books work, what slippage is, and why low liquidity makes trading dangerous for beginners."
category: "market"
translationKey: "liquidity-and-slippage"
slug: "liquidity-and-slippage"
keywords:
  - liquidity
  - market depth
  - slippage
  - order book
  - low liquidity risk
---

## What Is Liquidity and Why It Matters for Price

---

Sound familiar?

You decide to sell a coin on an exchange. You place a sell order at the current price — $100. You wait a minute. Two minutes. Ten minutes. Nobody buys.

You lower the price to $99. Then $98. Only when you get down to $95 does someone finally take your coin.

Or the other way around: you want to buy an altcoin. You see the price at $10, hit "Buy" — and the order fills at $12. How is that possible?

It all comes down to **[liquidity](/en/glossary/#liquidity)**.

In this article we'll cover:
>- what liquidity means in simple terms;
>- how an order book works;
>- what slippage is;
>- and why low liquidity is dangerous.

---

## Liquidity: the ability to buy or sell quickly without losing on price

### What it is

**Liquidity** is how easily you can exchange an asset for cash (or another asset) without moving the price significantly.

> **Real-world example:**
> Selling an apartment at market price within a month is tough. Finding a buyer, negotiating, handling paperwork. That's a **low-liquidity asset**.
>
> Selling dollars at a currency exchange booth — 5 seconds. That's a **high-liquidity asset**.

Same thing in crypto:

- **Bitcoin on Binance** — high liquidity. You can sell $50,000 in seconds and the price barely moves.
- **An obscure [token](/en/glossary/#token) on a small exchange** — low liquidity. Even a $1,000 sell order can move the price by 10-20%.

### Why it matters

Liquidity determines:
- how fast you can exit a position;
- what price your order will fill at;
- how predictable price movements will be.

---

## Market depth: the order book

### How an order book works

Every exchange is just a place where buyers and sellers meet. All their orders are collected in an **order book**.

It looks like this:

```
SELLERS (Asks)
───────────────
$101.00 — 500 coins
$100.80 — 200 coins
$100.50 — 100 coins
───────────────
CURRENT PRICE: $100.00
───────────────
BUYERS (Bids)
───────────────
$99.80  — 150 coins
$99.50  — 300 coins
$99.00  — 600 coins
```

- **Bids** — buy orders (how much people are willing to buy and at what price).
- **Asks** — sell orders.
- The gap between the best bid and best ask is the **spread**.

### What market depth is

**Market depth** is the volume of orders sitting at different price levels.

If every level has millions of dollars behind it — the market is deep. If only 10 coins are sitting one dollar above the current price — the market is shallow. Any buy order will immediately move the price.

> **Simple metaphor:**
> - A deep market is like a swimming pool. You can jump in — the water level barely changes.
> - A shallow market is like a puddle. One step and water splashes everywhere.

### Spread — a liquidity indicator

**Spread** is the difference between the best bid price and the best ask price.

- Tight spread ($0.01) → high liquidity.
- Wide spread ($1+) → low liquidity.

If you see a spread of 5-10% on an exchange — that's a red flag. Buying that coin is risky.

---

## Slippage: bought at 100, filled at 105

### What slippage is

**[Slippage](/en/glossary/#slippage)** is the difference between the price you expected and the price your order actually filled at.

It happens because there isn't enough liquidity at the level you wanted.

### How it works

You want to buy a coin at $100. You place a **market order** (buy right now at the best available price).

The system checks the order book:
- at $100.00 — 5 coins for sale;
- at $100.50 — another 5 coins;
- at $101.00 — another 5 coins;
- at $102.00 — another 10 coins...

If you want to buy 25 coins, your order will eat through several levels in a row. Your average fill price won't be $100 — it'll be around $101.20.

You wanted to buy at $100 — you bought at ~$101. That's **slippage**.

> **The bigger your order relative to market depth, the more slippage you get.**

### Limit orders save you from slippage

You can use a **limit order** — you set the price you're willing to buy or sell at, and wait for a counterparty to show up on the market.

But there's another risk:
- if liquidity is low, you might wait hours or days;
- the price could move against you while you wait.

---

## Why low liquidity is dangerous

### 1. Sharp price swings

With low liquidity, one large order can move the price 20-30% in a second.

Example: on a small exchange, sell orders up to $50 total only 100 coins. Someone decides to buy $10,000 worth. Their order eats through every sell order all the way to $70, and the price shoots up instantly.

This is **slippage in its purest form**. And it works both ways:

- you bought at $50 — the price jumped to $70;
- you want to sell — the nearest buyer is at $40.

### 2. Getting stuck in a position

The scariest scenario with low liquidity:

The market starts dropping. You want to sell, but there isn't a single large buyer in the order book. Your order sits there for minutes. The price keeps falling. You lower your price. Nobody takes it.

By the time you find a buyer, the price has already dropped 40%.

> **When the market panics, liquidity evaporates first.**

Everyone wants to sell — nobody wants to buy. The spread blows out to ridiculous levels. And anyone holding low-liquidity coins can't get out, even at a big loss.

### 3. Price manipulation

On low-liquidity coins, it's easy to manipulate the price. A large player ([whale](/en/glossary/#whale)) can:

- boost the price 50% with a single order;
- wait for newcomers to pile in on [FOMO](/en/glossary/#fomo);
- sell everything at the high price — and the price crashes back down.

This is the classic **Pump & Dump** scheme, and it only works on coins with low liquidity.

### 4. Unpredictable fees

On some [decentralized](/en/glossary/#decentralization) exchanges, when liquidity is low, transaction fees can be higher than the trade itself. Or the trade simply fails — there isn't enough pool depth.

---

## How to check liquidity before buying

### 1. Look at the spread

If the difference between buy and sell is more than 1-2%, that's a reason to think twice.

### 2. Check trading volume

On CoinMarketCap or CoinGecko, look at the **24-hour trading volume**. If it's below $1 million for an altcoin — liquidity is low.

### 3. Check the order book

Open the order book on the exchange. How many coins are sitting at levels near the current price? If each level has only 10-20 coins — be careful.

### 4. Compare with Bitcoin

For reference: Bitcoin's daily trading volume is $10-30 billion. Spread is fractions of a cent. Any coin with less than $10 million in daily volume is considered low-liquidity.

---

## Liquidity levels at a glance

| Level | Spread | 24h Volume | Impact of a $10k Order | Example |
|---|---|---|---|---|
| Very high | < 0.01% | > $1B | Negligible | BTC, ETH on Binance |
| High | 0.01-0.1% | $100M-1B | Minimal | Top-10 altcoins |
| Medium | 0.1-0.5% | $10-100M | Noticeable | Mid-cap altcoins |
| Low | 0.5-2% | $1-10M | Strong | Small altcoins |
| Very low | > 2% | < $1M | Critical | Shitcoins, new tokens |

---

## Conclusion

Liquidity is what separates a real market from a casino.

When you trade on an exchange with high liquidity:
- you enter and exit at fair prices;
- the spread is minimal;
- wild swings from a single order don't happen;
- you can plan your trades without surprises.

When liquidity is low:
- every order is a lottery;
- slippage eats into your profits;
- at the critical moment, you can't get out.

> **Simple rule: never trade coins with liquidity lower than the amount you're working with.**

And always check the order book before hitting "Buy". One glance at the spread and market depth can save you from losing money.

---

## FAQ

### What is liquidity in simple terms?

It's the ability to quickly buy or sell an asset at a price close to the market rate, without major losses.

### How is liquidity different from volatility?

Liquidity is about market depth and execution speed. Volatility is how much the price swings. They're often connected: low liquidity leads to high volatility.

### What spread is considered normal?

For Bitcoin and top coins — fractions of a percent. For altcoins — up to 0.5% is acceptable. Anything above 1-2% is the danger zone.

### Why is slippage higher on DEXs (decentralized exchanges)?

DEXs don't have a centralized order book. Price is determined by the size of the liquidity pool. The smaller the pool, the more slippage on any trade.

### Can you lose money from low liquidity even if the price is going up?

Yes. If you can't sell your coin at the current price because there are no buyers — you can't lock in profit. The price may be on the chart, but you can't sell at it.
