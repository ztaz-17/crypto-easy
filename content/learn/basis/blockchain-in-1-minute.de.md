---
weight: 120
title: "Blockchain in 1 Minute erklärt (Die einfachste Erklärung)"
description: "Blockchain für Anfänger: Was ist ein gemeinsames Hauptbuch, warum Einträge nicht überschrieben werden können und wie es funktioniert — die einfachste Erklärung"
category: "basis"
translationKey: "blockchain-in-1-minute"
slug: "blockchain-in-1-minute"
keywords:
  - Blockchain erklärt
  - verteiltes Hauptbuch
  - wie Blockchain funktioniert
  - Blockchain für Anfänger
---

## Blockchain in 1 Minute erklärt (die einfachste Erklärung)

---

Stell dir vor, du und deine **10.000 besten Freunde** führen alle gleichzeitig dasselbe Heft.

In diesem Heft sind alle Geldüberweisungen zwischen euch festgehalten. Immer wenn jemand einem anderen 10 Euro schickt, schreiben alle 10.000 Personen es gleichzeitig in ihre Kopien.

Und jetzt das Beste:

> **Niemand kann die Einträge fälschen!**

Selbst wenn jemand eine Million Euro dazu dichten wollte — müsste er alle 10.000 Kopien gleichzeitig ändern. Alle anderen würden den Betrug sofort bemerken und die unehrliche Version ablehnen.

Das ist **Blockchain**.

Nur statt einem "Heft" — ein digitales Hauptbuch. Statt "Freunden" — Computer auf der ganzen Welt. Und statt "handschriftlichen Notizen" — mathematische Formeln, die man nicht täuschen kann.

---

## Das gemeinsame Hauptbuch

### Was ist ein Hauptbuch?

Ein **Hauptbuch (Ledger)** ist einfach ein Journal, das festhält, wer wem wie viel schuldet.

Früher führte jede Bank ihr **eigenes** Hauptbuch. Wenn du Geld von Bank A zu Bank B überwiesen hast, verglichen die beiden Banken ihre Aufzeichnungen und einigten sich, welcher Saldo stieg und welcher fiel.

### Was ist anders bei Blockchain?

[Blockchain](/de/glossary/#blockchain) ist ein **gemeinsames Hauptbuch**, das bei allen Netzwerkteilnehmern gleichzeitig existiert.

Besonderheiten:

- jeder Teilnehmer speichert eine **vollständige Kopie** des Hauptbuchs;
- alle Kopien synchronisieren sich automatisch;
- es gibt kein Zentrum — keine Bank, die einen Eintrag "korrigieren" könnte.

Einfacher Vergleich:

> **Ein Klassenbuch, das für jeden Schüler dupliziert wird.**

In einer normalen Schule hat der Lehrer das Klassenbuch. Wenn der Lehrer eine Note ändern will — tut er es, und niemand merkt es. Bei Blockchain haben alle das Buch. Jede Änderung fällt sofort auf.

---

## Warum man Einträge nicht überschreiben kann

### Wie ein Block funktioniert

Blockchain besteht aus Blöcken. Jeder Block ist wie eine Seite im gemeinsamen Heft. Er enthält:

- **mehrere Transaktionen** (wer hat wem was geschickt);
- **einen Zeitstempel** (wann der Block erstellt wurde);
- **den Hash des vorherigen Blocks** (einen digitalen "Fingerabdruck" der letzten Seite).

### Was ist ein Hash und warum ist er wichtig?

Ein **Hash** ist eine kurze Zeichenkette, die aus beliebigen Daten erzeugt wird. Wie ein Fingerabdruck: Jeder Datensatz hat einen eindeutigen Hash. Ändere auch nur einen Buchstaben — und der Hash wird völlig anders.

So sieht das aus:

> Daten: "Anna hat 10 € an Ben überwiesen" → Hash: `d5f1f8a8c5b2e8f7d9c4a1b3e6f2c8d9`
>
> Daten: "Anna hat 20 € an Ben überwiesen" → Hash: `a3e7b9f2d1c5e8a4b7f6d2e9c1a5f8b3`

Ändere nur eine Ziffer — der Hash ändert sich komplett.

### Die Kette der Blöcke

Jeder Block enthält den Hash des **vorherigen** Blocks. Das ergibt eine Kette:

```
[Block 1] —Hash—> [Block 2] —Hash—> [Block 3] —Hash—> [Block 4]
```

Wenn jemand versucht, Daten in Block 2 zu ändern, ändert sich der Hash dieses Blocks. Block 3, der den alten Hash referenziert, wird ungültig. Und Block 4 auch.

Um **einen** Block zu ändern, müsstest du **alle nachfolgenden Blöcke** umschreiben. Und dafür braucht man mehr Rechenleistung als 50% des gesamten Netzwerks.

Einfacher Vergleich:

> **Die Seiten eines Buches sind zusammengeheftet und gebunden — du kannst keine herausreißen und eine andere einfügen, ohne den Einband zu beschädigen.**

---

## Warum es funktioniert

### Konsens — die Einigung der Teilnehmer

Die Netzwerkteilnehmer vertrauen einander nicht. Stattdessen vertrauen sie der Mathematik. Damit ein neuer Eintrag (Block) akzeptiert wird, müssen sich die Teilnehmer **einigen**, dass er korrekt ist. Dieser Prozess heißt **Konsens**.

Es gibt zwei Hauptmethoden, sich zu einigen:

- **[Proof of Work](/de/glossary/#proof-of-work) (PoW)** — von Bitcoin verwendet. Teilnehmer lösen komplexe Mathematikaufgaben, um einen Block zu bestätigen. Wer zuerst löst, darf die "Seite schreiben".
- **[Proof of Stake](/de/glossary/#proof-of-stake) (PoS)** — von Ethereum verwendet. Teilnehmer "sperren" ihre Coins als Sicherheit und bestätigen Blöcke proportional zu ihrem Anteil.

Beide Mechanismen funktionieren gleich gut: **Niemand kann falsche Informationen aufzeichnen**.

### Dezentralisierung — kein einzelner Angriffspunkt

In einem normalen System gibt es einen Server, den man abschalten kann. Bei Blockchain — Tausende von Computern weltweit. Um eine Blockchain zu stoppen, müsstest du **alle** diese Computer gleichzeitig abschalten.

Das Netzwerk läuft, solange auch nur ein Teilnehmer am Leben ist.

> **Bitcoin läuft seit 2009 und wurde noch nie gehackt.**

In über 16 Jahren konnte niemand Einträge fälschen oder Coins durch "Netzwerk-Hacking" stehlen. Alle Crypto-Vorfälle betrafen Börsen und Wallets — wo Menschen **selbst** den Zugriff auf ihre Schlüssel verloren. Die Blockchain selbst blieb unberührt.

---

## Was Blockchain NICHT tut

Blockchain ist keine Wunderwaffe. Es ist wichtig, ihre Grenzen zu verstehen:

### Es beschleunigt keine Transaktionen

Bitcoin verarbeitet etwa **7 Transaktionen pro Sekunde** (tps). Visa — etwa **24.000 tps**. Für alltägliche Einkäufe ist Blockchain langsamer.

### Es macht nichts kostenlos

Jede Transaktion erfordert eine **Netzwerkgebühr** — gezahlt an die Teilnehmer, die Blöcke bestätigen. In Spitzenzeiten können die Gebühren hoch sein.

### Es speichert keine eigentlichen Daten

Blockchain speichert keine Dateien oder Dokumente selbst — nur **Hashes** — digitale Fingerabdrücke der Daten. Wenn jemand ein Dokument hochgeladen hat, beweist Blockchain nur, dass es zu einem bestimmten Zeitpunkt existiert hat.

### Aber es löst das Hauptproblem

> **Vertrauen ohne Mittelsmann.**

Zum ersten Mal in der Geschichte können zwei Fremde auf verschiedenen Seiten der Welt Werte austauschen, ohne einander zu vertrauen und ohne Bank, Notar oder Regierung einzuschalten. Das allein reichte aus, um die Finanzwelt zu verändern.

---

## Zusammenfassung

Blockchain ist ein gemeinsames digitales Hauptbuch, das Tausende von Menschen gleichzeitig führen. Es ist unmöglich zu fälschen, weil:

- jede Seite (Block) mit der vorherigen verknüpft ist;
- jede Änderung alle nachfolgenden Blöcke verändert;
- um einen Eintrag zu fälschen, müsste man die Geschichte auf Tausenden von Computern gleichzeitig umschreiben.

Blockchain ist nicht perfekt: Sie ist langsam, nicht kostenlos und speichert keine Daten. Aber sie löst etwas, das keine Technologie vor ihr konnte:

> **Sie ermöglicht es Fremden, einander ohne Mittelsmänner zu vertrauen.**

Das macht Blockchain zu einer echten Revolution.

---

## FAQ

### Kann ich eine Blockchain mit eigenen Augen sehen?

Ja, und es ist einfacher als du denkst. Jede Blockchain ist ein öffentliches Register. Gehe auf **[blockchain.com/explorer](https://www.blockchain.com/explorer)** oder **[etherscan.io](https://etherscan.io)** und sieh alle Bitcoin- oder Ethereum-Transaktionen in Echtzeit. Du siehst: wer wem was geschickt hat, wie viel, in welchem Block und wann. Völlig transparent.

### Wie groß ist die gesamte Bitcoin-Blockchain?

Stand April 2026 — **~735 GB**. Das ist die gesamte Blockkette seit 2009. Jeder neue Block (etwa alle 10 Minuten) fügt etwa 1-2 MB hinzu. Du kannst die vollständige Blockchain selbst herunterladen und speichern — so arbeiten "vollständige Knoten".

### Was passiert, wenn alle Netzwerkteilnehmer verschwinden?

Wenn alle verschwinden, stirbt die Blockchain. Aber das ist der Punkt: Es gibt so viele Teilnehmer (Zehntausende), dass ein gleichzeitiges Verschwinden aller praktisch unmöglich ist. Selbst wenn 99% gehen, hält das verbleibende 1% das Netzwerk am Leben.
