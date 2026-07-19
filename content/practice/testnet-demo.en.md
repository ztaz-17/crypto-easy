---
weight: 30
title: "Demo Mode in Crypto: Testnet"
description: "How to try crypto without any risk: testnets explained, where to get free test tokens, and popular testnet dApps to practice before going live on mainnet."
category: "practice"
translationKey: "testnet-demo"
slug: "testnet-demo-practice-without-risk"
keywords:
  - testnet
  - faucet
  - Goerli
  - Sepolia
  - test ETH
  - crypto demo mode
  - safe learning
---

## Demo Mode in Crypto: Testnet — Try It Without Risk

---

You've heard about crypto. You want to try it out — but you're afraid of losing money.

That's totally normal.

Send to the wrong address. Click the wrong button. Mistype an address. And just like that — your money is gone forever. Crypto doesn't have an "undo" button or a support team that can reverse a transaction.

But here's the good news:

> **You can practice for free, with zero risk and zero investment.**

Cryptocurrencies have a built-in "demo mode" — **testnets**. These are exact copies of real [blockchains](/en/glossary/#blockchain), except the coins have no real value. You can get them for free, send them around, deploy contracts, and make mistakes — all without any financial consequences.

In this article we'll cover:

>- what a testnet is and why you'd use one;
>- where to get free test coins (faucets);
>- how to avoid mixing up a testnet with the real network;
>- a few things a beginner can try.

---

## What Is a Testnet?

A **testnet** is a full copy of the main network (mainnet), with one crucial difference:

> **Coins on a testnet are worthless.**

Developers run testnets so programmers can test apps, smart contracts, and upgrades before going live on the real network. But anyone can use them — including beginners.

Here's what it looks like in practice:

- Ethereum has several testnets: **Sepolia**, **Goerli** (being phased out soon), **Holesky**.
- Polygon has **Amoy** (previously Mumbai).
- BNB Smart Chain has **BSC Testnet**.
- Bitcoin has **Testnet** (yes, Bitcoin has a testnet too).

Every one of these networks follows the same rules as the main one. You create a wallet, get an address, send coins, and pay fees (also test fees). There's only one difference:

> **If you mess up — you lose nothing.**

---

## Where to Get Test Coins: Faucets

To start working on a testnet, you need test coins. Special websites called **faucets** hand them out for free.

Here's how it works:

1. Go to a faucet website.
2. Enter your testnet wallet address.
3. Click "Request" (or "Send me test ETH").
4. A few seconds later, coins arrive in your wallet.

### Faucets for Ethereum Testnet (Sepolia)

The most popular ones:

- **[Google Cloud Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)** — no need to sign up on third-party platforms; you can get ETH, tokens (PYUSD, WBTC, etc.) and [NFTs](/en/glossary/#nft). Just need a Google account.
- **sepoliafaucet.com** — one of the most reliable.
- **infura.io/faucet/sepolia** — requires an Infura account, but gives regular drips.
- **alchemy.com/faucets/ethereum-sepolia** — from Alchemy, also after registration.
- **faucet.quicknode.com/ethereum/sepolia** — from QuickNode.

> 💡 Some faucets require an account on the platform (Alchemy, Infura) or GitHub login — that's normal, it's how they keep bots away.

On Google Cloud Faucet you can request ETH + tokens (e.g. PYUSD and WBTC) at the same time. If you grabbed tokens, you'll need to add them to MetaMask (see the token import section below).

### Faucets for Other Networks

| Network | Faucet | Currency |
|---------|--------|----------|
| Polygon Amoy | faucet.polygon.technology | test MATIC |
| BSC Testnet | testnet.bnbchain.org/faucet-smart | test BNB |
| Bitcoin Testnet | bitcoinfaucet.energy or coinfaucet.eu | test BTC |

> **Important:** all test coins exist only inside their own testnet. You cannot send them to a real wallet or exchange them for real money.

---

## How to Set Up MetaMask for a Testnet

You already have MetaMask installed (see the [previous article](/en/practice/create-wallet-in-5-minutes/) for setup). Switching to a testnet takes just a couple of clicks.

1. Open MetaMask.
2. Click the menu on the right **&rarr;** Networks.
3. In the list, toggle **Show test networks** on.
> ![Enabling test networks in MetaMask](/images/metamask-show-testnet.jpg)

4. From the network selector on the **Custom** tab, choose **Sepolia**.
5. Done — you're on a testnet.

### Get Free Coins

Now let's get some coins into your crypto wallet:

1. Copy your `ETH` address from the top of the wallet: `0x56f218c5aaE76128131A901F4E5cd3B9565bf014` (use your own, of course!)
2. Go to **[Google Cloud Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)**. Enter your address and select **Ethereum Sepolia**.
> ![Google Cloud Faucet — entering your address](/images/google-cloud-faucet-input.jpg)
3. Wait for your balance to update.
> ![MetaMask balance after claiming](/images/metamask-balance-updated.jpg)

### Gimme More! Let's Get USD

Ethereum is a blockchain that became popular because of smart contracts.

Put simply, a smart contract is a program that can issue any kind of token, NFT, define their economics, rules, and so on. And it all runs on gas (Gwei — the fuel of the Ethereum system).

> Important! Only trust official contracts. Any script kiddie hacker can create a coin and send you millions of `USD`, baiting you to visit their site where — after jumping through hoops — you might give them access to your wallet and lose real coins.

So make sure to read the **[Security](/en/security/)** and **[Bonus](/en/bonus/)** sections — there's a lot of useful stuff there. It'll save you from rookie mistakes.

Alright... we want USD!

#### Import Tokens in MetaMask
1. Go back to **[Google Cloud Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)**
2. Select **PayPal USD (PYUSD)** and claim coins to your crypto wallet
3. MetaMask protects you from **dust tokens** and won't show such tokens by default. You have two options:
> - allow all tokens to be displayed (not safe)
> - add the smart contract address to your wallet — then only those tokens will appear and you can transfer them
4. Let's add our contract to the wallet. You can find its address on the blockchain:
> - open the block explorer [sepolia.etherscan.io](https://sepolia.etherscan.io/tx/0x51ffec256bf03a539fb8b435d3b4ee0057cfd6781c452fb2321074caae25dbd9)
> - paste your wallet address `0x56f218c5aaE76128131A901F4E5cd3B9565bf014` (use your own!)
> - go to the **Token Transfers (ERC-20)** tab
> - find your transaction and copy the smart contract address for **ERC-20: PayPal USD (PYUSD)**
> `0xCaC524BcA292aaade2DF8A05cC58F0a65B1B3bB9`
> - in MetaMask, go to **...** **&rarr;** **Import tokens** **&rarr;** paste the smart contract address

Done! We now have **100 USD** 🎉


### What You Can Try on a Testnet

You've got test coins. Now what? Here are a few ideas for a beginner.

#### 1. Send a Transfer to a New Account (Tokens)

Try sending ETH and tokens from one account to another:

1. In MetaMask click the **&or;** next to the account name **&rarr;**  **+ Add account** — a second wallet with a new address will appear.
2. Copy the second account's address.
3. Switch back to the first account, select the **Sepolia** network.
4. On the **Tokens** tab, select PYUSD (or any token you received) **&rarr;** click **Send** **&rarr;** paste the second account's address **&rarr;** enter an amount (e.g., 10 PYUSD).

Watch how the gas fee is deducted and how the transaction shows up on the block explorer: **[sepolia.etherscan.io](https://sepolia.etherscan.io/address/0xd36D4Ed7d4Ed7414190cCDF3159E7eF561683128#tokentxns)**.


#### 2. Send a Transfer to a Friend

Ask a friend to send you some test coins.  
Or send some to the author at this address: `0xd36D4Ed7d4Ed7414190cCDF3159E7eF561683128` from your wallet.

Don't forget to check how the transaction looks on the block explorer: **[sepolia.etherscan.io](https://sepolia.etherscan.io/address/0xd36D4Ed7d4Ed7414190cCDF3159E7eF561683128#tokentxns)**.

#### 3. Check a Transaction on the Explorer

After every operation, open **[sepolia.etherscan.io](https://sepolia.etherscan.io/)**, paste the transaction hash, and look at:

- how much gas you paid;
- how many blocks confirmed the transaction;
- the status (success or failure).

This will teach you how to "read" the blockchain.

#### 4. Try a DeFi App (Carefully)

Some protocols (Uniswap, Aave) have test versions. You can try swapping one token for another or lending coins — all with test funds.

> 🔍 Make sure the site actually offers a test version. Most dApps work with the main network by default.

---

## Why It's Safe

The biggest advantage of testnets:

> **Mistakes don't cost money.**

You can:

- send coins to the wrong address (and lose nothing);
- lose the [seed phrase](/en/glossary/#seed-phrase) for your test wallet (just create a new one);
- click a phishing link (test coins are worthless anyway);
- deploy a broken contract (free practice).

On a testnet, you build the skills you'll later carry into the real world — but with real money.

---

## How Not to Mix Up a Testnet and Mainnet

This is the single most important practical tip.

If you're working on Ethereum Mainnet and send coins to a testnet address — **your money is gone forever**. Technically they're two different networks, but the addresses look identical.

How to stay safe:

| ✅ Do This | ❌ Avoid That |
|------------|---------------|
| Always check the network name in MetaMask (next to the logo) | Don't keep real assets in the same wallet as test coins |
| Use a separate wallet just for testing | Don't mindlessly switch networks in one wallet |
| Set a different theme or label for your test profile | Don't store test and real seed phrases side by side |
| Pause before every send — verify the network | Don't use testnet addresses in real transactions |

> **Golden rule:** before any transaction, pause and check the network name. Three seconds — and your money stays safe.

---

## Conclusion

Testnets are the best way to start exploring crypto without any risk.

They give you the essentials:

- **a safe environment** for learning;
- **free coins** for any experiment you can dream up;
- **complete peace of mind** — make as many mistakes as you like.

Spend an hour: install MetaMask, switch to Sepolia, grab some test ETH from a faucet, send a transaction or two. Watch how they appear on the block explorer.

> **That one hour of practice could save you real money down the road.**

A testnet is your personal training ground. Zero risk. Just practice.

---

## FAQ

### Can I exchange test coins for real money?

No. Test coins exist only inside the testnet and have no real-world value.

### How often can I request test coins?

Each faucet has its own limits — usually once every 24 hours. Some give more after registration.

### What if a faucet isn't working?

Try another one — there are dozens. Or ask a friend to send you some test coins (they're free, after all).

### Can I lose real money on a testnet?

No. If you're only working with the testnet — there are zero real coins there. Danger only comes from mixing up networks (see the section above).

### Why do testnets exist?

To test smart contracts and [dApps](/en/glossary/#dapp) before launch. A bug in a mainnet contract can cost millions of dollars. On a testnet — nothing.
