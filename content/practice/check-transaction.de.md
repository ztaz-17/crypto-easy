---
weight: 6
title: "So Überprüfst Du eine Transaktion in der Blockchain"
description: "Wie man jede Crypto-Transaktion mit Etherscan und ähnlichen Tools überprüft: worauf man achten muss, wie man Status und Bestätigungen liest"
category: "practice"
translationKey: "check-transaction"
slug: "check-transaction-in-blockchain"
keywords:
  - Etherscan
  - Blockchain-Explorer
  - Transaktion prüfen
  - Transaktionsstatus
  - TxID
  - Wallet-Tracking
prev: "/de/practice/first-transaction-without-mistakes"
next: "/de/practice/"
---

## So Überprüfst Du eine Transaktion in der Blockchain: Alles, was Du Wissen Musst

---

Du hast etwas Crypto gesendet. Das Geld hat deine Wallet verlassen. Aber ist es tatsächlich beim Empfänger angekommen?

In der Bankenwelt wartest du einfach auf eine SMS oder Push-Benachrichtigung. In der Crypto-Welt ist alles viel transparenter:

> **Jede Transaktion ist ein öffentlicher Eintrag, den jeder überprüfen kann.**

Und du brauchst weder den Banksupport noch Zugriff auf das Konto einer anderen Person. Alles, was du brauchst, ist ein Tool — ein **Blockchain-Explorer**.

In diesem Artikel behandeln wir:
- wie du jede Transaktion anhand ihrer ID findest;
- was die Status Success, Pending und Failed bedeuten;
- wie du die Details liest: Block, Gebühr, von wo nach wo;
- welche Explorer für verschiedene Netzwerke funktionieren;
- wie du Wallet-Überwachung einrichtest.

---

## Was ist ein Blockchain-Explorer und Wozu Braucht Man Ihn?

Ein **Blockchain-Explorer** ist wie "Google für die Blockchain." Eine öffentliche Website, die alles zeigt, was im Netzwerk passiert:

- jede Transaktion;
- jede Wallet und ihren Saldo;
- jeden Block und seinen Inhalt.

Im Gegensatz zu einer Bank, wo du nur deine eigene Aktivität siehst, ist in der Blockchain **alles sichtbar**. Die Daten sind nur in Adressen codiert — ohne Verbindung zu deiner Identität.

Du brauchst einen Explorer, wenn:

| Situation | Warum prüfen? |
|-----------|---------------|
| Du hast Geld gesendet, der Empfänger sagt "nicht angekommen" | Zeige den TxID — Beweis des Sendens |
| Eine Transaktion hängt fest | Überprüfe den Status und die Anzahl der Bestätigungen |
| Du willst eine Adresse überprüfen | Sieh dir den Verlauf und Saldo der Wallet an |
| Ein Betrüger hat eine falsche Überweisung geschickt | Prüfe, ob die Transaktion wirklich in der Blockchain existiert |

---

## Etherscan: Der Wichtigste Ethereum-Explorer

**Etherscan** ([etherscan.io](https://etherscan.io)) ist der beliebteste Blockchain-Explorer. Er funktioniert für das Ethereum-Netzwerk und alle ERC-20-Standard-Token.

### Transaktions-Hash (TxID)

Lass uns ein zufälliges Beispiel durchgehen. Ich habe eine interessante Transaktion gefunden — wir nutzen sie, um alle Details aufzuschlüsseln:  
`TxID: 0x6f6fd3e8018516ff5e60bfcc2c4fd01be74a877f6b4fac1705651623ad7d70cd`

1. Gehe zu [etherscan.io](https://etherscan.io).
2. **Füge den TxID** in die Suchleiste ein (oben in der Mitte der Seite).
3. Drücke Enter.

Innerhalb einer Sekunde siehst du alle Transaktionsdetails.

Betrachte es als "Belegnummer." Kopiere sie und sende sie an den Empfänger — es ist der offizielle Beweis der Überweisung.

### Was Etherscan Anzeigt

Das siehst du auf der Transaktionsseite:

#### Status

| Status | Was es bedeutet |
|--------|-----------------|
| ✅ **Success** | Transaktion ausgeführt, Guthaben gutgeschrieben |
| ⏳ **Pending** | Wartet — noch nicht in einem Block enthalten |
| ❌ **Failed** | Fehler — Transaktion nicht durchgeführt (Gas-Gebühr verbrannt) |

> **Wichtig:** Failed ≠ Geld verloren. Wenn die Transaktion fehlschlug, kehren die Gelder zum Sender zurück (abzüglich der Gas-Gebühr).

#### Block

Die Blocknummer, in der die Transaktion enthalten ist.  
Zum Beispiel:  
`Block: `**`25093288`**` 22 Block Confirmations`

Je mehr Block-**Bestätigungen**, desto sicherer die Transaktion:

| Netzwerk | Mindestbestätigungen für Sicherheit |
|----------|-------------------------------------|
| Bitcoin | 3–6 |
| Ethereum | 12–32 |
| Solana | 1 (sehr schnelle Finalisierung) |

#### From / To

- **From** — die Adresse des Senders.  
`From: 0x56Eddb7aa87536c09CCc2793473599fD21A8b17F (Binance 17)`
- **To** — die Adresse des Empfängers (oder Vertragsadresse).  
`To: 0x42008C6392F552fcFF9abbf310E4421eEd22fAF9`

> \* *Binance 17* — **Etherscan** hat die Wallet-Adresse als zur Börse Binance gehörig identifiziert. Diese Info steht nicht in der Blockchain selbst, aber die Analyse der Website stellt diese Verbindung her.

Klicke auf eine beliebige Adresse — du siehst ihren gesamten Verlauf und Saldo.

#### Value

Der Überweisungsbetrag: `0 ETH ($0.00)` weil es eine Token-Überweisung (ERC-20) war: `6,000,000.25342 ($5,997,252.25) Tether USD (USDT)`.

#### Transaktionsgebühr (Gas Fee)

Die für die Transaktion gezahlte Gebühr. Zeigt zwei Zahlen:

- **Transaction Fee** — wie viel Gas tatsächlich verbraucht wurde;  
`Transaction Fee: 0.000063066067464358 ETH ($0.14)`
- **Gas Price** — der Preis pro Gas-Einheit (in Gwei);  
`Gas Price: 1.367404598 Gwei (0.000000001367404598 ETH)`

Da hast du's. $6,000,000 gesendet und $0.14 an Gebühren bezahlt.

#### Gas Limit

Das maximale Gas, das du zu zahlen bereit warst, und wie viel tatsächlich verbraucht wurde.  
`Gas Limit & Usage by Txn: 220,436 | 46,121 (20.92%)`

---

## Liste der Explorer

Jedes Blockchain-Netzwerk hat seinen eigenen Explorer. Hier sind die bekanntesten:

### Ethereum (ERC-20)

- **Etherscan** — [etherscan.io](https://etherscan.io) — der wichtigste Ethereum-Explorer.
- **Etherscan für Sepolia-Testnet** — [sepolia.etherscan.io](https://sepolia.etherscan.io) (praktisch zum Üben).

### BNB Chain (BEP-20)

- **BscScan** — [bscscan.com](https://bscscan.com) — das vollständige Etherscan-Äquivalent für Binance Smart Chain.  
Die Oberfläche ist fast identisch — gleiche Status, Blöcke, Gebühren.

### Solana

- **Solscan** — [solscan.io](https://solscan.io) — der wichtigste Explorer für Solana.

Solana-Besonderheit: Transaktionen bestätigen in **Millisekunden**. Der Status Pending existiert hier praktisch nicht.

### TRON (TRC-20)

- **Tronscan** — [tronscan.org](https://tronscan.org) — der offizielle Explorer des Tron-Netzwerks.  
Beliebt für USDT — viele Leute nutzen Tron wegen der niedrigen Gebühren.

### Bitcoin

- **Blockchain.com** — [blockchain.com/explorer](https://www.blockchain.com/explorer) — der bekannteste BTC-Explorer.
- **Mempool.space** — [mempool.space](https://mempool.space) — fortgeschrittener Explorer mit Visualisierung der Transaktions-Warteschlange (Mempool).

### Universalsuche

- Bitcoin und Litecoin — [bitaps.com](https://bitaps.com/) — ein alternativer Explorer.

---

## So Überwachst Du eine Wallet: Benachrichtigungen

Du musst nicht jede Transaktion manuell prüfen. Explorer können dich über Wallet-Aktivitäten benachrichtigen.

### Einrichtung auf Etherscan

1. Registriere dich auf [etherscan.io](https://etherscan.io) (kostenlos).
2. Gehe zu **"Watch List"** → **"Add Address"**.
3. Füge die zu überwachende Wallet-Adresse ein.
4. Richte Benachrichtigungen ein:
   - **Email** — erhalte eine E-Mail bei jeder eingehenden/ausgehenden Transaktion;
   - **Telegram** — über den Etherscan Alert Bot.

### Ähnliche Funktionen in Anderen Exploern

- **BscScan** — gleiches Watch List-System, E-Mail-Benachrichtigungen.
- **Solscan** — klicke auf **"Subscribe"** auf der Adressseite.
- **Tronscan** — der **"Follow"**-Button auf der Wallet-Seite.

### Drittanbieter-Überwachungsdienste

- **Dextools** ([dextools.io](https://dextools.io)) — verfolge Transaktionen nach Token und Liquiditätspool.
- **Nansen** ([nansen.ai](https://nansen.ai)) — professionelles Wallet-Analyse-Tool (kostenpflichtig).
- **Telegram-Bots** — unzählige Bots verfolgen "Wale" und große Transaktionen in Echtzeit.

> Tipp: Wenn du eine wichtige Überweisung erwartest, richte eine Benachrichtigung im Explorer ein. Du wirst benachrichtigt, **bevor** der Empfänger "ist angekommen" sagt.

---

## So Überprüfst Du eine Transaktion auf einer Börse (CEX)

Wenn du Crypto **von einer Börse** an eine externe Wallet oder umgekehrt bewegst, ist der Prozess etwas anders:

1. Finde den **TxID** im Transaktionsverlauf der Börse (normalerweise unter "Verlauf" → "Ein-/Auszahlungen").
2. Kopiere den TxID.
3. Öffne den Explorer für das richtige Netzwerk und füge den TxID ein.

> **Wichtig:** Börsen zeigen oft ihren eigenen internen TxID für interne Überweisungen an. Wenn du **zwischen Nutzern derselben Börse** gesendet hast — gibt es keine Blockchain-Transaktion, es ist nur ein Datenbankeintrag auf der Börsenseite.

### Wie Man eine Interne Überweisung von einer Blockchain-Transaktion Unterscheidet

| Überweisungstyp | Hat einen TxID? | Kann man im Explorer prüfen? |
|-----------------|-----------------|------------------------------|
| Innerhalb der Börse (Nutzer A → Nutzer B auf Binance) | Ja, aber intern | ❌ Nein |
| Von Börse zu externer Wallet | Ja, ein echter TxID | ✅ Ja |
| Von Wallet zur Börse | Ja | ✅ Ja |

---

## Was Tun, Wenn eine Transaktion Hängt

Der Status **Pending** kann von ein paar Sekunden bis zu mehreren Tagen dauern. So läuft es ab und was du tun kannst.

### Warum Transaktionen Hängen

- **Niedrige Gas-Gebühr.** In Netzwerken wie Ethereum verarbeiten Miner zuerst die Transaktionen mit den höchsten Gebühren. Wenn du das Gas zu niedrig angesetzt hast — bleibt die Transaktion in der Warteschlange.
- **Netzwerk-Überlastung.** In Hype-Momenten (z.B. einem beliebten NFT-Drop) kann die Warteschlange riesig werden.
- **Node-Probleme.** Selten, aber manchmal verlangsamt ein bestimmter Validator die Dinge.

### Was Du Tun Kannst

1. **Warten.** Wenn das Netzwerk nicht kritisch überlastet ist, wird die Transaktion durchgehen — nur langsam.
2. **Beschleunigen (Replace-by-Fee).** Manche Wallets (MetaMask, Trust Wallet) haben eine **"Speed Up"**-Option — du sendest dieselbe Transaktion mit einer höheren Gebühr erneut.
3. **Abbrechen.** Wenn deine Wallet **"Cancel"** unterstützt, kannst du die feststeckende Transaktion durch eine leere mit höherer Gas-Gebühr ersetzen.

> **Wenn die Transaktion nach 24 Stunden immer noch Pending ist** — wird sie höchstwahrscheinlich "herausfallen" (nie in einen Block aufgenommen), und die Gelder kehren zurück.

### Wann Panik (Spoiler: Fast Nie)

| Status | Solltest du dir Sorgen machen? |
|--------|--------------------------------|
| Pending (bis zu 30 Min) | Nein, das ist normal |
| Pending (1–6 Stunden) | Es lohnt sich, Gas und Netzwerk zu prüfen |
| Pending (über 24 Stunden) | Transaktion wird wahrscheinlich nicht durchgehen — Gelder kehren zurück |
| Success | ✅ Betrachte die Überweisung als abgeschlossen |
| Failed | ❌ Gelder zurück (abzüglich Gas-Gebühr) |

---

## Checkliste: Was Nach dem Senden Prüfen

Wenn du Crypto gesendet hast, gehe diese Liste durch:

| # | Schritt | Worauf achten |
|---|---------|---------------|
| 1 | Kopiere den TxID aus deiner Wallet | Stelle sicher, dass es kein leerer String ist |
| 2 | Öffne einen Explorer (Etherscan, etc.) | Füge den TxID in die Suche ein |
| 3 | Überprüfe den Status | ✅ Success = erledigt |
| 4 | Überprüfe den Betrag (Value) | Stimmt er mit dem überein, was du gesendet hast? |
| 5 | Überprüfe die Empfängeradresse (To) | Hast du an die richtige Adresse gesendet? |
| 6 | Sieh dir die Anzahl der Bestätigungen an | Je mehr, desto sicherer |
| 7 | Sende den TxID an den Empfänger | Dies ist der Beweis der Überweisung |

---

## Häufig Gestellte Fragen

### Kann ich eine Transaktion ohne TxID prüfen?

Ja, wenn du die **Adresse des Senders oder Empfängers** kennst. Füge die Adresse in die Suche des Explorers ein — du siehst **alle ihre Transaktionen** und kannst die richtige nach Betrag, Datum oder Hash finden.

### Wie überprüfe ich, ob ein Betrüger eine echte Überweisung gesendet hat?

Betrüger schicken oft Screenshots oder PDFs mit "Beweis" einer Überweisung. Der einzige Weg zu prüfen:

1. Fordere den TxID an.
2. Füge ihn in einen Explorer ein.
3. Wenn es keine Transaktion gibt — ist sie gefälscht.

### Was sind Bestätigungen?

Jeder neue Block, der nach dem Block mit deiner Transaktion hinzugefügt wird, gibt **+1 Bestätigung**. Je mehr Bestätigungen, desto schwerer ist die Transaktion umkehrbar.
- Für kleine Beträge: 1–3 Bestätigungen reichen.
- Für große Beträge: 6+ Bestätigungen.
- Bei Bitcoin warten Börsen normalerweise auf 3–6 Bestätigungen.

### Warum wurde die Gebühr berechnet, obwohl die Transaktion fehlschlug?

Gas ist die Bezahlung für **Rechenarbeit**, nicht für Erfolg. Wenn eine Transaktion fehlschlug (z.B. unzureichender Token-Saldo), hat der Miner dennoch den Code ausgeführt und die Gebühr verdient. Die Gelder **kehren** in deine Wallet zurück, aber das Gas ist verbrannt.

### Kann ich eine bereits gesendete Transaktion stornieren?

Nein. Wenn eine Transaktion bestätigt ist (Success), ist sie **dauerhaft** in der Blockchain aufgezeichnet. Niemand — nicht der Entwickler, nicht ein Miner, nicht eine Regierung — kann sie rückgängig machen.

---

## Zusammenfassung

Eine Transaktion in der Blockchain zu überprüfen, ist eine Superkraft, die dir traditionelle Finanzen nicht geben:

- Du kannst **jede** Operation öffentlich und transparent sehen.
- Du musst keinen Support anrufen oder auf eine Antwort warten.
- Der TxID ist ein rechtlich bedeutsamer Beweis einer Überweisung.
- Du kannst jede Wallet in Echtzeit verfolgen.

Denk an drei Dinge:

1. **TxID = Belegnummer.** Speichere ihn nach jedem Senden.
2. **Explorer sind kostenlos.** Etherscan, BscScan, Solscan, Tronscan — alle jederzeit verfügbar.
3. **Status Success = Geld angekommen.** Wenn der Status Success ist, zählt nichts anderes.

Crypto gibt dir **volle Kontrolle und volle Transparenz**. Eine Transaktion zu überprüfen ist der erste Schritt, um sich in dieser Welt sicher zu fühlen.
