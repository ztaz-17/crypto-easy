---
weight: 30
title: "Token-Berechtigungen: Was sie sind und warum sie gefährlich sind"
description: "Was Token-Berechtigungen sind, warum unbegrenzte Freigaben ein Sicherheitsrisiko darstellen und wie man den Zugriff auf seine Tokens widerruft"
category: "security"
translationKey: "token-allowances"
slug: "token-berechtigungen-erklaert"
keywords:
  - token berechtigung
  - token freigabe
  - freigabe widerrufen
  - smart contract risiko
  - ethereum freigabe
  - erc20 freigabe
---

## Token-Berechtigungen: Was sie sind und warum sie gefährlich sind

---

**"Zugriff auf deine USDT bestätigen"** — diese Meldung hast du bestimmt schon gesehen, wenn du deine [Wallet](/de/glossary/#wallet) mit einem neuen [DeFi](/de/glossary/#defi)-Dienst, einer [DEX](/de/glossary/#dex) (Uniswap, PancakeSwap) oder einem [NFT](/de/glossary/#nft)-Marktplatz verbunden hast.

Viele klicken einfach auf "Bestätigen", ohne es überhaupt zu lesen. Und das kann dich jeden einzelnen [Token](/de/glossary/#token) in deiner Wallet kosten.

In diesem Artikel erfährst du:

> - was Token-Berechtigungen sind;
> - warum **unbegrenzte Freigaben** eines der größten Sicherheitslöcher überhaupt sind;
> - wie du prüfst, welche dApps Zugriff auf deine Tokens haben;
> - wie du eine Freigabe widerrufst, falls du versehentlich eine gegeben hast.

---

## Was ist eine Token-Berechtigung

### Wie ERC-20-Tokens funktionieren

Um Berechtigungen zu verstehen, musst du erst verstehen, wie [Tokens](/de/glossary/#token) eigentlich funktionieren.

Der **ERC-20**-Standard (und seine Verwandten BEP-20, TRC-20 usw.) ist ein Smart Contract mit zwei zentralen Funktionen:

- `transfer(from, to, amount)` — verschiebt Tokens;
- `approve(spender, amount)` — erlaubt einer anderen Adresse, deine Tokens auszugeben.

Bei einer normalen Überweisung unterschreibst du die Transaktion selbst. Aber wenn du mit einer [DeFi](/de/glossary/#defi)-App interagierst, muss der Vertrag Tokens **selbstständig** von dir abziehen können.

So läuft das im Hintergrund ab:

1. Du rufst `approve(DEX_Contract, 1000 USDT)` auf;
2. Jetzt kann der [DEX](/de/glossary/#dex)-Vertrag `transferFrom(deine_Adresse, Pool, 1000 USDT)` aufrufen;
3. Der Tausch erfolgt, ohne dass du jeden Schritt einzeln signieren musst.

👉 **Das ist eine Token-Berechtigung** — du gibst einem Smart Contract die Erlaubnis, deine Tokens zu bewegen.

---

### Ein Beispiel aus dem echten Leben

Stell dir vor, du gibst deinem Nachbarn den Schlüssel zu deiner Wohnung, damit er deine Katze füttern kann, während du im Urlaub bist.

Eine Token-Berechtigung ist genau dasselbe, nur digital. Du lässt einen Vertrag eine bestimmte Menge Tokens (oder alle) nehmen und damit machen, was er will.

---

## Warum das gefährlich ist

### Unbegrenzte Freigaben

Das größte Problem: Die meisten [dApps](/de/glossary/#dapp) fragen nicht nach einer **begrenzten** Freigabe — sie verlangen eine unbegrenzte:

```
approve(DEX, MAX_UINT_256)
```

`MAX_UINT_256` ist die größte Zahl in Ethereum (2²⁵⁶ − 1). Praktisch unendlich.

Warum machen [dApps](/de/glossary/#dapp) das?

- **Bequemlichkeit** — kein Bestätigen bei jedem einzelnen Trade nötig;
- **günstiger** — eine `approve`-Transaktion statt mehrerer;
- **es ist der De-facto-Standard** in [DeFi](/de/glossary/#defi).

Aber der Preis für diese Bequemlichkeit ist: **Deine Tokens sind zur Geisel gemacht**.

---

### Was schiefgehen kann

Wenn ein Vertrag, dem du eine unbegrenzte Freigabe gegeben hast:

- **gehackt wird** — kann der Angreifer jeden einzelnen Token abziehen;
- **upgedatet wird** — können die Vertragsbesitzer eine Funktion einbauen, die alles wegnimmt;
- **sich als bösartig herausstellt** — sind deine Gelder sofort weg.

Beispiele aus der Praxis:

- **Poly Network Hack** — 610 Millionen $ Schaden — Ausnutzung einer Cross-Chain-[Brücke](/de/glossary/#bridge)
- **BadgerDAO** — 120 Millionen $ Schaden — Phishing-Angriff mit Freigabe auf einen schädlichen Vertrag
- **Curve Finance Hack** — 570.000 $ Schaden — DNS-basierte Manipulation von Berechtigungen

> **Wichtig:** Ein Angreifer braucht weder deine Seed-Phrase noch deinen Private Key. Es reicht, dass du irgendwann ein `approve` auf einem schädlichen Vertrag unterschrieben hast — und schon gehören deine Tokens ihm.

---

### Du erinnerst dich nicht, wem du Zugriff gegeben hast

Wenn du aktiv in DeFi unterwegs bist, sammelst du im Laufe der Monate und Jahre dutzende Berechtigungen an: Uniswap, OpenSea, 1inch, irgendwelche Test-[dApps](/de/glossary/#dapp), die du längst vergessen hast.

Hier die Frage: Weißt du tatsächlich noch, welche Verträge du freigegeben hast?

Wenn du "nein" gesagt hast — bist du nicht allein. Das ist völlig normal. Aber **genau diese "vergessenen" Berechtigungen sind es, auf die Hacker es abgesehen haben**.

---

## Wie du prüfst, welche dApps Zugriff auf deine Tokens haben

### Etherscan

Der einfachste Weg:

1. öffne [Etherscan.io](https://etherscan.io);
2. füge deine [Wallet](/de/glossary/#wallet)-Adresse ein;
3. gehe zum Tab **"Token Approvals"** (oder einfach "Approvals");
4. siehst du eine Liste der Verträge und wie viel sie ausgeben dürfen.

Für BSC nutzt du [BscScan.com](https://bscscan.com) — die Oberfläche ist dieselbe.

---

### Revoke.cash

Eine bequemere Option ist [Revoke.cash](https://revoke.cash):

1. verbinde deine [Wallet](/de/glossary/#wallet) (MetaMask, WalletConnect);
2. die Seite zeigt **alle deine aktiven Freigaben** über alle Netzwerke hinweg an;
3. zu jeder Freigabe siehst du: den Vertrag, den Token und das Limit.

Der Dienst speichert keine deiner Daten und verlangt keine Gebühr — du signierst die Widerruf-Transaktionen einfach über deine eigene Wallet.

---

### Weitere Tools

- **Zapper.xyz** — Dashboard mit einem "Approvals"-Bereich;
- **DeBank.com** — zeigt Freigaben in deinem Wallet-Profil an;
- **Rabby Wallet** — eingebauter Freigabe-Erkenner;
- **Token Approval Checker** — ein einfacher Prüfer für einzelne Tokens.

---

## Wie man eine Freigabe widerruft

### Über Revoke.cash

1. öffne [Revoke.cash](https://revoke.cash);
2. wähle das Netzwerk (Ethereum, Arbitrum, Optimism, BSC usw.);
3. klicke auf **"Revoke"** neben der Freigabe, die du entfernen willst;
4. bestätige die Transaktion in deiner Wallet.

Fertig. Der Vertrag kann deine Tokens nicht mehr ausgeben.

---

### Über Etherscan

1. finde den Token, dessen Freigabe du widerrufen willst;
2. öffne den Token-Vertrag auf Etherscan;
3. gehe zu **"Contract" → "Write Contract"**;
4. verbinde deine Wallet;
5. suche die `approve`-Funktion und setze:
   - `spender` — die Adresse des Vertrags, den du freigegeben hast;
   - `amount` — **0** (setzt die Berechtigung zurück);
6. signiere die Transaktion.

👉 **Tipp:** Nutz Revoke.cash — das ist einfacher und sicherer (weniger Risiko, eine Adresse zu vertippen).

---

### Wichtige Dinge beim Widerrufen

- Jedes `approve` auf 0 ist eine **Gas-Transaktion** — du musst die Gebühr bezahlen;
- Wenn du die Freigabe für eine [DEX](/de/glossary/#dex) widerrufst, die du aktiv nutzt, musst du sie beim nächsten Tausch erneut freigeben;
- Nach dem Widerruf bleiben deine Tokens in deiner Wallet — es geht nichts verloren.

---

## Best Practices: So bleibst du sicher

### Gib nur frei, was du brauchst

Statt einer unbegrenzten Freigabe gib den **genauen Betrag** an, den du tauschen oder nutzen willst.

Die meisten Wallets und dApps erlauben dir, den Betrag im Bestätigungsfenster zu ändern:

- **MetaMask:** Tippe vor dem Signieren des `approve` auf den Betrag und gib eine **konkrete Zahl** ein;
- **Rabby Wallet:** Schlägt automatisch eine begrenzte Freigabe vor.

👉 **Prüfe immer, wie viel du einen Vertrag ausgeben lässt.**

---

### Nutz ein separates Wallet für DeFi

Erstell dir ein "Hot"-Wallet, das nur Folgendes enthält:

- nur den Betrag, den du bereit bist zu riskieren;
- nicht mehr als 5–20 % deines gesamten Portfolios.

Bewahre deine Hauptgelder in einer **[Cold Wallet](/de/glossary/#cold-wallet)** (Ledger, Trezor) oder auf einer separaten Adresse auf, zu der dApps keinen Zugriff haben.

---

### Prüf deine Freigaben regelmäßig

Mach es dir zur Gewohnheit, das einmal im Monat zu machen:

1. geh zu [Revoke.cash](https://revoke.cash);
2. prüf, welche Verträge Zugriff haben;
3. widerruf alles, was du nicht aktiv nutzt.

Wenn du eine dApp seit 3+ Monaten nicht mehr angefasst hast — widerruf die Freigabe.

---

### Sei vorsichtig bei neuen dApps

Bevor du eine Freigabe erteilst:

- prüf den Vertrag auf [DexScreener](https://dexscreener.com) oder [Dune Analytics](https://dune.com);
- schau, wie lange das Projekt schon existiert;
- such nach einem Smart-Contract-Audit;
- lies auf [Twitter](https://x.com) nach, was andere Nutzer sagen.

Wenn eine dApp verlangt, dass du **sofort alle deine Tokens** freigibst, und dich ohne das nicht handeln lässt — das ist eine **Warnflagge**.

---

### Fazit

Token-Berechtigungen sind ein zentraler DeFi-Mechanismus — ohne sie würden Swaps, Liquiditätspools und [NFT](/de/glossary/#nft)-Marktplätze nicht funktionieren.

Aber sie sind auch **der beliebteste Angriffsvektor**:

> - unbegrenzte Freigaben sind die Norm, nicht die Ausnahme;
> - vergessene Berechtigungen sind eine tickende Zeitbombe;
> - ein falscher Klick auf "Bestätigen" — und all deine Tokens gehen direkt an einen Angreifer.

Die Sicherheitsregeln sind einfach:

> - gib nur den Betrag frei, den du brauchst;
> - nutz ein separates Wallet für DeFi;
> - prüf deine Freigaben einmal im Monat auf [Revoke.cash](https://revoke.cash);
> - unterschreib kein `approve`, ohne hinzuschauen.

**Krypto gibt dir die Kontrolle über dein Geld. Aber diese Kontrolle muss ausgeübt werden — nicht links und rechts verschenkt werden.**

---

## FAQ

### Was ist eine Token-Berechtigung in einfachen Worten?
Es ist die Erlaubnis, die du einem Smart Contract gibst, deine Tokens auszugeben. Stell es dir vor wie die Schlüssel zu deinem Safe zu übergeben — der Vertrag kann so viel nehmen, wie du erlaubt hast.

### Warum ist eine unbegrenzte Freigabe gefährlich?
Wenn der Vertrag gehackt wird oder sich als bösartig herausstellt, kann der Angreifer mit einem einzigen Klick **alle** deine Tokens abziehen.

### Wie widerrufe ich eine Freigabe?
Der einfachste Weg ist über [Revoke.cash](https://revoke.cash) — verbinde deine Wallet und klick bei allen Freigaben, die du nicht brauchst, auf "Revoke".

### Muss ich nach jedem Trade die Freigabe widerrufen?
Nicht unbedingt — aber wenn du diese dApp nicht mehr nutzen willst, ist es eine gute Idee, die Freigabe zu widerrufen.

### Verliere ich meine Tokens, wenn ich eine Freigabe widerrufe?
Nein. Die Tokens bleiben genau da, wo sie sind — in deiner Wallet. Du nimmst dem Vertrag nur die Erlaubnis, sie zu bewegen.
