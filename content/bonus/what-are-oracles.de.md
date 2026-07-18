---
weight: 2
title: "Was sind Orakel in der Kryptowelt"
description: "Orakel — wie Smart Contracts den echten Bitcoin-Preis erfahren. Chainlink, Preis-Feeds, Daten aus der realen Welt"
category: "bonus"
translationKey: "what-are-oracles"
slug: "oracles-erklaert"
keywords:
  - Orakel
  - Chainlink
  - Smart-Contract-Daten
  - Preis-Feed
  - Off-Chain-Daten
prev: "/de/bonus/was-ist-eine-dao"
next: "/de/bonus/staking-vs-farming"
---

## Was sind Orakel: Wie Smart Contracts die echte Welt sehen

---

Stell dir einen Roboter vor, der in einem abgedichteten Raum ohne Fenster sitzt.

Er ist intelligent. Er befolgt Anweisungen perfekt. Aber er hat keine Ahnung, was draußen passiert — das Wetter, der Dollarkurs, wer gewonnen hat.

> **Ein Smart Contract ist genau so ein Roboter.**

Er lebt innerhalb einer Blockchain und kann nur mit dem interagieren, was bereits auf der Chain ist. Daten aus der Außenwelt — Preise, Wechselkurse, Sportergebnisse — sind tabu.

Wie bringt man also einen Smart Contract dazu, dir den aktuellen Bitcoin-Preis zu verraten?

---

## Das Problem: Die Blockchain ist von externen Daten abgeschnitten

### Warum die Blockchain die echte Welt nicht sehen kann

Die Blockchain ist ein geschlossenes System.

Jeder Knoten speichert eine identische Kopie der Daten. Damit alles fair bleibt, müssen alle Knoten **eine einzige Übereinkunft (Konsens)** erzielen.

Aber wie können Knoten sich darüber einig werden, was außerhalb des Netzwerks passiert?

Zum Beispiel:
- Bitcoin-Preis auf Binance — 60.000 $;
- Bitcoin-Preis auf Coinbase — 60.100 $;
- auf einer kleinen Börse — 59.500 $.

> **Welcher Preis ist der richtige? Und wer entscheidet das?**

Die Blockchain kann das nicht von alleine beantworten. Sie braucht einen Helfer.

---

### Beispiel: Regenversicherung

Angenommen, es gibt einen Smart Contract, der eine Versicherung auszahlt, wenn es morgen in Berlin regnet.

Problem:
- der Smart Contract kann nicht aus dem Fenster schauen;
- er kann keine Wetter-Website abrufen;
- er hat keine Ahnung, ob es tatsächlich regnet.

Ohne externe Daten ist dieser Vertrag nutzlos.

---

## Die Lösung: Orakel — die Brücke zwischen Blockchain und der Welt

### Was ist ein Orakel

Ein **Orakel** ist ein Dienst, der Daten aus der Außenwelt in eine Blockchain liefert.

Einfach gesagt:
> **Ein Orakel bringt einem Smart Contract die Informationen, die er nicht selbst beschaffen kann.**

Orakel können liefern:
- **Asset-Preise** — BTC/USD, ETH/USD;
- **Wetter** — Temperatur, Niederschlag;
- **Sportergebnisse** — wer gewonnen hat;
- **Ereignisse** — ob eine Zahlung durchgegangen ist, ob ein Datum erreicht wurde;
- **Zufallszahlen** — für Lotterien und Spiele.

---

### Wie es funktioniert

1. Der Smart Contract fordert Daten an (z. B. „Wie hoch ist der ETH-Kurs gerade?");
2. Das Orakel holt die Daten aus einer externen Quelle (Börse, API);
3. Das Orakel liefert die Daten in die Blockchain;
4. Der Smart Contract nutzt die Daten, um seine Logik auszuführen.

---

### Arten von Orakeln

| Typ | Beschreibung | Beispiel |
|-----|--------------|---------|
| **Software** | Sammelt Daten aus dem Internet | Preise, Wetter, APIs |
| **Hardware** | Liest Daten von physischen Sensoren | Temperatur, GPS, RFID |
| **Inbound** | Bringt Daten in die Blockchain | Wechselkurs |
| **Outbound** | Sendet Daten aus der Blockchain heraus | Transaktionsbenachrichtigung |
| **Zentralisiert** | Einzelne Datenquelle | Einfach, aber unzuverlässig |
| **Dezentralisiert** | Mehrere Quellen | Zuverlässig, aber komplexer |

---

### Das Vertrauensproblem

Hier ist die große Frage:

> **Wenn ein Smart Contract einem einzigen Orakel vertraut — was bringt dann die Blockchain?**

Wenn das Orakel ein einzelner Ausfallpunkt ist, kann es:
- falsche Daten liefern (Fehler);
- manipulierte Daten liefern (Angriff);
- einfach offline gehen.

Die Lösung — **dezentrale Orakel**.

Statt einer einzigen Datenquelle wird ein Netzwerk unabhängiger Knoten verwendet. Jeder Knoten sammelt Daten selbstständig. Wenn die meisten Knoten denselben Wert bestätigen — gelten die Daten als vertrauenswürdig.

---

## Chainlink: Das bekannteste Orakel

### Was ist Chainlink

**Chainlink** ist das größte dezentrale Orakel-Netzwerk.

Statt eines einzelnen Servers nutzt Chainlink Hunderte unabhängiger Knoten, die:
- Daten von mehreren Börsen und APIs sammeln;
- Ergebnisse untereinander abgleichen;
- abgestimmte Daten an die Blockchain liefern.

> Chainlink unterstützt Dutzende Blockchains und Tausende von Smart Contracts.

---

### Price Feeds: Fertige Preiskanäle

Chainlinks beliebtester Dienst sind **Price Feeds**.

Das sind fertige Datenquellen, die bereits auf der Blockchain leben.

Ein Smart Contract kann zum Beispiel einfach die **ETH/USD Price Feed**-Adresse aufrufen und den aktuellen Preis abrufen. Kein eigenes Orakel nötig — alles ist startklar.

---

### Wie Chainlink Daten schützt

Chainlink verwendet mehrere Schutzebenen:

1. **Dezentralisierung** — Daten werden von vielen unabhängigen Knoten gesammelt;
2. **Aggregation** — der endgültige Preis ist der Median aller Quellen;
3. **Anreize** — Knoten erhalten Belohnungen für ehrliche Arbeit und verlieren ihre Hinterlegung bei Betrug.

👉 Dadurch ist Chainlink der De-facto-Standard für DeFi-Anwendungen.

---

### Praxisbeispiel: Krypto-besicherte Kredite

Stell dir ein DeFi-Protokoll vor, das Kredite gegen ETH vergibt:

- 🔹 ein Nutzer hinterlegt 10 ETH als Sicherheit;
- 🔹 das Protokoll ruft den ETH-Preis vom Chainlink-Orakel ab;
- 🔹 fällt die Sicherheit unter einen sicheren Wert — wird die Liquidation ausgelöst.

Ohne ein zuverlässiges Orakel:
- falscher Preis → falsche Liquidation → Nutzer verliert Geld;
- überhöhter Preis → das Protokoll geht ein Risiko ein.

> **Ein Orakel ist nicht nur „Daten". Es ist die Sicherheit des Protokolls.**

---

## Fazit

Orakel sind ein unsichtbarer, aber essenzieller Teil der Kryptowelt.

- Smart Contracts sind **blind** — sie können die Außenwelt nicht sehen;
- Orakel **geben ihnen Sicht** — sie liefern Daten aus der realen Welt;
- Chainlink ist der beliebteste und am meisten erprobte Orakel-Anbieter.

Ohne Orakel würde nichts davon funktionieren:
- DeFi-Protokolle (Aave, Compound);
- Stablecoins (DAI prüft Sicherheitenpreise);
- Versicherungs-Smart-Contracts;
- Prognosemärkte.

> **Orakel sind die Brücke zwischen Blockchain und Realität. Ohne diese Brücke ist DeFi nur ein Sandkastenspiel.**

---

## FAQ

### Wie unterscheidet sich ein Orakel von einer normalen API?

Eine API ist nur ein Weg, Daten abzurufen. Ein Orakel holt nicht nur Daten — es **liefert sie in die Blockchain** mit Garantien für Zuverlässigkeit.

### Kann ich nur ein einziges Orakel verwenden?

Kannst du, aber es ist riskant. Ein zentralisiertes Orakel ist ein einzelner Ausfallpunkt. DeFi-Protokolle verwenden in der Regel dezentrale Netzwerke wie Chainlink.

### Muss ich für Orakel bezahlen?

Ja. Ein Smart Contract zahlt eine Gebühr an Orakel-Knoten für die Bereitstellung von Daten. Bei Chainlink wird die Gebühr in LINK-Token bezahlt.

### Kann ein Orakel falsch liegen?

Kann es. Auch dezentrale Orakel sind nicht perfekt. Aber je mehr unabhängige Datenquellen du hast — desto geringer ist die Fehlerwahrscheinlichkeit.
