---
weight: 210
title: "Was passiert, wenn du Crypto sendest"
description: "Hinter den Kulissen einer Crypto-Transaktion: Erstellung, Signierung, Netzwerk-Broadcast und Bestätigung – einfach erklärt"
category: "how-it-works"
translationKey: "what-happens-when-you-send-crypto"
slug: "was-passiert-wenn-du-crypto-sendest"
keywords:
  - Crypto-Transaktion
  - Wie Crypto funktioniert
  - Blockchain-Transaktion
  - Transaktion signieren
  - Mining
  - Bestätigung
  - Broadcasting
---

## Was passiert, wenn du Crypto sendest

---

Du öffnest deine [Wallet](/de/glossary/#wallet), tippst die Empfängeradresse ein, gibst den Betrag ein – und drückst auf „Senden."

Ist das Geld jetzt weg? Noch nicht.

Auf deinem Bildschirm erscheint eine Meldung: „Transaktion gesendet. Warte auf Bestätigung …"

Und genau hier beginnt die eigentliche Action.

Was als Nächstes passiert, ist ein komplexes Zusammenspiel zwischen deiner Wallet, tausenden Computern auf der ganzen Welt und der Mathematik, die das System ehrlich hält.

> In diesem Artikel gehen wir jede Phase durch: vom Moment, in dem du auf „Senden" klickst, bis die Coins im Wallet des Empfängers landen.

Schauen wir uns an, was wirklich passiert, wenn du Crypto sendest.

---

## Phase 1: Erstellung der Transaktion

Es beginnt damit, dass deine Wallet Daten sammelt. Sie baut ein digitales „Paket" – eine Transaktion. In diesem Paket:

- **von** – deine öffentliche Adresse;
- **an** – die Adresse des Empfängers;
- **Betrag** – wie viel du sendest;
- **Gebühr** – was du dem Netzwerk für die Verarbeitung zahlst.

Die Transaktion wurde noch nicht gesendet. Es ist nur ein Entwurf – ein Datenpaket, das nur auf deinem Gerät existiert.

### Was wichtig zu wissen ist

Deine Wallet „zieht" kein Geld von einem Konto ab. Stattdessen durchsucht sie die gesamte Historie früherer Transaktionen, die jemals an deine Adresse gingen, und wählt unverbrauchte Guthaben aus.

Stell es dir vor wie mehrere Geldscheine in deiner Tasche – du suchst dir den aus, mit dem du bezahlen willst. In der Crypto-Welt sind diese „Scheine" Einträge auf der [Blockchain](/de/glossary/#blockchain).

> Mehr zu Adressen und Schlüsseln findest du im Glossar: [öffentliche Adresse](/de/glossary/#public-address), [privater Schlüssel](/de/glossary/#private-key).

---

## Phase 2: Signieren der Transaktion

Jetzt kommt der wichtigste Teil.

Deine Wallet nimmt die Transaktionsdaten und signiert sie mit deinem **[privaten Schlüssel](/de/glossary/#private-key)**. Es ist, als würdest du deinen persönlichen digitalen Stempel draufdrücken – einen, den niemand fälschen kann.

### Warum Signaturen nicht gefälscht werden können

Dein privater Schlüssel ist eine lange, zufällige Zeichenkette. Nur du kennst ihn. Das Netzwerk kennt nur deine öffentliche Adresse – eine Ableitung dieses Schlüssels.

Wenn du eine Transaktion signierst:

1. Wendet deine Wallet eine mathematische Formel auf die Transaktionsdaten und deinen Schlüssel an.
2. Das Ergebnis ist eine **digitale Signatur** – eine einzigartige Zeichenkette.
3. Jeder Netzwerkteilnehmer kann diese Signatur mit deiner öffentlichen Adresse überprüfen.
4. Aber niemand kann deinen privaten Schlüssel aus der Signatur zurückgewinnen.

> **Wichtig:** Dein privater Schlüssel wird niemals irgendwohin gesendet. Er bleibt auf deinem Gerät. Das Netzwerk überprüft die Signatur, ohne den Schlüssel selbst zu sehen.

Versucht jemand, den Betrag in einer signierten Transaktion zu ändern – wird die Signatur ungültig. Das Netzwerk lehnt sie sofort ab.

Das ist die Magie: Du beweist, dass dir die Coins gehören, ohne dein Geheimnis preiszugeben.

---

## Phase 3: Broadcasting im Netzwerk

Die Transaktion ist signiert. Jetzt muss sie ins Netzwerk gelangen.

Deine Wallet sendet die Transaktion an einen oder mehrere Netzwerkknoten – **Nodes**. Ein Node ist ein Computer, der einen vollständigen Blockchain-Client ausführt. Er speichert die gesamte Transaktionshistorie und prüft neue.

### Was ein Node prüft

Wenn ein Node deine Transaktion erhält, überprüft er:

- die Signatur ist korrekt;
- du hast genug Guthaben;
- du versuchst nicht, dieselben Coins zweimal auszugeben (Double-Spending).

Wenn alles in Ordnung ist – fügt der Node die Transaktion zum **Mempool** (kurz für Memory Pool) hinzu. Das ist der Wartebereich für unbestätigte Transaktionen.

### Der Mempool – ein Warteraum

Stell dir einen Bahnhof vor. Deine Transaktion ist ein Fahrgast, der auf einen Zug (einen [Block](/de/glossary/#block)) wartet. Es gibt viele Fahrgäste, der Zug fährt nur alle 10 Minuten ab (bei Bitcoin), und die Plätze sind begrenzt.

Wer kommt in den Zug? Diejenigen, die ein Ticket bezahlt haben – also die Gebühr. Je höher die Gebühr, desto eher wird deine Transaktion für einen Block ausgewählt.

> Ist die Gebühr zu niedrig, kann deine Transaktion Stunden oder sogar Tage warten. Der Mempool kann zu jeder Zeit zehntausende unbestätigte Transaktionen enthalten.

Nach der Überprüfung **leitet** der Node die Transaktion an seine Nachbarn weiter. Diese leiten sie an ihre Nachbarn weiter. In Sekunden verbreitet sich die Transaktion über den ganzen Globus.

---

## Phase 4: Bestätigung in einem Block

Die Transaktion ist im Mempool. Jetzt muss sie von einem **Miner** (bei Bitcoin) oder einem **Validator** (bei Ethereum und anderen PoS-Netzwerken) bestätigt werden.

### Wie Miner Transaktionen auswählen

Miner sammeln Transaktionen aus dem Mempool und packen sie in einen Block. Die Priorität hängt von der Gebühr ab – je höher die Gebühr, desto höher die Priorität.

Sobald der Block zusammengestellt ist, beginnt der Miner, ein mathematisches Rätsel ([Proof of Work](/de/glossary/#proof-of-work)) zu lösen, um den Block zu versiegeln. Dafür ist massive Rechenleistung nötig. Wer es zuerst schafft, bekommt:

- die Blockbelohnung (neu geschaffene Coins);
- alle Gebühren der enthaltenen Transaktionen.

Sobald ein Block gefunden wurde, sendet der Miner ihn an alle Nodes. Die Nodes überprüfen den Block und fügen ihn – wenn alles korrekt ist – ihrer Chain hinzu.

### Wie lange auf Bestätigung warten

Bei Bitcoin bedeutet eine Bestätigung, dass deine Transaktion in einem Block gelandet ist. Aber normalerweise wartet man auf mehrere Bestätigungen (je mehr, desto sicherer):

| Netzwerk | Blockzeit | Wie viele abwarten |
|----------|-----------|-------------------|
| Bitcoin | ~10 Minuten | 3 Blöcke (~30 Min.) |
| Ethereum | ~12 Sekunden | 12–30 Blöcke (~2–6 Min.) |
| Solana | ~400 ms | 1 Block (sofort) |

> Warum nicht nur eine Bestätigung? Weil ein Miner theoretisch einen alternativen Block (einen Fork) erzeugen könnte. Je mehr Blöcke nach deinem kommen, desto schwerer ist es, die Transaktion rückgängig zu machen. Nach 6 Bestätigungen bei Bitcoin ist eine Umkehrung praktisch unmöglich.

---

## Zusammenfassung: Die Phasen einer Transaktion

Hier ist der komplette Weg einer Transaktion vom Klick auf „Senden" bis zur endgültigen Bestätigung:

| Phase | Was passiert | Wer ist beteiligt | Zeit |
|-------|-------------|-------------------|------|
| 1. Erstellung | Wallet bereitet die Daten vor: von, an, Betrag | Deine Wallet | Sofort |
| 2. Signierung | Transaktion wird mit deinem privaten Schlüssel signiert | Deine Wallet | Sofort |
| 3. Broadcasting | Transaktion wird an Nodes gesendet, landet im Mempool | Nodes, Mempool | Sekunden–Minuten |
| 4. Bestätigung | Miner/Validator fügt Transaktion zu einem Block hinzu | Miner/Validatoren | Minuten–Stunden |
| 5. Finalisierung | Block wird zur Chain hinzugefügt, Transaktion abgeschlossen | Alle Netzwerk-Nodes | Noch ein paar Blöcke |

---

## Was ist mit den Gebühren?

Die Gebühr ist die Bezahlung für einen Platz in einem Block. Sie besteht aus zwei Teilen:

- **Base Fee** – der vom Netzwerk festgelegte Basispreis;
- **Priority Fee** – das, was du freiwillig drauflegst, um es zu beschleunigen.

Bei Bitcoin richtet sich die Gebühr nicht nach dem Betrag, den du sendest – sondern nach der **Transaktionsgröße in Bytes**. Je komplexer die Transaktion (viele Inputs/Outputs), desto „schwerer" und teurer ist sie.

Bei Ethereum hängt die Gebühr von der Komplexität der Operation ab (Gas). Eine einfache Überweisung kostet etwa 21.000 Gas. Die Interaktion mit einem Smart Contract kann Hunderttausende kosten.

> Mehr dazu: [Netzwerkgebühr](/de/glossary/#network-fee), [Gas](/de/glossary/#gas).

---

## Was sieht der Empfänger?

Der Empfänger kann die Transaktion sehen, sobald sie gesendet wird – noch vor der Bestätigung.

Seine Wallet zeigt möglicherweise den Status „Ausstehend" an. Die Coins sind noch nicht angekommen, aber es ist klar, dass eine Überweisung unterwegs ist.

Nach der ersten Bestätigung aktualisiert sich der Saldo. Börsen und Dienste schreiben Guthaben in der Regel erst nach einer bestimmten Anzahl von Bestätigungen gut – aus Sicherheitsgründen.

---

## Was kann schiefgehen?

### Steckengebliebene Transaktion

Ist die Gebühr zu niedrig, ignorieren Miner deine Transaktion möglicherweise. Sie bleibt im Mempool und wartet.

Bei Bitcoin können solche Transaktionen tagelang dort sitzen. Bei Ethereum gibt es den Replace-by-Fee-Mechanismus – du kannst dieselbe Transaktion mit einer höheren Gebühr erneut senden.

### Abgelehnte Transaktion

Wenn das Netzwerk überlastet ist und deine Gebühr minimal, kann die Transaktion aus dem Mempool „geworfen" und unausgegeben zurückgegeben werden. Dein Geld verschwindet nicht – es geht zurück an deine Adresse.

### Annullierte Transaktion

Du kannst eine signierte und gesendete Transaktion nicht annullieren. Das ist die Natur der Blockchain – der Eintrag ist unveränderlich. Hast du an die falsche Adresse gesendet, kann nur der Empfänger die Coins zurückgeben.

> Überprüfe die Adresse immer doppelt vor dem Senden. Mindestens die ersten 4 und die letzten 4 Zeichen.

---

## Fazit

Wenn du auf „Senden" drückst, startet eine ganze Kette von Ereignissen:

1. **Erstellung** – deine Wallet bereitet die Daten vor.
2. **Signierung** – dein privater Schlüssel beweist, dass es dein Geld ist.
3. **Broadcasting** – die Transaktion saust durchs Netzwerk in den Mempool.
4. **Bestätigung** – ein Miner nimmt sie in einen Block auf.
5. **Finalisierung** – der Block wird dauerhafter Teil der Blockchain.

Dieses gesamte System funktioniert ohne Banken, ohne Mittelsmänner, ohne eine einzige zentrale Autorität. Nur Mathematik, tausende unabhängige Computer und dein privater Schlüssel.

> Crypto ist keine Magie. Es ist Mathematik – die Art, die dir die Kontrolle über dein eigenes Geld gibt.

---

## FAQ

### Kann ich eine Transaktion nach dem Senden annullieren?
Nein. Sobald eine Transaktion signiert und an das Netzwerk gesendet wurde, kann sie nicht mehr annulliert werden. Nur der Empfänger kann das Geld zurückschicken. Überprüfe immer die Adresse.

### Warum gehen manche Transaktionen in Minuten durch, während andere Stunden dauern?
Es kommt auf die Gebühr und die Netzwerkauslastung an. In Spitzenzeiten wählen Miner die Transaktionen mit den höchsten Gebühren aus. Ist deine niedrig – wartest du.

### Was passiert, wenn ich Coins an eine nicht existierende Adresse sende?
Höchstwahrscheinlich lehnt das Netzwerk die Transaktion ab. Aber wenn die Adresse existiert und einfach niemandem gehört (oder jemand anderem), gehen die Coins dorthin, ohne dass du sie zurückholen kannst.

### Was ist Double-Spending?
Es ist der Versuch, dieselben Coins an zwei verschiedene Empfänger zu senden. Die Blockchain verhindert das durch Konsens: Die zuerst bestätigte Transaktion gilt als gültig, die zweite wird abgelehnt.

### Wie kann ich den Status meiner Transaktion überprüfen?
Nutze einen Blockchain-Explorer. Für Bitcoin – [mempool.space](https://mempool.space), für Ethereum – [etherscan.io](https://etherscan.io). Füge deinen Transaktions-Hash ein, und du siehst alles: vom Mempool bis zur endgültigen Bestätigung.
