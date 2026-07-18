---
weight: 4
title: "What to Do When Your Crypto Wallet Gets Hacked"
description: "Emergency steps when your crypto wallet is hacked: how to save your assets, what actions to take in the first few minutes"
category: "security"
translationKey: "hacked-what-to-do"
slug: "hacked-wallet-what-to-do"
keywords:
  - wallet hacked
  - crypto theft
  - emergency response
  - stolen crypto
  - revoke access
  - move funds
prev: "/en/security/token-allowances-explained"
next: "/en/security/common-mistakes"
---

## What to Do When Your Crypto Wallet Gets Hacked

---

You open your wallet app — and you don't recognize your balance.

The tokens that were in your account are gone. Or you see a few strange outgoing transactions you never made.

It could be worse: you're watching someone drain your funds right now.

> **In crypto, nobody is getting your stolen money back.**

Not a bank. Not the police. Not the blockchain developers.

But that doesn't mean there's nothing you can do. This article lays out a clear action plan for the first minutes after discovering a hack.

---

## The First Seconds: Don't Panic

Your biggest enemy in this situation is panic. It's what makes you mess up:

- moving your remaining funds to a "safe" wallet that actually belongs to the scammer;
- clicking links in shady "recover your funds" messages;
- paying "gas fees" to get your stolen money back;
- giving your seed phrase to "support staff."

All of these are traps that will only make things worse.

> **Rule #1: Stop. Look around. Follow the plan.**

---

## Step 1. Isolate the Wallet

The moment you notice suspicious activity, your goal is to **cut off** the attacker's access to your funds.

If a hot wallet was compromised (MetaMask, Trust Wallet, Phantom, etc.):

1. **Turn off the internet** on the device (airplane mode) if you see a transaction that hasn't confirmed yet. This won't help if the seed phrase is already out there, but it might buy you seconds.
2. **Immediately create a new wallet** — on a different device or in a different app.
3. **Generate a fresh seed phrase.** Never reuse the old one.

> **Your old wallet can never be considered safe again. Ever.**

---

## Step 2. Rescue What's Left

If there are still funds in the wallet — move fast:

- Open a new, clean wallet (fresh seed phrase, fresh address).
- Transfer **all remaining tokens** to it.
- Start with the most valuable assets.
- Make sure the old wallet doesn't have any claimable tokens (staking, farming rewards).

Important: the scammer may have set up a script that automatically intercepts incoming transfers. So:

> **Don't send anything to the compromised address.**

Even if you got a message saying "send 0.001 ETH to the old address to recover your funds" — it's a scam.

---

## Step 3. Revoke Token Approvals

Often a hack happens not through a stolen seed phrase, but through malicious **token allowances**.

Here's what goes down:

- you once signed a transaction that gave a smart contract access to your tokens;
- the attacker uses that access and drains your funds.

Even after you move your remaining funds to a new wallet, **the allowances on the old address could be used again** if anything ever lands there.

What to do:

1. Go to [Revoke.cash](https://revoke.cash) or a similar service.
2. Connect the **compromised** wallet (read-only, don't sign any transactions).
3. Find tokens with suspicious allowances.
4. Revoke them.

> **Check allowances on every address where you held assets.**

---

## Step 4. Change All Passwords and Seed Phrases

If an attacker got into one account, they may have compromised others too:

- your exchange password;
- your email (via a password reset simulation);
- your Google Authenticator / 2FA.

So:

1. Change the password on **every exchange** where you have an account.
2. Update 2FA — generate new keys.
3. Check whether your email or phone number was changed.
4. If you reuse the same password across multiple services — **change them all**.

> **Use a password manager. One password, one service.**

---

## Step 5. Regenerate Your Seed Phrase Completely

If you suspect your seed phrase was compromised, **don't try to "fix" it**.

Create a brand new wallet from scratch:

1. Install a fresh wallet app (or use a clean browser/device).
2. Create a new wallet — **generate a brand new seed phrase**.
3. Write it down on paper. Never store it digitally.
4. Transfer funds from your other addresses to the new wallet.

The old seed phrase? Throw it away. It's compromised.

---

## Step 6. Contact Exchange Support

If the attacker managed to move funds to a centralized exchange (Binance, Bybit, Kraken, OKX), there's a chance the exchange can **freeze the scammer's account**.

What to do:

1. Contact the exchange's support team as fast as you can.
2. Provide:
   - your compromised wallet address;
   - the transaction hash where the funds were stolen;
   - the destination address (if you know it);
   - the date and time of the incident.
3. Ask them to freeze the recipient's account.

The odds aren't great, but they're not zero — especially if the amount is large and you act quickly.

> **The faster you act, the better your chances.**

---

## Step 7. Warn the Community

If you fell victim to a specific scam, phishing site, or malicious dApp:

- report it on [Scam Sniffer](https://scamsniffer.io) (a database of known scams);
- post on X (Twitter) tagging the project or wallet involved;
- warn others in Telegram chats or Discord.

It helps keep the next person from falling for the same trick.

---

## What NOT to Do

Some things will **only make the situation worse**:

- ❌ Paying "gas" or a fee to get your funds back — 100% a scam.
- ❌ Using "crypto recovery services" — they're all fraudulent.
- ❌ Downloading software recommended by strangers on social media.
- ❌ Telling your seed phrase to anyone, even "wallet representatives."
- ❌ Trying to "reverse" a blockchain transaction — it's impossible.

> **If someone promises to get your stolen money back for a fee — they're scamming you.**

---

## Prevention for the Future

Once you've dealt with the emergency, it's worth rethinking your security habits:

- ✅ Use a **hardware wallet** (Ledger, Trezor) for storing large amounts.
- ✅ Set **transaction limits** in your wallet.
- ✅ Check token approvals once a month.
- ✅ Don't sign transactions you don't understand.
- ✅ Use separate wallets for different purposes (one for everyday use, another for storage).
- ✅ Store your seed phrase **physically** (paper, metal) where nobody else can get to it.

> **Crypto gives you freedom. But freedom comes with responsibility.**

---

## FAQ

### Can I get my stolen funds back?
In most cases — no. The blockchain is irreversible. The exception is if the funds ended up on a centralized exchange and you reported it in time.

### What if my seed phrase was stolen but my funds are still there?
Create a new wallet immediately and transfer everything to it. The old seed phrase is now compromised.

### Should I pay "gas fees" to recover my funds?
No. That's a scam. Stolen funds aren't returned for a fee.

### Will the police help?
Almost never. Crypto has no "issuer" that can reverse a transaction. Going to the police might make sense only for very large amounts and if you can provide the suspect's details.

### What if my exchange wallet was hacked?
Contact exchange support immediately, change your password, revoke all API keys, and enable 2FA (if you hadn't already). Exchanges can freeze withdrawals while they investigate.
