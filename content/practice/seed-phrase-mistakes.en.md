---
weight: 20
title: "Seed Phrase: the Moment People Lose Money"
description: "How to safely store your seed phrase, where NOT to keep it (no screenshots, cloud, or email), and mistakes that cause permanent loss of funds and crypto."
category: "practice"
translationKey: "seed-phrase-mistakes"
slug: "seed-phrase-mistakes"
keywords:
  - seed phrase
  - recovery phrase
  - private key backup
  - crypto security
  - wallet recovery
  - 12 words
  - cold storage
---

## Seed Phrase: the Moment People Lose Money

---

You just created a [wallet](/en/glossary/#wallet). MetaMask shows 12 words.

"Write down your [seed phrase](/en/glossary/#seed-phrase)," the prompt says.

Right here, most people make a **fatal mistake**.

Not because they're stupid. But because **it's hard to overstate how important this is**, and our brains are wired to think "passwords can be reset."

In crypto, there's no reset.

> **Whoever holds the seed phrase holds the money.**

Lose the phrase — lose everything. Give it to someone — give everything away. Take a screenshot — kiss your balance goodbye.

In this article:

> - how to properly store your seed phrase;
> - where NEVER to store it;
> - the most common mistakes that have cost people millions;
> - and how to verify you did everything right.

---

## What Is a Seed Phrase and Why It *Is* Your Money

A [seed phrase](/en/glossary/#seed-phrase) (recovery phrase) is **12 or 24 words** from which all your [wallet](/en/glossary/#wallet) keys are derived.

It's not a "wallet password." It **is the wallet itself**.

Lose your MetaMask password — just reset it, you have the seed phrase.

Lose your seed phrase — **your password won't help**. The wallet cannot be recovered. By anyone. Ever.

> **The technology is designed so recovery without the phrase is impossible.**

Not MetaMask, not Trust Wallet, not customer support — nobody can give you back access.

---

## How to Properly Store Your Seed Phrase

### ✅ Paper — the Minimum Everyone Should Have

The simplest and most reliable method:

- grab a **pen** (not a pencil — it fades);
- a **sheet of paper** (not a sticky note — it'll get lost);
- write down **every word in exact order**;
- double-check **each word**.

Keep the paper somewhere safe:

- inside a book on a shelf;
- in an envelope in a desk drawer;
- in a safe, if you have one.

> Important: write by hand. Don't copy-paste, don't print, don't type.

### ✅ Metal Plate (Cryptosteel / Steel Wallet) — for the Serious

Paper is vulnerable to fire, water, and time.

A metal plate solves all of these:

- **Cryptosteel** — letter tiles that assemble into words on a metal strip;
- **Billfodler** — a steel plate where words are stamped in;
- **Keystone Tablet** — a similar solution.

It's a small metal card that can be hidden in a safe, buried, or stored in a bank deposit box.

> Metal fears neither fire, nor flood, nor time.

### ✅ Fireproof Safe — for Extra Insurance

If you have a safe, keep your seed phrase there.

The ideal scenario:

- a metal plate in your home safe;
- a paper copy in a bank safety deposit box;
- a third copy (metal) with a trusted person in another city.

> More copies means more risk. Two to three is the sweet spot.

---

## Where NOT to Store Your Seed Phrase

### ❌ Screenshot on Your Phone

The most common beginner mistake.

"I'll just snap a photo just in case" — and that's the last of your money.

Why:

- your phone can break or be stolen;
- apps have access to your gallery;
- cloud backups (Google Photos, iCloud) auto-save the screenshot.

Once that screenshot hits the cloud — **it's no longer yours**.

### ❌ Cloud Services

Google Drive, iCloud, Dropbox — **any cloud** — is a risk.

Doesn't matter if the file is encrypted. If someone gets into your account, they get your phrase.

Example: a user saved his phrase in Google Keep. A month later, his account was hacked. Loss: $50,000.

### ❌ Photos in Your Gallery

Same as a screenshot. Camera, gallery, Google Photos — it all syncs.

Took a photo of your seed phrase? Consider it **published on the internet**.

### ❌ Email

Emailing yourself your seed phrase — "so you don't lose it" — is one of the worst ideas.

Email is a prime target for hackers. **If your email is compromised, the attacker finds that message.**

### ❌ Telegram / Messengers / "Saved Messages"

Telegram is not a place for your seed phrase.

Even "Saved Messages" is cloud storage. Your phrase sits on Telegram's servers. Nobody can guarantee your account won't be hacked, Telegram won't have a breach, or you won't accidentally send it to the wrong chat.

### ❌ "Verify Your Wallet" Websites

A classic scam: you get a message saying your wallet needs verification. You enter your seed phrase — and kiss your money goodbye.

> **No one, ever, should ask for your seed phrase.**

Not MetaMask, not Trust Wallet, not "tech support." If a website asks — it's **100% scammers**.

### ❌ SIM Card / NFC Tag

Some people save their phrase in phone contacts or on their SIM. Terrible idea — SIM cards can be removed, contacts sync to the cloud, and anyone with your phone gets the phrase.

---

## A Real Story

One user bought $12,000 in Bitcoin back in 2017.

He created a wallet and saved his seed phrase in Notes on his phone. It synced to iCloud.

Three years later, he checked his balance. Opens the wallet — **empty**.

His iCloud had been hacked in 2018. The attacker saw every note, including the seed phrase. But he didn't take the money right away — he waited for the price to rise.

In 2021, when Bitcoin hit $60,000, he moved it all to his wallet.

> **Result: $12,000 turned into $0 because of a note on a phone.**

If he'd written the words on paper — he'd have roughly $700,000 today.

---

## Most Common Mistakes

### 1. Wrong Word Order

A seed phrase isn't a bag of words — it's a **sequence**. Swap even two words and the wallet won't recover.

The mistake: you wrote the words but didn't mark which is first. A year later, restoration fails.

### 2. A Misspelled Word

The BIP39 word list has 2,048 distinct words. One wrong word — recovery is impossible. The wallet simply says "invalid phrase."

### 3. Losing the Phrase

You put the paper in a book and forgot which one. You moved — the paper fell out. Spring cleaning — it got thrown out.

> **Without a seed phrase, your money is gone forever.** Not the police, not hackers, not developers can get it back.

### 4. Giving the Phrase to Someone

Trusted a friend — they lost it. Trusted a relative — they moved the funds. Trusted a "manager" — they were a scammer.

Never give your seed phrase to anyone. **Under no circumstances.** Even if you trust them — what if their device gets hacked?

### 5. Storing It in a Text File on Your Computer

"It's just a document" — one that any virus or trojan can read. Info-stealers (RedLine, Vidar) specifically scan drives for BIP39 words.

> **If your computer has that malware, your seed phrase is in the attacker's hands within a minute.**

### 6. Using Online Wallet Generators

"I'll just generate a wallet on a website" — terrible idea. Fake sites keep a copy of the keys. You think it's yours — the site has a second copy. When there's a balance — it gets drained.

> **Only use official wallets: MetaMask, Trust Wallet, Ledger, Trezor.**

---

## How to Verify Your Phrase Was Written Correctly

### Check #1. Restore the Wallet on a Different Device

1. Install the same wallet on another device.
2. Select "Restore wallet with seed phrase."
3. Enter the words in exact order.
4. Confirm the wallet address matches.

> If it matches — the phrase is correct.

### Check #2. Verify the Address Before Depositing

1. Note your public address (starts with `0x...` or `bc1...`).
2. Reset the wallet or open it on another device using the seed phrase.
3. Compare addresses.

If they match — **everything works**.

### Check #3. Test Transaction

1. Send a small amount (e.g., $5) to the wallet.
2. Reset the wallet.
3. Restore with your seed phrase.
4. Confirm the test amount is still there.

> Better to lose $5 on a test than $5,000 from a phrase error.

---

## Summary Table: What's Okay and What's Not

| ✅ Okay | ❌ Not Okay |
|---|---|
| Write by hand on paper | Take a screenshot |
| Stamp onto a metal plate | Store in the cloud (Google Drive, iCloud) |
| Keep in a safe | Send via email |
| Hide inside a book | Save in phone notes |
| Make a copy in a bank deposit box | Store in a text file on your computer |
| | Send over Telegram / messengers |
| | Give to anyone (even family) |
| | Enter on third-party websites |

---

## What to Do If Your Seed Phrase Is Compromised

If you suspect your seed phrase fell into someone else's hands:

1. **Don't panic** — you have time if the money is still there.
2. **Create a new wallet** — generate a fresh seed phrase.
3. **Immediately transfer all funds** to the new wallet.
4. **Never use the old wallet again** — it's compromised.

> Transfer funds as quickly as possible. The attacker could take the money at any moment.

---

## FAQ

### Can I just memorize my seed phrase?

Theoretically — yes. Practically — no. People forget, make mistakes, mix up the order. A stressful situation can throw you off. Write it down. Always.

### How many copies should I make?

2 to 3 is optimal. One at home, a second with a trusted person or in a bank deposit box. A third, metal one, as a backup.

### Can I split the seed phrase into parts?

Yes — there's **Shamir Backup** (secret sharing). The phrase is split into pieces, and recovery needs, say, 2 of 3. For beginners, this is overkill — just write the full phrase in two places.

### Which is safer: 12 words or 24 words?

24 words — more entropy, harder to brute-force. But harder to store and verify. For most users, 12 words is sufficient.

### How do I know if someone stole my seed phrase?

You don't. You'll only find out when the money is gone. The only defense: never store your phrase digitally and never enter it on suspicious websites.

---

## Conclusion

The seed phrase is the most vulnerable moment in crypto.

This is where people lose money. Not from hackers, exchange hacks, or price swings. But from **a single mistake**: a screenshot, a note on your phone, an email, "I'll just remember it."

The rules are simple:

- ✏️ **Paper or metal only.**
- 🔐 **Keep it somewhere safe.**
- 🙅 **Never give it to anyone.**
- 🔄 **Verify before depositing.**

Follow these rules — and your money stays yours.

> Crypto gives you full control over your money. But that control is worthless if you can't control your own key.
