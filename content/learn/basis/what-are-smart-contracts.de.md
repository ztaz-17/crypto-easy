---
weight: 155
title: "Smart Contracts: Was sie sind und wie sie funktionieren"
description: "Smart Contracts einfach erklärt: Was sind intelligente Verträge, wo werden sie eingesetzt, wie funktionieren sie auf Ethereum und welche Risiken gibt es"
category: "basis"
translationKey: "what-are-smart-contracts"
slug: "was-sind-smart-contracts"
keywords:
  - Smart Contracts
  - intelligente Verträge
  - Ethereum
  - DeFi
  - dApps
  - dezentrale Anwendungen
  - Blockchain-Programmierung
  - Solidity
  - Krypto für Anfänger
---

## Was ist ein Smart Contract?

Ein Smart Contract ist ein Programm, das auf der Blockchain lebt und **automatisch** funktioniert — ohne menschliches Eingreifen. Du stellst die Regeln auf, und sie werden ohne Gerichte, Anwälte oder Mittelsmänner ausgeführt.

Stell dir einen Getränkeautomaten vor. Du wirfst eine Münze ein, drückst einen Knopf — bekommst ein Getränk. Niemand prüft deinen Ausweis, niemand unterschreibt einen Vertrag. Der Automat führt einfach sein Programm aus.

Ein Smart Contract funktioniert genauso — aber anstelle von Getränken verwaltet er Geld, Token und digitale Vermögenswerte.

> **Kurz gesagt:** Ein normaler Vertrag = Papier + Unterschrift + Gericht.  
> Ein Smart Contract = Code + Blockchain + automatische Ausführung.

## Wie ein Smart Contract funktioniert — ein einfaches Beispiel

Angenommen, du wettest mit einem Freund um $100, dass es morgen regnet.

**Die übliche Methode:**  
Ihr vereinbart es mündlich. Morgen verliert jemand, «vergisst» aber zu zahlen. Du gehst vor Gericht — das dauert Monate. Am Ende gibst du mehr für Anwälte aus, als du gewonnen hast.

**Mit einem Smart Contract:**  
1. Ihr schickt beide $100 an die Adresse des Smart Contracts.
2. Morgen überprüft der Vertrag die Wetterdaten (über einen **Orakel** — einen Mechanismus, der reale Daten in die Blockchain bringt).
3. Wenn es geregnet hat — sendet der Vertrag alle $200 an denjenigen, der auf Regen gewettet hat. Wenn nicht — an den anderen.
4. Niemand kann seine Meinung ändern oder die Zahlung verweigern. Der Code wird automatisch ausgeführt.

Das ist ein vereinfachtes Beispiel, aber die Idee ist dieselbe: **Smart Contracts ersetzen Vertrauen durch Code**.

## Wo werden Smart Contracts eingesetzt?

Smart Contracts sind das Rückgrat der gesamten Krypto-Industrie über einfache Überweisungen hinaus. Hier werden sie tatsächlich genutzt:

### DeFi (Dezentrale Finanzen)

Die häufigste Anwendung. DeFi-Protokolle sind Sammlungen von Smart Contracts, die Banken ersetzen:

- **Währungstausch** — du tauschst USDT gegen ETH auf Uniswap ohne Mittelsmann. Der Vertrag findet den Kurs und führt den Handel aus.
- **Kredite** — du schickst ETH als Sicherheit, der Vertrag leiht dir USDC. Fällt die Sicherheit im Preis — verkauft der Vertrag sie automatisch (Liquidation).
- **Yield Farming** — du sperrst Token in einem Liquiditätspool, der Vertrag berechnet jede Sekunde Zinsen.

Im traditionellen Finanzwesen kümmern sich Menschen darum: Manager, Kassierer, Anwälte. In DeFi — Smart Contracts.

### NFTs (Non-Fungible Token)

Jedes NFT ist ein Eintrag in einem Smart Contract. Wenn du ein NFT kaufst, führt der Vertrag Folgendes aus:
1. Prüft, ob du genug Geld hast
2. Überweist die Zahlung an den Verkäufer
3. Trägt dich als neuen Besitzer ein
4. Zahlt Lizenzgebühren an den Ersteller (einen Prozentsatz des Weiterverkaufs)

### DAOs (Dezentrale Autonome Organisationen)

Smart Contracts verwalten die Schatzkammer der Organisation ohne CEO. Mitglieder stimmen mit Token ab, und der Vertrag führt die Entscheidung automatisch aus:

- «Für die Zuweisung von 10.000 USDT für Marketing gestimmt» → der Vertrag sendet die Gelder
- «Für die Änderung des Zinssatzes gestimmt» → der Vertrag passt die Protokollparameter an

### Token

Wenn du einen neuen Token erstellst (USDT, UNI, SHIB oder einen beliebigen anderen), ist das keine Magie — es ist ein Smart Contract, der dem ERC-20-Standard (auf Ethereum) oder BEP-20 (auf BSC) folgt. Der Vertrag speichert die Guthaben aller Inhaber und autorisiert Überweisungen.

> Fakt: Der beliebteste Smart Contract ist USDT Tether. Er verarbeitet täglich Milliarden von Dollar.

## Smart Contracts auf Ethereum

Ethereum war die erste Plattform, die Smart Contracts massentauglich machte. Bitcoin erlaubt nur das Senden von Coins. Ethereum erlaubt das Programmieren beliebiger Regeln.

**Ethereums Kernidee:** nicht nur «Alice hat 5 ETH an Bob geschickt», sondern «WENN die Bedingung erfüllt ist, DANN führe die Aktion aus».

Ethereum Smart Contracts werden in **Solidity** geschrieben, einer Sprache ähnlich wie JavaScript, die aber auf der Blockchain läuft. Jeder kann den Code eines Vertrags lesen — alle Smart Contracts sind standardmäßig Open Source.

### Gas: Warum jede Operation Geld kostet

Jede Smart-Contract-Aktion erfordert Rechenressourcen. Alle Computer im Netzwerk (Knoten) müssen den Code ausführen und das Ergebnis überprüfen. Du bezahlst dafür mit **Gas** — einer Gebühr in ETH.

Eine komplexe Operation (wie ein Swap auf Uniswap) kostet mehr als eine einfache (ETH senden). Je mehr Leute das Netzwerk nutzen, desto höher ist das Gas.

## Vorteile von Smart Contracts

**Transparenz** — der Code des Vertrags ist für alle sichtbar. Du kannst überprüfen, was mit deinem Geld passiert, bevor du es sendest.

**Unveränderlichkeit** — einmal auf der Blockchain veröffentlicht, kann der Vertrag nicht mehr geändert werden. Niemand kann im Nachhinein Regeln hinzufügen.

**Keine Mittelsmänner** — keine Banken, Anwälte oder Notare nötig. Der Vertrag führt die Bedingungen selbst aus.

**24/7 Verfügbarkeit** — der Vertrag läuft rund um die Uhr, ohne Wochenenden oder Pausen. Niemand kann sagen «kommen Sie morgen wieder» oder «der Sachbearbeiter ist in der Mittagspause».

**Automatisierung** — Zahlungen, Zinsansammlungen, Umsatzverteilung — alles kann automatisch ablaufen.

## Risiken von Smart Contracts

Smart Contracts sind nicht perfekt. Hier sind die Hauptrisiken:

### Fehler im Code

Menschen schreiben Code — Menschen machen Fehler. Wenn ein Vertrag einen Fehler hat, kann ein Hacker ihn ausnutzen.

**Beispiel:** der DAO-Hack von 2016. Ein Hacker fand eine Schwachstelle im Code und zog 3,6 Millionen ETH (~$50 Millionen zu der Zeit) ab. Dies zwang Ethereum zu einem Hard Fork — der Aufspaltung in Ethereum und Ethereum Classic.

Es gibt Tausende solcher Fälle. Jeden Monat werden Protokolle für Millionen von Dollar gehackt — fast immer aufgrund von Fehlern in Smart Contracts.

### Unveränderlichkeit — ein zweischneidiges Schwert

Wenn du einen Fehler im Vertrag gemacht hast, kannst du nicht einfach «bitten, es zu reparieren». Der Vertrag lebt sein eigenes Leben. Deshalb durchlaufen Verträge vor dem Start **Audits** — Code-Überprüfungen durch Sicherheitsexperten.

### Orakel — das schwache Glied

Ein Smart Contract kann nicht selbstständig den Bitcoin-Kurs oder das Wetter überprüfen. Diese Daten kommen von **Orakeln** — externen Diensten. Wenn ein Orakel falsche Daten sendet (oder gehackt wird), führt der Vertrag Bedingungen auf der Grundlage falscher Informationen aus.

### Frontrunning

Wenn du eine Smart-Contract-Transaktion sendest, gelangt sie in den Mempool (die Warteschlange unbestätigter Transaktionen). Bots können sie erkennen, mehr Gas zahlen und ihre eigene Transaktion vor deiner ausführen. Das nennt man Frontrunning — und es ist legal.

## So überprüfst du einen Smart Contract vor der Nutzung

1. **Suche nach einem Audit** — seriöse Protokolle veröffentlichen Audits von Firmen wie Trail of Bits, OpenZeppelin oder Certik. Kein Audit? Schicke kein Geld.
2. **Überprüfe das Alter des Vertrags** — wenn ein Vertrag einen Monat alt ist, Millionen an TVL hat und kein Audit vorliegt — ist das eine rote Flagge.
3. **Lies den Code** — wenn du kannst, überprüfe den Code auf Etherscan. Wenn nicht, bleib bei Projekten, denen die Community vertraut.
4. **Überprüfe Berechtigungen** — wenn du eine Smart-Contract-Transaktion signierst, gibst du ihm oft die Erlaubnis, deine Token auszugeben. Nutze [Token-Berechtigungen](/de/security/token-berechtigungen-erklaert/) — widerrufe Berechtigungen von Verträgen, die du nicht mehr verwendest.

## Die Zukunft der Smart Contracts

Smart Contracts sind nicht nur ein Krypto-Gimmick. Sie sind eine neue Form digitaler Vereinbarungen, die nach und nach in die reale Welt einzieht:

- **Versicherungen** — ein Vertrag zahlt automatisch Entschädigung bei Flugverspätung.
- **Immobilien** — Smart Contracts können Immobilienkäufe ohne Notar abwickeln.
- **Lizenzgebühren** — Musiker erhalten automatisch Zahlungen, jedes Mal wenn ihr Song abgespielt wird.
- **Wahlen** — Verträge können eine transparente Stimmenauszählung ohne Betrug ermöglichen.

Die meisten dieser Anwendungen sind noch experimentell. Aber die Technologie entwickelt sich weiter, und in 5-10 Jahren könnten Smart Contracts so alltäglich sein wie E-Mail.

## Wichtige Erkenntnisse

- Ein Smart Contract ist ein Programm auf der Blockchain, das ohne menschliches Eingreifen läuft
- Sie betreiben DeFi, NFTs, DAOs und Token
- Ethereum ist die Hauptplattform für Smart Contracts
- Das größte Risiko sind Fehler im Code und Sicherheitslücken
- Überprüfe immer Audits und Berechtigungen, bevor du eine dApp (dezentrale Anwendung) nutzt
