---
weight: 6
title: "Eine Transaktion in der Blockchain überprüfen"
description: "Wie man jede Krypto-Transaktion mit Etherscan und ähnlichen Tools prüft: worauf man achten muss, wie man Status und Bestätigungen liest"
category: "practice"
translationKey: "check-transaction"
slug: "transaktion-ueberpruefen-blockchain"
keywords:
  - Etherscan
  - Blockchain-Explorer
  - Transaktion prüfen
  - Transaktionsstatus
  - TxID
  - Wallet-Überwachung
prev: "/de/practice/first-transaction-without-mistakes"
next: "/de/exchanges"
---

## Eine Transaktion in der Blockchain überprüfen: Alles, was du wissen musst

---

Du hast Krypto verschickt. Das Geld hat dein Wallet verlassen. Aber ist es auch wirklich beim Empfänger angekommen?

In der Bankenwelt wartest du einfach auf eine SMS oder Push-Benachrichtigung. In der Krypto-Welt ist alles viel transparenter:

> **Jede Transaktion ist ein öffentlicher Eintrag, den jeder überprüfen kann.**

Und dafür brauchst du weder den Banksupport noch Zugriff auf ein fremdes Konto. Alles, was du brauchst, ist ein Tool – ein **Blockchain-Explorer**.

In diesem Artikel erfährst du:

- wie du jede Transaktion anhand ihrer ID findest;
- was die Status Success, Pending und Failed bedeuten;
- wie du die Details liest: Block, Gebühr, von wo nach wo;
- welche Explorer für verschiedene Netzwerke funktionieren;
- wie du eine Wallet-Überwachung einrichtest.

---

## Was ist ein Blockchain-Explorer und warum brauchst du ihn?

Ein **Blockchain-Explorer** ist wie „Google für die Blockchain" – eine öffentliche Website, die alles zeigt, was im Netzwerk passiert:

- jede Transaktion;
- jedes Wallet und dessen Guthaben;
- jeden Block und seinen Inhalt.

Im Gegensatz zu einer Bank, wo du nur deine eigenen Aktivitäten siehst, ist in der Blockchain **alles sichtbar**. Die Daten sind nur in Adressen codiert – ohne Verbindung zu deiner Identität.

Du brauchst einen Explorer, wenn:

| Situation | Warum prüfen? |
|-----------|---------------|
| Du hast Geld gesendet, der Empfänger sagt „nicht angekommen" | Zeige die TxID – der Nachweis der Sendung |
| Eine Transaktion hängt fest | Prüfe den Status und die Anzahl der Bestätigungen |
| Du willst eine Adresse überprüfen | Schau dir die Historie und das Guthaben des Wallets an |
| Ein Betrüger hat eine falsche Überweisung geschickt | Prüfe, ob die Transaktion wirklich auf der Blockchain existiert |

---

## Etherscan: Der wichtigste Ethereum-Explorer

**Etherscan** ([etherscan.io](https://etherscan.io)) ist der bekannteste Blockchain-Explorer. Er funktioniert für das Ethereum-Netzwerk und alle ERC-20-Token.

### Transaktions-Hash (TxID)

Schauen wir uns ein Beispiel an. Ich habe eine interessante Transaktion gefunden – daran erklären wir alle Details:

`TxID: 0x6f6fd3e8018516ff5e60bfcc2c4fd01be74a877f6b4fac1705651623ad7d70cd`

1. Gehe zu [etherscan.io](https://etherscan.io).
2. **Füge die TxID** in die Suchleiste ein (oben in der Mitte der Seite).
3. Drücke Enter.

Innerhalb einer Sekunde siehst du die vollständigen Transaktionsdetails.

Stell es dir wie eine „Quittungsnummer" vor. Kopiere sie und schicke sie dem Empfänger – das ist der offizielle Nachweis der Überweisung.

### Was Etherscan anzeigt

So sieht die Transaktionsseite aus:

#### Status

| Status | Bedeutung |
|--------|-----------|
| ✅ **Success** | Transaktion ausgeführt, Guthaben gutgeschrieben |
| ⏳ **Pending** | Wartet – noch nicht in einem Block enthalten |
| ❌ **Failed** | Fehler – Transaktion nicht durchgekommen (Gas-Gebühr verbraucht) |

> **Wichtig:** Failed ≠ Geld verloren. Wenn die Transaktion fehlschlägt, wird das Geld abzüglich der Gas-Gebühr an den Sender zurückgegeben.

#### Block

Die Blocknummer, in der die Transaktion enthalten ist.

Zum Beispiel:
`Block: **25093288** 22 Block Confirmations`

Je mehr Blöcke **bestätigt** sind, desto sicherer ist die Transaktion:

| Netzwerk | Mindestbestätigungen für Sicherheit |
|----------|-------------------------------------|
| Bitcoin | 3–6 |
| Ethereum | 12–32 |
| Solana | 1 (sehr schnelle Finalisierung) |

#### Von / An

- **Von** – die Adresse des Senders.
  `From: 0x56Eddb7aa87536c09CCc2793473599fD21A8b17F (Binance 17)`
- **An** – die Adresse des Empfängers (oder Vertragsadresse).
  `To: 0x42008C6392F552fcFF9abbf310E4421eEd22fAF9`

> \* *Binance 17* – **Etherscan** hat die Wallet-Adresse der Börse Binance zugeordnet. Diese Info steht nicht auf der Blockchain selbst, sondern die Analysefunktionen der Seite stellen diese Verbindung her.

Klicke auf eine Adresse – du siehst ihre gesamte Historie und das Guthaben.

#### Wert

Der überwiesene Betrag: `0 ETH ($0.00)`, weil es sich um einen Token-Transfer (ERC-20) handelt: `6.000.000,25342 ($5.997.252,25) Tether USD (USDT)`.

#### Transaktionsgebühr (Gas-Gebühr)

Die Gebühr für die Transaktion. Zwei Werte werden angezeigt:

- **Transaction Fee** – wie viel Gas tatsächlich verbraucht wurde;
  `Transaction Fee: 0,000063066067464358 ETH ($0,14)`
- **Gas Price** – der Preis pro Gas-Einheit (in Gwei);
  `Gas Price: 1,367404598 Gwei (0,000000001367404598 ETH)`

Da hast du es. 6.000.000 $ gesendet und 0,14 $ Gebühren gezahlt.

#### Gas Limit

Das maximale Gas, das du zu zahlen bereit warst, und wie viel tatsächlich verbraucht wurde.
`Gas Limit & Usage by Txn: 220.436 | 46.121 (20,92%)`

---

## Liste der Explorer

Jedes Blockchain-Netzwerk hat seinen eigenen Explorer. Hier sind die bekanntesten:

### Ethereum (ERC-20)

- **Etherscan** – [etherscan.io](https://etherscan.io) – der wichtigste Ethereum-Explorer.
- **Etherscan für Sepolia-Testnetz** – [sepolia.etherscan.io](https://sepolia.etherscan.io) (praktisch zum Üben).

### BNB Chain (BEP-20)

- **BscScan** – [bscscan.com](https://bscscan.com) – das vollwertige Etherscan-Pendant für die Binance Smart Chain.
  Die Oberfläche ist fast identisch – gleiche Status, Blöcke, Gebühren.

### Solana

- **Solscan** – [solscan.io](https://solscan.io) – der wichtigste Explorer für Solana.

Besonderheit von Solana: Transaktionen werden in **Millisekunden** bestätigt. Der Status Pending existiert hier praktisch nicht.

### TRON (TRC-20)

- **Tronscan** – [tronscan.org](https://tronscan.org) – der offizielle Tron-Netzwerk-Explorer.
  Beliebt für USDT – viele nutzen Tron wegen der geringen Gebühren.

### Bitcoin

- **Blockchain.com** – [blockchain.com/explorer](https://www.blockchain.com/explorer) – der bekannteste BTC-Explorer.
- **Mempool.space** – [mempool.space](https://mempool.space) – fortgeschrittener Explorer mit Visualisierung der Transaktionswarteschlange (Mempool).

### Universalsuche

- Bitcoin und Litecoin – [bitaps.com](https://bitaps.com/) – ein alternativer Explorer.

---

## Wie überwache ich ein Wallet: Benachrichtigungen

Du musst nicht jede Transaktion manuell prüfen. Explorer können dich über Wallet-Aktivitäten benachrichtigen.

### Einrichtung auf Etherscan

1. Registriere dich auf [etherscan.io](https://etherscan.io) (kostenlos).
2. Gehe zu **„Watch List"** → **„Add Address"**.
3. Füge die zu überwachende Wallet-Adresse ein.
4. Richte Benachrichtigungen ein:
   - **E-Mail** – du erhältst eine E-Mail bei jeder ein- oder ausgehenden Transaktion;
   - **Telegram** – über den Etherscan Alert Bot.

### Ähnliche Funktionen in anderen Explorern

- **BscScan** – gleiches Watch-List-System, E-Mail-Benachrichtigungen.
- **Solscan** – klicke auf **„Subscribe"** auf der Adressseite.
- **Tronscan** – der **„Follow"**-Button auf der Wallet-Seite.

### Drittanbieter-Überwachungsdienste

- **Dextools** ([dextools.io](https://dextools.io)) – Transaktionen nach Token und Liquiditätspool verfolgen.
- **Nansen** ([nansen.ai](https://nansen.ai)) – professionelles Wallet-Analyse-Tool (kostenpflichtig).
- **Telegram-Bots** – unzählige Bots verfolgen „Wale" und große Transaktionen in Echtzeit.

> Tipp: Wenn du eine wichtige Überweisung erwartest, richte eine Benachrichtigung im Explorer ein. Du wirst benachrichtigt, **bevor** der Empfänger überhaupt sagt „es ist angekommen".

---

## Wie prüfe ich eine Transaktion auf einer Börse (CEX)?

Wenn du Krypto **von einer Börse** an ein externes Wallet sendest oder umgekehrt, läuft der Prozess etwas anders:

1. Finde die **TxID** im Transaktionsverlauf der Börse (normalerweise unter „Verlauf" → „Ein-/Auszahlungen").
2. Kopiere die TxID.
3. Öffne den Explorer für das richtige Netzwerk und füge die TxID ein.

> **Wichtig:** Börsen zeigen oft ihre eigene interne TxID für interne Überweisungen. Wenn du **zwischen Nutzern derselben Börse** gesendet hast – das ist keine Blockchain-Transaktion, sondern nur ein Datenbankeintrag auf Seiten der Börse.

### Woran erkennt man eine interne Überweisung von einer Blockchain-Transaktion?

| Überweisungsart | Hat eine TxID? | Im Explorer prüfbar? |
|-----------------|----------------|----------------------|
| Innerhalb der Börse (Nutzer A → Nutzer B auf Binance) | Ja, aber intern | ❌ Nein |
| Von Börse zu externem Wallet | Ja, echte TxID | ✅ Ja |
| Von Wallet zu Börse | Ja | ✅ Ja |

---

## Was tun, wenn eine Transaktion hängt?

Der Status **Pending** kann von einigen Sekunden bis zu mehreren Tagen dauern. Hier erfährst du, was passiert und was du tun kannst.

### Warum bleiben Transaktionen hängen?

- **Zu niedrige Gas-Gebühr.** In Netzwerken wie Ethereum verarbeiten Miner zuerst die Transaktionen mit den höchsten Gebühren. Wenn du das Gas zu niedrig ansetzt, bleibt die Transaktion in der Warteschlange.
- **Netzwerküberlastung.** In Hype-Momenten (z. B. bei einem beliebten NFT-Drop) kann die Warteschlange enorm werden.
- **Node-Probleme.** Selten, aber manchmal bremst ein bestimmter Validator die Verarbeitung.

### Was du tun kannst

1. **Warten.** Wenn das Netzwerk nicht kritisch überlastet ist, wird die Transaktion durchgehen – nur langsam.
2. **Beschleunigen (Replace-by-Fee).** Manche Wallets (MetaMask, Trust Wallet) haben eine **„Speed Up"**-Option – du sendest dieselbe Transaktion mit einer höheren Gebühr erneut.
3. **Abbrechen.** Wenn dein Wallet **„Cancel"** unterstützt, kannst du die hängende Transaktion durch eine leere Transaktion mit höherer Gas-Gebühr ersetzen.

> **Wenn die Transaktion nach 24 Stunden immer noch Pending ist** – dann wird sie höchstwahrscheinlich „herausfallen" (nie in einen Block aufgenommen), und das Geld wird zurückgegeben.

### Wann solltest du in Panik geraten? (Spoiler: Fast nie)

| Status | Solltest du dir Sorgen machen? |
|--------|--------------------------------|
| Pending (bis zu 30 Minuten) | Nein, das ist normal |
| Pending (1–6 Stunden) | Es lohnt sich, Gas und Netzwerk zu prüfen |
| Pending (über 24 Stunden) | Transaktion wird wahrscheinlich nicht durchgehen – Geld kommt zurück |
| Success | ✅ Die Überweisung gilt als abgeschlossen |
| Failed | ❌ Geld zurück (abzüglich Gas-Gebühr) |

---

## Checkliste: Was du nach dem Senden prüfen solltest

Wenn du Krypto gesendet hast, geh diese Liste durch:

| # | Schritt | Worauf achten |
|---|---------|---------------|
| 1 | TxID aus dem Wallet kopieren | Stelle sicher, dass es kein leerer String ist |
| 2 | Explorer öffnen (Etherscan usw.) | TxID in die Suche einfügen |
| 3 | Status prüfen | ✅ Success = erledigt |
| 4 | Betrag (Value) überprüfen | Stimmt er mit dem überein, was du gesendet hast? |
| 5 | Empfängeradresse (To) prüfen | Hast du an die richtige Adresse gesendet? |
| 6 | Anzahl der Bestätigungen ansehen | Je mehr, desto sicherer |
| 7 | TxID an den Empfänger senden | Das ist der Nachweis der Überweisung |

---

## Häufig gestellte Fragen

### Kann ich eine Transaktion ohne TxID überprüfen?

Ja, wenn du die **Adresse des Senders oder Empfängers** kennst. Gib die Adresse in die Suche des Explorers ein – du siehst **alle ihre Transaktionen** und kannst die richtige anhand von Betrag, Datum oder Hash finden.

### Wie überprüfe ich, ob ein Betrüger eine echte Überweisung geschickt hat?

Betrüger schicken oft Screenshots oder PDFs mit einem „Nachweis" einer Überweisung. Die einzige Möglichkeit zur Überprüfung:

1. Fordere die TxID an.
2. Füge sie in einen Explorer ein.
3. Wenn es keine Transaktion gibt – ist sie gefälscht.

### Was sind Bestätigungen?

Jeder neue Block, der nach dem Block mit deiner Transaktion hinzugefügt wird, gibt **+1 Bestätigung**. Je mehr Bestätigungen, desto schwieriger ist es, die Transaktion rückgängig zu machen.

- Für kleine Beträge: 1–3 Bestätigungen reichen.
- Für große Beträge: 6+ Bestätigungen.
- Bei Bitcoin warten Börsen normalerweise auf 3–6 Bestätigungen.

### Warum wurde die Gebühr erhoben, obwohl die Transaktion fehlgeschlagen ist?

Gas ist die Bezahlung für **Berechnung**, nicht für den Erfolg. Wenn eine Transaktion fehlschlägt (z. B. unzureichendes Token-Guthaben), hat der Miner den Code trotzdem ausgeführt und die Gebühr verdient. Das Geld **kommt** in dein Wallet zurück, aber das Gas ist verbraucht.

### Kann ich eine bereits gesendete Transaktion stornieren?

Nein. Wenn eine Transaktion bestätigt ist (Success), ist sie **dauerhaft** in der Blockchain aufgezeichnet. Niemand – nicht der Entwickler, nicht ein Miner, nicht eine Regierung – kann sie rückgängig machen.

---

## Zusammenfassung

Eine Transaktion in der Blockchain zu überprüfen, ist eine Superkraft, die dir das traditionelle Finanzsystem nicht gibt:

- Du kannst **jede** Operation öffentlich und transparent einsehen.
- Du musst nicht den Support anrufen oder auf eine Antwort warten.
- Die TxID ist ein rechtlich bedeutsamer Nachweis einer Überweisung.
- Du kannst jedes Wallet in Echtzeit verfolgen.

Denk einfach an drei Dinge:

1. **TxID = Quittungsnummer.** Speichere sie nach jeder Sendung.
2. **Explorer sind kostenlos.** Etherscan, BscScan, Solscan, Tronscan – alle hast du immer zur Hand.
3. **Success-Status = Geld angekommen.** Wenn der Status Success ist, ist alles andere egal.

Krypto gibt dir **die volle Kontrolle und volle Transparenz**. Eine Transaktion zu prüfen, ist der erste Schritt, um dich in dieser Welt sicher zu fühlen.
