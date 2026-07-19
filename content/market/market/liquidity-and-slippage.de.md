---
weight: 20
title: "Was ist Liquidität und warum sie für den Preis wichtig ist"
description: "Was Liquidität im Krypto-Bereich bedeutet, Markttiefe, Slippage und warum niedrige Liquidität gefährlich ist — einfach erklärt"
category: "market"
translationKey: "liquidity-and-slippage"
slug: "liquiditat-und-slippage"
keywords:
  - Liquidität
  - Markttiefe
  - Slippage
  - Orderbuch
  - Risiko niedriger Liquidität
---

## Was ist Liquidität und warum sie für den Preis wichtig ist

---

Kommt dir bekannt vor?

Du willst eine Coin auf einer Börse verkaufen. Du setzt eine Verkaufsorder zum aktuellen Preis — 100 $. Du wartest eine Minute. Zwei Minuten. Zehn Minuten. Niemand kauft.

Du senkst den Preis auf 99 $. Dann auf 98 $. Erst bei 95 $ findet sich endlich jemand, der deine Coin nimmt.

Oder andersrum: Du willst einen Altcoin kaufen. Siehst den Preis bei 10 $, drückst auf „Kaufen" — und die Order wird zu 12 $ ausgeführt. Wie kann das sein?

Alles hängt mit **[Liquidität](/de/glossary/#liquidity)** zusammen.

In diesem Artikel erfährst du:
> - was Liquidität in einfachen Worten bedeutet;
> - wie ein Orderbuch funktioniert;
> - was Slippage ist;
> - und warum niedrige Liquidität gefährlich ist.

---

## Liquidität: die Fähigkeit, schnell zu kaufen oder zu verkaufen, ohne beim Preis einzubußen

### Was das ist

**[Liquidität](/de/glossary/#liquidity)** ist ein Maß dafür, wie leicht du einen Vermögenswert gegen Geld (oder einen anderen Vermögenswert) tauschen kannst, ohne den Preis wesentlich zu beeinflussen.

> **Beispiel aus dem echten Leben:**
> Eine Wohnung zum Marktpreis innerhalb eines Monats zu verkaufen, ist schwierig. Einen Käufer finden, verhandeln, Papierkram erledigen. Das ist ein ** Vermögenswert mit geringer Liquidität**.
>
> Dollar an einem Wechselstuben-Schalter zu verkaufen — 5 Sekunden. Das ist ein **Vermögenswert mit hoher Liquidität**.

Im Krypto-Bereich ist es genauso:

- **Bitcoin auf Binance** — hohe [Liquidität](/de/glossary/#liquidity). Du kannst in Sekunden 50.000 $ verkaufen, und der Preis bewegt sich kaum.
- **Ein obskurer [Token](/de/glossary/#token) auf einer kleinen Börse** — niedrige Liquidität. Schon eine Verkaufsorder über 1.000 $ kann den Preis um 10–20 % verschieben.

### Warum das wichtig ist

Liquidität bestimmt:
- wie schnell du eine Position verlassen kannst;
- zu welchem Preis deine Order ausgeführt wird;
- wie berechenbar die Kursbewegungen sind.

---

## Markttiefe: das Orderbuch

### Wie ein Orderbuch funktioniert

Jede Börse ist im Grunde nur ein Ort, an dem Käufer und Verkäufer aufeinandertreffen. Alle ihre Orders werden in einem **Orderbuch** gesammelt.

Es sieht so aus:

```
VERKÄUFER (Asks)
────────────────
101,00 $ — 500 Coins
100,80 $ — 200 Coins
100,50 $ — 100 Coins
────────────────
AKTUELLER PREIS: 100,00 $
────────────────
KÄUFER (Bids)
────────────────
99,80 $  — 150 Coins
99,50 $  — 300 Coins
99,00 $  — 600 Coins
```

- **Bids** — Kauforders (wie viel die Leute kaufen wollen und zu welchem Preis).
- **Asks** — Verkaufsorders.
- Die Differenz zwischen dem besten Bid und dem besten Ask ist der **Spread**.

### Was Markttiefe ist

**Markttiefe** ist das Volumen an Orders, das auf den verschiedenen Preisstufen liegt.

Wenn hinter jeder Stufe Millionen von Dollar stehen — dann ist der Markt tief. Wenn nur 10 Coins einen Dollar über dem aktuellen Preis liegen — dann ist der Markt flach. Jede Kauforder bewegt sofort den Preis.

> **Einfache Metapher:**
> - Ein tiefer Markt ist wie ein Schwimmbecken. Du springst hinein — der Wasserspiegel ändert sich kaum.
> - Ein flacher Markt ist wie eine Pfütze. Ein Schritt und das Wasser spritzt überall hin.

### Spread — ein Indikator für Liquidität

**Spread** ist die Differenz zwischen dem besten Kaufkurs (Bid) und dem besten Verkaufskurs (Ask).

- Enger Spread (0,01 $) → hohe Liquidität.
- Weiter Spread (1 $+) → niedrige Liquidität.

Wenn du an einer Börse einen Spread von 5–10 % siehst — ist das ein Warnsignal. Diese Coin zu kaufen, ist riskant.

---

## Slippage: bei 100 gekauft, zu 105 ausgeführt

### Was Slippage ist

**[Slippage](/de/glossary/#slippage)** ist die Differenz zwischen dem Preis, den du erwartet hast, und dem Preis, zu dem deine Order tatsächlich ausgeführt wurde.

Das passiert, weil nicht genug Liquidität auf der Stufe vorhanden ist, die du haben wolltest.

### Wie es funktioniert

Du willst eine Coin zu 100 $ kaufen. Du setzt eine **Marktorder** (kaufe sofort zum besten verfügbaren Preis).

Das System prüft das Orderbuch:
- bei 100,00 $ — 5 Coins zum Verkauf;
- bei 100,50 $ — weitere 5 Coins;
- bei 101,00 $ — weitere 5 Coins;
- bei 102,00 $ — weitere 10 Coins ...

Wenn du 25 Coins kaufen willst, frisst sich deine Order durch mehrere Stufen hindurch. Dein durchschnittlicher Ausführungspreis liegt nicht bei 100 $, sondern etwa bei 101,20 $.

Du wolltest zu 100 $ kaufen — gekauft hast du zu ~101 $. Das ist **[Slippage](/de/glossary/#slippage)**.

> **Je größer deine Order im Verhältnis zur Markttiefe, desto mehr Slippage bekommst du.**

### Limit-Orders schützen vor Slippage

Du kannst eine **Limit-Order** verwenden — du legst den Preis fest, zu dem du kaufen oder verkaufen willst, und wartest, bis ein Gegenüber am Markt auftaucht.

Aber es gibt ein anderes Risiko:
- bei niedriger Liquidität kann es Stunden oder Tage dauern;
- der Preis kann sich gegen dich bewegen, während du wartest.

---

## Warum niedrige Liquidität gefährlich ist

### 1. Starke Kurssprünge

Bei niedriger Liquidität kann eine einzige große Order den Preis in Sekunden um 20–30 % bewegen.

Beispiel: Auf einer kleinen Börse liegen Verkaufsorders für insgesamt nur 100 Coins bis zu einem Preis von 50 $. Jemand beschließt, für 10.000 $ zu kaufen. Seine Order frisst sich durch alle Verkaufsorders bis zu 70 $, und der Preis schießt sofort nach oben.

Das ist **[Slippage](/de/glossary/#slippage) in Reinform**. Und es funktioniert in beide Richtungen:

- du hast zu 50 $ gekauft — der Preis sprang auf 70 $;
- du willst verkaufen — der nächste Käufer steht bei 40 $.

### 2. In einer Position feststecken

Das beängstigendste Szenario bei niedriger Liquidität:

Der Markt fängt an zu fallen. Du willst verkaufen, aber im Orderbuch gibt es keinen einzigen großen Käufer. Deine Order bleibt minutenlang stehen. Der Preis fällt weiter. Du senkst deinen Preis. Niemand nimmt ihn.

Bis du einen Käufer findest, ist der Preis schon um 40 % gefallen.

> **Wenn der Markt in Panik gerät, verdampft die Liquidität zuerst.**

Alle wollen verkaufen — niemand will kaufen. Der Spread weitet sich auf lächerliche Werte aus. Und wer Coins mit niedriger Liquidität hält, kommt da nicht mehr raus – selbst mit großen Verlusten.

### 3. Kursmanipulation

Bei Coins mit niedriger Liquidität lässt sich der Preis leicht manipulieren. Ein großer Spieler (Wal) kann:

- den Preis mit einer einzigen Order um 50 % nach oben treiben;
- warten, bis Neueinsteiger aus [FOMO](/de/glossary/#fomo) einsteigen;
- alles zum hohen Preis verkaufen — und der Preis stürzt wieder ab.

Das ist das klassische **Pump & Dump**-Schema, und es funktioniert nur bei Coins mit niedriger Liquidität.

### 4. Unvorhersehbare Gebühren

Auf manchen dezentralen Börsen können die Transaktionsgebühren bei niedriger Liquidität höher sein als der Trade selbst. Oder der Trade scheitert einfach — die Pool-Tiefe reicht nicht aus.

---

## Wie du die Liquidität vor dem Kauf prüfst

### 1. Schau auf den Spread

Wenn die Differenz zwischen Kauf- und Verkaufskurs mehr als 1–2 % beträgt, ist das ein Grund, nochmal nachzudenken.

### 2. Prüfe das Handelsvolumen

Auf CoinMarketCap oder CoinGecko schaust du dir das **24-Stunden-Handelsvolumen** an. Liegt es bei einem Altcoin unter 1 Million $ — ist die Liquidität niedrig.

### 3. Prüfe das Orderbuch

Öffne das Orderbuch auf der Börse. Wie viele Coins liegen auf den Stufen nahe dem aktuellen Preis? Wenn auf jeder Stufe nur 10–20 Coins stehen — sei vorsichtig.

### 4. Vergleich mit Bitcoin

Zum Vergleich: Bitcoins tägliches Handelsvolumen liegt bei 10–30 Milliarden $. Der Spread beträgt Bruchteile eines Cents. Jede Coin mit weniger als 10 Millionen $ täglichem Volumen gilt als liquiditätsschwach.

---

## Liquiditätsstufen auf einen Blick

| Stufe | Spread | 24h-Volumen | Auswirkung einer 10.000-$-Order | Beispiel |
|---|---|---|---|---|
| Sehr hoch | < 0,01 % | > 1 Mrd. $ | Vernachlässigbar | BTC, ETH auf Binance |
| Hoch | 0,01–0,1 % | 100 Mio.–1 Mrd. $ | Minimal | Top-10-Altcoins |
| Mittel | 0,1–0,5 % | 10–100 Mio. $ | Spürbar | Mid-Cap-Altcoins |
| Niedrig | 0,5–2 % | 1–10 Mio. $ | Stark | Kleine Altcoins |
| Sehr niedrig | > 2 % | < 1 Mio. $ | Kritisch | Shitcoins, neue [Tokens](/de/glossary/#token) |

---

## Fazit

Liquidität ist das, was einen echten Markt von einem Casino unterscheidet.

Wenn du an einer Börse mit hoher Liquidität handelst:
- steigst du zu fairen Preisen ein und aus;
- ist der Spread minimal;
- gibt es keine wilden Ausschläge durch eine einzelne Order;
- kannst du deine Trades planen, ohne Überraschungen.

Wenn die Liquidität niedrig ist:
- ist jede Order eine Lotterie;
- frisst Slippage deine Gewinne auf;
- kommst du im entscheidenden Moment nicht raus.

> **Einfache Regel: Handle niemals Coins, deren Liquidität geringer ist als der Betrag, mit dem du arbeitest.**

Und schau immer ins Orderbuch, bevor du auf „Kaufen" drückst. Ein Blick auf den Spread und die Markttiefe kann dich davor bewahren, Geld zu verlieren.

---

## FAQ

### Was ist Liquidität in einfachen Worten?

Es ist die Fähigkeit, einen Vermögenswert schnell zu einem Preis zu kaufen oder zu verkaufen, der nahe am Marktkurs liegt — ohne große Verluste.

### Wie unterscheidet sich Liquidität von Volatilität?

Liquidität hat mit Markttiefe und Ausführungsgeschwindigkeit zu tun. Volatilität gibt an, wie stark der Preis schwankt. Beide hängen oft zusammen: niedrige Liquidität führt zu hoher Volatilität.

### Welcher Spread gilt als normal?

Bei Bitcoin und den Top-Coins — Bruchteile eines Prozents. Bei Altcoins — bis zu 0,5 % ist akzeptabel. Alles über 1–2 % ist die Gefahrenzone.

### Warum ist der Slippage auf DEXs (dezentralen Börsen) höher?

DEXs haben kein zentrales Orderbuch. Der Preis wird durch die Größe des Liquiditätspools bestimmt. Je kleiner der Pool, desto mehr Slippage bei jedem Trade.

### Kann man auch dann Geld verlieren, wenn der Preis steigt?

Ja. Wenn du deine Coin nicht zum aktuellen Kurs verkaufen kannst, weil es keine Käufer gibt — kannst du den Gewinn nicht realisieren. Der Preis steht vielleicht im Chart, aber du kannst nicht zu diesem Preis verkaufen.
