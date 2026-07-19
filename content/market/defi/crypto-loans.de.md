---
weight: 130
title: "Kredite ohne Bank: Wie DeFi-Darlehen funktionieren"
description: "Wie Krypto-Darlehen ohne Bank über DeFi funktionieren: Besicherung, Liquidation, Risiken. Aave, Compound"
category: "defi"
translationKey: "crypto-loans"
slug: "kredite-ohne-bank-defi"
keywords:
  - DeFi Kredite
  - Krypto Darlehen
  - Aave
  - Compound
  - Besicherung
  - Liquidation
  - Überbesicherung
---

## DeFi-Darlehen: Wie du dir Geld leihst – ohne Bank und ohne Schufa

---

Stell dir vor: Du brauchst schnell Geld, aber die Bank lehnt dich ab wegen einer schlechten Bonität. Oder du willst einen Kredit aufnehmen, hast aber keine Lust auf [KYC](/de/glossary/#kyc) und ellenlange Formulare.

In [DeFi](/de/glossary/#defi) ist das kein Problem.

> **Ein Krypto-Darlehen** ist Geld, das du dir gegen deine Kryptos als Sicherheit leihst – ohne eine einzige Frage zu deiner Kreditgeschichte.

Kein Einkommensnachweis, keine nervigen Anrufe von der Bank, kein tagelanges Warten auf die Zusage. Der Code erledigt alles.

In diesem Artikel erfährst du:

> - wie DeFi-Darlehen funktionieren;
> - warum du mehr Sicherheiten hinterlegen musst, als du dir leihst;
> - was Liquidation ist und wie du sie vermeidest;
> - die wichtigsten Risiken;
> - echte Beispiele: Aave, Compound, MakerDAO.

---

## Wie ein DeFi-Darlehen funktioniert

In der traditionellen Welt läuft ein Kredit so ab:

- du beweist der Bank, dass du das Geld zurückzahlen kannst;
- die Bank prüft deine Kreditwürdigkeit und dein Einkommen;
- wenn alles passt – bekommst du das Geld.

[DeFi](/de/glossary/#defi) funktioniert ganz anders:

> **du beweist nicht, dass du zahlungsfähig bist – du hinterlegst Sicherheiten.**

Der Ablauf ist einfach:

1. Du zahlst Krypto (z. B. ETH) in einen Smart Contract ein;
2. Der Smart Contract erlaubt dir, eine andere [Kryptowährung](/de/glossary/#cryptocurrency) (wie USDC) zu leihen;
3. Du nutzt das geliehene Geld;
4. Wenn du den Kredit plus Zinsen zurückzahlst – bekommst du deine Sicherheiten zurück.

> Der entscheidende Unterschied: **Ein Kredit wird nicht von einer Person oder Firma vergeben, sondern von Code.**

Niemand fragt, wo du arbeitest oder wie viel du verdienst. Schließe einfach deine [Wallet](/de/glossary/#wallet) an und zahle Sicherheiten ein.

---

## Überbesicherung: Warum du mehr hinterlegen musst, als du dir leihst

In DeFi gibt es keine Inkassobüros oder Gerichte. Wenn ein Kreditnehmer nicht zurückzahlt, kann ein Smart Contract ihn nicht verklagen.

Deshalb funktioniert das System anders:

> **Die Sicherheiten müssen mehr wert sein als der Kreditbetrag.**

Das nennt man **Überbesicherung** (Overcollateralization).

So sieht das in der Praxis aus:

- du willst dir 1.000 $ in USDC leihen;
- das Protokoll verlangt mindestens 1.500 $ an Sicherheiten (150 %);
- du zahlst ETH im Wert von 1.500 $ ein;
- du bekommst 1.000 $.

Warum genau 150 %? Das ist ein Puffer gegen Kursschwankungen. Fällt ETH um 30 %, ist immer noch genug Sicherheit da, um den Kredit zu decken.

### Übliche Werte

| Protokoll | Max. Kredit (LTV)         | Beispiel                            |
|-----------|---------------------------|-------------------------------------|
| Aave      | 50–75 % der Sicherheiten | Bei 100 $ ETH leiht du 50–75 $     |
| Compound  | 50–75 %                  | Ähnlich                             |
| MakerDAO  | 66 % (150 % überbesichert)| Bei 100 $ ETH mintest du ~66 $ DAI |

Je volatiler der Vermögenswert – desto niedriger der LTV (Loan-to-Value), also desto weniger kannst du dir dagegen leihen.

---

## Liquidation: Wenn deine Sicherheiten im Wert fallen

Das Wichtigste, was du über DeFi-Darlehen wissen musst:

> **Wenn der Preis deiner Sicherheiten zu stark fällt – verlierst du sie.**

Das nennt man **Liquidation**.

### Wie es abläuft

Angenommen, du hast ETH im Wert von 1.500 $ eingezahlt und dir 1.000 $ USDC geliehen. Dein Health Factor liegt bei 1,5.

Wenn der ETH-Kurs fällt:

- 1.500 $ → 1.300 $ – noch sicher;
- 1.300 $ → 1.100 $ – der Health Factor sinkt;
- 1.100 $ → 1.050 $ – kritische Schwelle.

Sobald der Health Factor 1 erreicht (oder tiefer, je nach Protokoll), wird eine **automatische Liquidation** ausgelöst:

> Der Smart Contract verkauft einen Teil deiner Sicherheiten, um die Schulden zu decken.

Auf den liquidierten Betrag wird eine **Strafe** erhoben – meist 5–15 % der Summe. Das ist die Risikogebühr, die an Liquidatoren geht (meist Bots, die die Positionen überwachen).

### So vermeidest du die Liquidation

1. **Leih dir nicht das Maximum.** Wenn du 75 $ auf 100 $ leihen könntest – leihe dir 40–50 $. Je kleiner die Schuld, desto größer dein Sicherheitspuffer.
2. **Beobachte den Kurs.** An volatilen Tagen prüfe deinen Health Factor alle paar Stunden.
3. **Zahle mehr Sicherheiten ein.** Fällt ETH – zahle mehr ETH (oder [Stablecoins](/de/glossary/#stablecoin)) nach, um deinen Health Factor zu erhöhen.
4. **Nutze Benachrichtigungen.** Es gibt Dienste, die dich warnen, wenn dein Health Factor kritisch wird (z. B. DeBank oder Aaves integrierte Benachrichtigungen).

---

## Beispiele für Protokolle

### Aave

**[Aave](https://aave.com)** – das größte DeFi-Kreditprotokoll.

Highlights:

- du kannst dir gegen mehr als 20 Vermögenswerte Geld leihen (ETH, USDC, DAI, WBTC, MATIC u. a.);
- die Zinssätze können **stabil** (stable rate) oder **variabel** (variable rate) sein;
- **Flash Loans** sind verfügbar – blitzschnelle Kredite ohne Sicherheiten (müssen aber in derselben Transaktion zurückgezahlt werden);
- der Zustand deiner Position wird als Health Factor angezeigt: >1 bedeutet alles okay, =1 bedeutet Liquidation.

### Compound

**[Compound](https://compound.finance)** – eines der ersten DeFi-Protokolle, gestartet 2018.

Highlights:

- funktioniert ähnlich wie Aave, jedoch ohne stabile Zinssätze;
- verwendet algorithmisch angepasste Zinssätze;
- lässt sich mit vielen [Wallets](/de/glossary/#wallet) und Diensten verbinden.

### MakerDAO

**[MakerDAO](https://makerdao.com)** – ein etwas anderes Modell.

Hier nimmst du nicht einfach einen Kredit auf – du **erschaffst den DAI-Stablecoin**, indem du ETH (oder andere Assets) als Sicherheit hinterlegst. Im Grunde ist es dasselbe wie ein Kredit: du sperrst ETH, bekommst DAI, und wenn du den DAI plus Zinsen zurückgibst – werden deine Sicherheiten freigegeben.

> MakerDAO ist das Rückgrat des gesamten DeFi-Ökosystems. Hunderte von Protokollen nutzen DAI.

---

## DeFi-Darlehen vs. Bankdarlehen: Vergleich

| Kriterium              | Bankdarlehen                         | DeFi-Darlehen                           |
|------------------------|--------------------------------------|-----------------------------------------|
| Bonitätsprüfung        | Erforderlich                         | Nicht nötig                             |
| Bearbeitungszeit       | Tage bis Wochen                      | Sekunden                                |
| Sicherheiten           | Meist nicht nötig (Privatkredite)    | Erforderlich (150 %+ des Kreditbetrags) |
| Zinsen                 | 5–30 % p.a. (abhängig von Bonität)   | 1–15 % p.a. (abhängig von Angebot/Nachfrage)|
| Zugang                 | Personalausweis, [KYC](/de/glossary/#kyc), 18+            | Internetverbindung, jedes Alter         |
| Liquidation            | Gericht, Gerichtsvollzieher, Mahnung | Automatisch, von Bots ausgeführt        |
| Geografie              | Nur im Land der Bank                 | Weltweit                                |
| Geschäftszeiten        | Während der Öffnungszeiten           | 24/7, keine freien Tage                 |

> Der Hauptunterschied: Eine Bank vertraut dir aufgrund deiner Vergangenheit. DeFi vertraut dir aufgrund deiner aktuellen Sicherheiten.

---

## Risiken von DeFi-Darlehen

DeFi-Kredite bedeuten nicht nur Freiheit – sie bringen auch ernsthafte Risiken mit sich.

### 1. Volatilität und Liquidation

Kryptowährungen gehören zu den volatilsten Vermögenswerten der Welt. ETH kann an einem einzigen Tag um 20–30 % fallen. Wenn dein Health Factor bereits niedrig war – ist die Liquidation vorprogrammiert.

> Empfehlung: Halte deinen Health Factor an ruhigen Tagen nicht unter 1,5–2,0 und an volatilen Tagen bei 2,5–3,0.

### 2. Smart-Contract-Fehler

DeFi-Protokolle sind Software. Software hat Fehler. Wenn ein Hacker eine Sicherheitslücke im Smart Contract von Aave oder Compound findet – können alle Einlagen der Nutzer gestohlen werden.

> Beispiel: der Cream-Finance-Hack (2021) – 130 Millionen $. Selbst große, geprüfte Protokolle sind nicht immun.

### 3. Oracle-Probleme

Orakel sind Dienste, die Preisdaten an Smart Contracts liefern (z. B. Chainlink). Wenn ein Oracle einen falschen Preis meldet – kann es versehentlich zur Liquidation kommen.

> 2022 gab es einen Vorfall mit dem Mango-Markets-Protokoll, bei dem Manipulationen am Oracle es Angreifern ermöglichten, 114 Millionen $ aus dem Protokoll abzuziehen.

### 4. Unfähigkeit, den Kredit zurückzuzahlen

Wenn du den Zugang zu deiner Wallet verlierst oder einfach nicht genug Geld hast, um zurückzuzahlen – werden deine Sicherheiten liquidiert. Niemand kann dir helfen, und es gibt keine Bank, die deinen Zugang wiederherstellt.

### 5. „Schrott"-Sicherheiten

Manche Protokolle erlauben es, obskure [Token](/de/glossary/#token) mit geringer [Liquidität](/de/glossary/#liquidity) als Sicherheit zu hinterlegen. Ein starker Kursverfall bei so einem Asset kann deine gesamte Position innerhalb von Minuten liquidieren.

> Verwende nur zuverlässige Assets mit hoher Liquidität (ETH, WBTC, USDC, DAI).

---

## Wann ein DeFi-Darlehen wirklich sinnvoll ist

Ein DeFi-Darlehen ist nicht dafür da, ein Auto oder ein Haus zu kaufen. Es ist ein Werkzeug für:

- **[Liquidität](/de/glossary/#liquidity) zu bekommen**, ohne deine Assets zu verkaufen (du willst ETH nicht verkaufen, brauchst aber USDC);
- **Arbitrage und Trading** (günstig leihen, in einen hochverzinslichen Pool investieren);
- **Hebelwirkung** (deine Position vergrößern, ohne deine Bestände zu verkaufen);
- **Flash Loans** (komplexe Strategien, die in einer einzigen Transaktion ausgeführt werden).

> Wenn du eine Hypothek oder einen Privatkredit brauchst – hilft dir DeFi nicht. Aber wenn du ETH hast und dagegen USDC leihen willst, ohne Kapitalertragsteuer zu zahlen – ist es die perfekte Lösung.

---

## Zusammenfassung

DeFi-Darlehen sind eine Revolution im Finanzwesen:

| Vorteile                               | Nachteile                                    |
|----------------------------------------|----------------------------------------------|
| Sofortige Genehmigung                  | Liquidationsrisiko bei Marktcrash            |
| Keine Bonitätsprüfung nötig            | Risiko von Smart-Contract-Fehlern            |
| Von überall auf der Welt zugänglich    | Erfordert aktive Überwachung der Position    |
| Transparenz (alles auf der [Blockchain](/de/glossary/#blockchain)) | Volatilität von Kryptowährungen              |
| Oft niedrigere Zinsen als bei Banken   | Verlust der Sicherheiten bei Liquidation     |

> Ein DeFi-Darlehen ist kein free money. Es ist ein Werkzeug, das dir Freiheit gibt – aber auch Verantwortung verlangt.

Wenn du es ausprobieren willst:

1. Fang klein an – 50–100 $;
2. Nutze ein bewährtes Protokoll (Aave, Compound);
3. Halte deinen Health Factor über 2,0;
4. Bleib wachsam – beobachte den Markt.

---

## FAQ

### Kann ich ein DeFi-Darlehen ohne Sicherheiten bekommen?

Im Allgemeinen nein. DeFi-Darlehen erfordern eine Überbesicherung. Die Ausnahme sind **Flash Loans** (Sofortkredite), die aber in derselben Transaktion zurückgezahlt werden müssen. Für den durchschnittlichen Nutzer sind Flash Loans nicht sehr praktisch.

### Wie hoch sind die Zinsen bei DeFi-Darlehen?

Das hängt von Angebot und Nachfrage ab. Auf Aave liegen die USDC-Zinsen bei 2–10 % p.a. In Zeiten hoher Nachfrage – bis zu 20–30 %.

### Was passiert, wenn ich den Kredit nicht zurückzahle?

Niemand wird dich anrufen oder bedrohen. Der Smart Contract liquidiert einfach deine Sicherheiten, deckt die Schulden und schickt dir den Restbetrag auf deine Wallet zurück. Allerdings verlierst du die Liquidationsstrafe (meist 5–15 %).

### Woran erkenne ich, dass meine Position kurz vor der Liquidation steht?

Sowohl Aave als auch Compound zeigen einen **Health Factor** an. Solange er über 1 liegt – ist deine Position sicher. Sobald er in Richtung 1 fällt – solltest du weitere Sicherheiten einzahlen oder einen Teil der Schulden zurückzahlen.

### Welche Coins kann ich als Sicherheit verwenden?

ETH, WBTC, USDC, DAI, MATIC, LINK und viele andere. Je liquider der Vermögenswert, desto höher der LTV (desto mehr kannst du dir dagegen leihen).

### Muss ich auf ein DeFi-Darlehen Steuern zahlen?

In den meisten Ländern – nein, denn ein Darlehen gilt nicht als Einkommen. Wenn deine Sicherheiten jedoch liquidiert werden, könnte das als steuerpflichtiger Vorgang gewertet werden (Verkauf des Vermögenswerts). Frag am besten einen lokalen Steuerberater.
