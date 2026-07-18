---
weight: 3
title: "Block-Bestätigungen: Was ein Block ist und warum du warten musst"
description: "Was ein Block in einer Blockchain ist, wie Bestätigungen funktionieren und wann eine Transaktion als sicher gilt"
category: "how-it-works"
translationKey: "block-confirmations"
slug: "block-bestaetigungen"
keywords:
  - Blockbestätigung
  - Blockchain-Block
  - Transaktionsbestätigung
  - Bitcoin-Bestätigung
  - Blockzeit
  - 6 Bestätigungen
prev: "/de/learn/how-it-works/warum-eine-uberweisung-30-kosten-kann"
next: "/de/learn/how-it-works/warum-transaktionen-haengen-bleiben"
---

## Block-Bestätigungen: Was ein Block ist und warum du warten musst

---

Du schickst Krypto. Der Bildschirm sagt: „Transaktion gesendet." Aber anstatt die Gutschrift zu sehen, erscheint: „Warte auf Bestätigung…"

Eine Minute vergeht. Dann noch eine. Und eine dritte.

Und die Coins sind immer noch nicht angekommen.

Warum können wir Dinge nicht einfach sofort senden? Es ist doch digitales Geld!

Die Antwort liegt in der Funktionsweise der Blockchain selbst. Deine Transaktion fliegt nicht direkt von Wallet zu Wallet. Zuerst muss sie in einem **Block** landen – und erst dann wird sie Teil der Geschichte.

> In diesem Artikel erfährst du: Was ein Block ist, warum Bestätigungen nötig sind, wie viele du abwarten solltest und wann eine Transaktion als sicher gilt.

---

## Was ist ein Block in einer Blockchain

Eine Blockchain ist eine Kette von Blöcken. Klingt wie eine Tautologie, ist aber genau das, was sie ist.

Ein **Block** ist ein Behälter, der Transaktionen bündelt. Stell dir das wie eine Seite in einem Hauptbuch vor. Auf eine einzelne Seite passen mehrere Überweisungen. Wenn die Seite voll ist, wird sie ans Buch angehängt und eine neue Seite beginnt.

In einer Blockchain:

- enthält jeder Block eine **Sammlung von Transaktionen** (von ein paar wenigen bis zu Tausenden);
- kommen Blöcke nacheinander in einer Reihenfolge;
- verweist jeder neue Block auf den vorherigen (daher „Kette").

Was in einem Block steckt:

| Was drin ist | Beispiel |
|---|---|
| **Block-Header** | Hash des vorherigen Blocks, Zeitstempel, Schwierigkeit, Nonce |
| **Transaktionsliste** | Alle in diesem Block enthaltenen Überweisungen |
| **Metadaten** | Blockgröße, Version, Anzahl Transaktionen |

Wenn jemand versucht, eine einzelne Transaktion in einem alten Block zu ändern – dann ändert sich der Hash dieses Blocks und die gesamte nachfolgende Kette wird ungültig. Das macht eine Blockchain **unveränderlich**.

> Mehr zu Hashes und Kryptographie: [Hash-Funktion](/de/glossary/#hash-funktion).

---

## Wer erstellt Blöcke

Verschiedene Blockchains erstellen Blöcke auf unterschiedliche Weise, aber die Idee ist dieselbe: **Jemand muss Transaktionen sammeln, in einen Block packen und dem Netzwerk vorschlagen.**

### Bitcoin: Miner (Proof of Work)

Miner sammeln Transaktionen aus dem Mempool in einen Block und beginnen, ein mathematisches Rätsel zu lösen. Der Erste, der eine Lösung findet, darf seinen Block an die Kette anhängen und die Belohnung kassieren.

Dieser Prozess erfordert enorme Rechenleistung. Deshalb erscheint bei Bitcoin im Schnitt nur alle **10 Minuten** ein neuer Block.

### Ethereum: Validatoren (Proof of Stake)

Seit der Umstellung auf Proof of Stake werden Blöcke in Ethereum von **Validatoren** erstellt – Teilnehmern, die mindestens 32 ETH eingesetzt haben. Sie „minen" nicht – sie bestätigen lediglich Blöcke.

Ein neuer Block in Ethereum erscheint etwa alle **~12 Sekunden**.

### Solana und andere schnelle Netzwerke

Solana nutzt eine Kombination aus Proof of History und Proof of Stake. Blöcke erscheinen hier etwa alle **~400 Millisekunden**. Eine Transaktion wird fast sofort bestätigt.

> Mehr zu Konsensmechanismen: [Proof of Work](/de/glossary/#proof-of-work), [Proof of Stake](/de/glossary/#proof-of-stake).

---

## Warum du auf Bestätigungen warten musst

Kommen wir zur Hauptfrage: Warum können Coins nicht sofort gutgeschrieben werden?

### Das Double-Spend-Problem

Stell dir vor, du hast 1 BTC. Du schickst ihn an Alice – und gleichzeitig denselben 1 BTC an Bob. Wenn Transaktionen sofort gutgeschrieben würden, könnten beide durchgehen. Das Netzwerk wäre verwirrt, wer die Coins nun wirklich bekommen hat.

Die Blockchain löst das so:

1. Die Transaktion wird an das Netzwerk gesendet.
2. Sie landet im Mempool (einer temporären Warteschlange).
3. Ein Miner/Validator nimmt sie in einen Block auf.
4. Einmal aufgenommen – ist ein Double Spend unmöglich.

> Bis eine Transaktion in einem Block ist, gilt sie nicht als endgültig.

### Warum mehrere Bestätigungen

Eine Bestätigung bedeutet, dass deine Transaktion in einen Block aufgenommen wurde. Aber eine einzige Bestätigung allein ist nicht zuverlässig genug.

Warum? Weil theoretisch ein Miner einen **Fork** erstellen könnte – einen alternativen Block mit einer anderen Transaktion. Wenn dieser Fork länger wird als die Hauptkette, wird die ursprüngliche Transaktion rückgängig gemacht.

Je mehr Blöcke nach deinem kommen – desto schwieriger wird es, die Transaktion rückgängig zu machen. Jeder zusätzliche Block ist wie eine weitere Schicht Beton, die auf die vorherige gegossen wird.

| Anzahl Bestätigungen | Zuverlässigkeit |
|---|---|
| 0 | Transaktion im Mempool – wird möglicherweise nicht bestätigt |
| 1 | In einem Block gelandet, aber Umkehrung durch Fork möglich |
| 3 | Zuverlässig genug für kleine Beträge |
| 6 | **Sehr zuverlässig** – der Standard für Bitcoin |
| 12+ | Maximale Sicherheit |

---

## Wie viele Bestätigungen sind nötig

Die Anzahl der erforderlichen Bestätigungen hängt vom Überweisungsbetrag und vom Netzwerk ab.

### Bitcoin: 6 Bestätigungen

Für Bitcoin sind **6 Bestätigungen** der Standard. Das bedeutet etwa eine Stunde Wartezeit.

Warum ausgerechnet 6? Mathematische Modelle zeigen, dass die Wahrscheinlichkeit einer Rückabwicklung nach 6 Blöcken gegen Null geht. Selbst wenn ein Angreifer 10 % der Netzwerk-Hashrate kontrolliert, liegt die Chance auf einen erfolgreichen Angriff nach 6 Blöcken unter 0,1 %.

Für kleine Überweisungen (wie einen Kaffee) reichen 1–3 Bestätigungen. Bei großen Beträgen – nimm lieber alle 6.

### Ethereum: 12–30 Bestätigungen

Ethereum ist schneller: ein Block alle ~12 Sekunden. Aber aufgrund des Finalitätsmechanismus liegt die Standardzahl der Bestätigungen bei **12–30 Blöcken** (~2–6 Minuten).

Nach 32 Blöcken (einem sogenannten Checkpoint) gilt eine Transaktion als endgültig – sie kann selbst theoretisch nicht mehr rückgängig gemacht werden.

### Tabelle: Bestätigungszeit für verschiedene Netzwerke

| Netzwerk | Blockzeit | Standard-Bestätigungen | Gesamte Wartezeit |
|---|---|---|---|
| Bitcoin | ~10 min | 6 | ~60 min |
| Bitcoin Cash | ~10 min | 3 | ~30 min |
| Ethereum | ~12 s | 12–30 | ~2–6 min |
| Litecoin | ~2,5 min | 6 | ~15 min |
| Solana | ~400 ms | 1 | Sofort |
| TRON | ~3 s | 19 | ~1 min |
| BNB Chain | ~3 s | 15 | ~45 s |
| Dogecoin | ~1 min | 5 | ~5 min |

> **Wichtig:** Börsen und Dienste legen ihre eigenen Bestätigungsanforderungen fest. Binance schreibt eine Einzahlung vielleicht schon nach 1 Bitcoin-Bestätigung gut, während Coinbase auf 3 wartet. Das ist deren Sicherheitsrichtlinie.

---

## Was der Benutzer in jeder Phase sieht

Betrachten wir eine Transaktion mit den Augen des Benutzers:

| Status | Was passiert | Sender sieht | Empfänger sieht |
|---|---|---|---|
| **Ausstehend** | Transaktion ist im Mempool, wartet auf Aufnahme in einen Block | „Gesendet" | Nichts |
| **1 Bestätigung** | Transaktion ist in einem Block | „Bestätigt (1/6)" | „Warte auf Gutschrift" |
| **3 Bestätigungen** | Sicher für kleine Beträge | „Bestätigt (3/6)" | „Warte auf Gutschrift" |
| **6 Bestätigungen** | Volle Sicherheit für Bitcoin | „Abgeschlossen" | „Gutschrift erhalten" |

Hinweis: Der Empfänger kann eine unbestätigte Transaktion über einen Block-Explorer sehen (z. B. [mempool.space](https://mempool.space) für Bitcoin). Sein Wallet zeigt aber trotzdem einen Nullsaldo, bis genügend Bestätigungen eingegangen sind.

---

## Eine wahre Geschichte

Ich habe mal ein Handy online gekauft und mit Bitcoin bezahlt. Der Verkäufer bat mich, auf **3 Bestätigungen** zu warten – „nur zur Sicherheit."

Ich schickte die Bitcoins. Die Transaktion schaffte es nach 8 Minuten in den ersten Block. Der zweite – weitere 12 Minuten später. Und der dritte… blieb hängen.

Das Netzwerk war überlastet: Mehr als 100.000 unbestätigte Transaktionen saßen im Mempool. Meine Gebühr war durchschnittlich – die Miner suchten sich die aus, die mehr zahlten.

Der dritte Block kam erst 47 Minuten später.

**Fazit:** Ich wartete 3 Tage auf das Handy und 67 Minuten auf die Transaktionsbestätigung. Der Verkäufer verschickte das Handy erst nach 3 Bestätigungen.

> Seitdem setze ich meine Gebühr immer etwas höher an, wenn die Zeit eine Rolle spielt. 1 $ zu sparen ist nicht eine Stunde Wartezeit wert.

---

## Kann man eine Bestätigung beschleunigen?

Ja, in manchen Fällen ist das möglich.

### 1. Die richtige Gebühr wählen

Je höher die Gebühr, desto schneller nehmen Miner deine Transaktion auf. Prüfe vor dem Senden die aktuelle Netzwerkauslastung:

- Bitcoin: [mempool.space](https://mempool.space)
- Ethereum: [etherscan.io/gastracker](https://etherscan.io/gastracker)

### 2. Replace-by-Fee (RBF) nutzen

Bitcoin unterstützt RBF – ein Mechanismus, mit dem du eine unbestätigte Transaktion durch dieselbe mit einer höheren Gebühr ersetzen kannst. Aktiviere diese Option vorher in deinem Wallet.

### 3. Schnelle Netzwerke wählen

Wenn du nicht auf Bitcoin oder Ethereum angewiesen bist, probiere:

- **Litecoin** – ein Block alle 2,5 Minuten;
- **Solana** – sofortige Bestätigungen;
- **Lightning Network** – Bitcoins zweite Schicht, Bestätigung in Sekunden.

> Geschwindigkeit bedeutet nicht immer Sicherheit. Schnelle Netzwerke verwenden einen anderen Konsensmechanismus, und die Anzahl der Bestätigungen zählt auch dort – die Blöcke kommen nur häufiger.

---

## Zusammenfassung

Transaktionsbestätigungen sind kein Fehler oder träges Netzwerkverhalten. Sie sind ein **grundlegender Schutz** gegen Double Spending und Betrug.

**Kurz gesagt:**

- Ein **Block** ist ein Behälter für Transaktionen. Jeder neue Block verweist auf den vorherigen.
- Eine **Bestätigung** bedeutet, dass deine Transaktion in einen Block aufgenommen wurde. Eine Bestätigung = ein Block nach deiner Transaktion.
- **Je mehr Bestätigungen, desto sicherer.** 6 für Bitcoin, 12–30 für Ethereum.
- **Die Wartezeit hängt vom Netzwerk ab:** von 400 ms (Solana) bis zu einer Stunde (Bitcoin).
- **Du kannst Dinge beschleunigen:** Gebühr anpassen, RBF nutzen oder ein schnelleres Netzwerk wählen.

Kryptowährung ist ein Abwägen zwischen Geschwindigkeit und Sicherheit. Je zuverlässiger das Netzwerk, desto länger wartest du. Aber sobald eine Transaktion endgültig bestätigt ist – wird sie Teil einer Geschichte, die niemand mehr umschreiben kann.

> Wie man so schön sagt: „Not your keys, not your coins." Fügen wir hinzu: „Nicht bestätigt, nicht deine Transaktion."

---

## FAQ

### Wie lange muss ich auf eine Bitcoin-Transaktion warten?

In der Regel 10–60 Minuten. Es hängt alles von der Gebühr und der Netzwerkauslastung ab. Die erste Bestätigung kommt normalerweise nach 10–30 Minuten, 6 Bestätigungen dauern etwa eine Stunde.

### Kann ich eine Transaktion vor der Bestätigung stornieren?

Wenn die Transaktion noch im Mempool ist – kannst du versuchen, sie per RBF zu ersetzen (falls dein Wallet das unterstützt). Ist sie bereits in einem Block – nein. Sind mehrere Blöcke vergangen – ist eine Rückabwicklung praktisch unmöglich.

### Warum kommt eine Einzahlung auf einer Börse schneller an als erwartet?

Börsen schreiben Gelder oft schon nach 1–2 Bestätigungen gut, ohne auf alle 6 zu warten. Das ist das Risiko der Börse, nicht deines. Allerdings lassen sie dich die Gelder möglicherweise erst abheben, wenn die volle Anzahl an Bestätigungen erreicht ist.

### Was ist ein Orphan-Block?

Das ist ein Block, der zur gleichen Zeit wie ein anderer gemined wurde und nicht in die Hauptkette gelangt ist. Transaktionen aus einem solchen Block gehen zurück in den Mempool und warten auf die nächste Bestätigung.

### Wie viele Bestätigungen braucht USDT?

Das hängt vom Netzwerk ab: für ERC-20 (Ethereum) – 12–30, für TRC-20 (TRON) – 19, für BEP-20 (BNB Chain) – 15.

### Wie überprüfe ich die Anzahl der Bestätigungen?

Nutze einen Block-Explorer. Für Bitcoin – [mempool.space](https://mempool.space), für Ethereum – [etherscan.io](https://etherscan.io). Füge einfach deinen Transaktions-Hash ein.

### Beeinflusst der Überweisungsbetrag die Geschwindigkeit?

Nein. Die Gebühr hängt nicht vom Betrag ab. Eine 1‑$-Transaktion und eine 1.000.000‑$-Transaktion mit derselben Gebühr werden zur gleichen Zeit bestätigt.
