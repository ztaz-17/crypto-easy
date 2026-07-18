---
weight: 4
title: "Warum Transaktionen hängen bleiben und was man dagegen tun kann"
description: "Warum Krypto-Transaktionen hängen bleiben: niedrige Gebühren, Netzüberlastung. So beschleunigst oder stornierst du eine steckengebliebene Transaktion"
category: "how-it-works"
translationKey: "why-transactions-stuck"
slug: "warum-transaktionen-haengen-bleiben"
keywords:
  - steckengebliebene Transaktion
  - ausstehende Transaktion
  - Replace-by-Fee
  - RBF
  - Transaktionsbeschleunigung
  - Bitcoin hängt
  - Ethereum hängt
prev: "/de/learn/how-it-works/block-bestaetigungen"
next: "/de/learn/how-it-works/verschiedene-netzwerke-erc20-trc20-bsc"
---

## Warum Transaktionen hängen bleiben und was man dagegen tun kann

---

Du schickst etwas Krypto. Der Betrag stimmt, die Adresse ist korrekt, du drückst auf Senden.

Und auf dem Bildschirm — »Ausstehend.« Eine Stunde. Zwei. Fünf.

Die Coins wurden abgezogen, aber der Empfänger sieht sie nicht. Die Transaktion steckt in der »Warten auf Bestätigung«-Endlosschleife fest, und nichts passiert.

Kommt dir bekannt vor?

> **Eine steckengebliebene Transaktion** — eines der häufigsten Probleme für Krypto-Einsteiger. Aber es ist fast immer behebbar.

In diesem Artikel erfährst du:

> - warum Transaktionen hängen bleiben;
> - wie du erkennst, ob sie wirklich feststeckt oder nur etwas Zeit braucht;
> - was du jetzt tun kannst: beschleunigen, stornieren oder ersetzen;
> - und wie du diese Situation in Zukunft vermeidest.

---

## Warum Transaktionen hängen bleiben

### 1. Gebühr zu niedrig

Das ist der häufigste Grund.

Jede Blockchain-Transaktion ist eine Anfrage auf einen Platz in einem Block. Der Platz im Block ist begrenzt. Miner (Bitcoin) oder Validatoren (Ethereum) entscheiden, welche Transaktionen zuerst aufgenommen werden.

Die Regel ist einfach: **Wer mehr zahlt, kommt zuerst.**

Wenn du deine Gebühr unter dem aktuellen Marktpreis ansetzt — bleibt deine Transaktion im Mempool und wartet darauf, dass das Netzwerk sich leert.

Mehr zur Gebührenermittlung: [Warum Krypto zu versenden manchmal 30 $ kostet](/de/learn/how-it-works/why-transaction-costs-30).

---

### 2. Netzüberlastung (Mempool ist voll)

Selbst mit einer angemessenen Gebühr kann deine Transaktion zu Stoßzeiten hängen bleiben.

Wenn tausende Transaktionen gleichzeitig gesendet werden (z. B. bei einem Memecoin-Hype, einem NFT-Mint oder einem Großereignis), wird der Mempool überschwemmt. Die Blockgröße bleibt gleich, aber die Anzahl der Leute, die reinwollen, ist zehnmal höher als sonst.

In solchen Zeiten picken sich Miner nur die fettesten Transaktionen heraus — alle anderen warten.

> Bitcoins Mempool kann **300.000+ unbestätigte Transaktionen** erreichen. Die Warteschlange bei Ethereum ist kleiner, aber zu Stoßzeiten kann die Basisgebühr um das 5- bis 10-Fache steigen.

---

### 3. Feststecken wegen eines Wallet-Fehlers

Manchmal liegt das Problem nicht am Netzwerk — sondern an deinem Wallet:

- Gas wurde falsch berechnet (bei Ethereum — Gas-Limit unter 21.000);
- das Wallet hat den Transaktionsstatus nicht aktualisiert;
- du bist mit einem veralteten oder defekten Knoten verbunden.

In diesen Fällen wird die Transaktion vielleicht sogar nach der Bestätigung noch als »gesendet« angezeigt. Prüfe es in einem Blockchain-Explorer — wahrscheinlich ist alles in Ordnung.

---

### 4. Eine Transaktion mit sehr niedriger Priorität wurde verworfen

Wenn der Mempool vollgestopft ist und deine Gebühr extrem niedrig, kann es passieren, dass einige Knoten die Transaktion einfach aus dem Pool werfen. Sie verschwindet nicht für immer — wenn sie nie erneut gesendet wird, »verdampft« sie und die Coins bleiben auf deiner Adresse.

Aber bis du eine neue Transaktion sendest, sind deine Gelder praktisch »eingefroren«: Das Netzwerk ignoriert die alte, und du kannst keine neue senden, weil dein Wallet denkt, diese Coins seien bereits weg.

---

## Wie du erkennst, ob eine Transaktion wirklich feststeckt

Bevor du in Panik gerätst, prüfe den Transaktionsstatus in einem Blockchain-Explorer:

| Netzwerk | Explorer |
|----------|----------|
| Bitcoin | [mempool.space](https://mempool.space) |
| Ethereum | [etherscan.io](https://etherscan.io) |
| Solana | [solscan.io](https://solscan.io) |
| TRON | [tronscan.org](https://tronscan.org) |
| BNB Chain | [bscscan.com](https://bscscan.com) |

Füge deinen Transaktions-Hash (TXID) ein — und du siehst den Status:

- **Ausstehend / Im Mempool** — die Transaktion ist in der Warteschlange, noch nicht in einem Block.
- **Bestätigt / Erfolgreich** — alles ist in Ordnung, dein Wallet aktualisiert nur langsam.
- **Verworfen / Ersetzt** — die Transaktion wurde ersetzt oder aus dem Mempool entfernt.

> Wenn der Status »Bestätigt« ist, aber dein Wallet »Ausstehend« anzeigt — liegt es am Wallet, nicht am Netzwerk. Aktualisiere oder starte die App neu.

---

## Was tun, wenn deine Transaktion feststeckt?

Du hast mehrere Optionen. Welche du wählst, hängt vom Netzwerk, deinem Wallet und deiner Geduld ab.

---

### 1. Transaktion per RBF (Replace-by-Fee) ersetzen

**Funktioniert bei:** Bitcoin (und einigen anderen UTXO-basierten Chains)  
**Erfordert:** ein Wallet, das RBF unterstützt

Replace-by-Fee ist ein Mechanismus, mit dem du dieselbe Transaktion (gleiche Inputs) mit einer höheren Gebühr erneut senden kannst. Du sagst dem Netzwerk: »Vergiss die alte Transaktion — hier ist die neue mit einem Aufschlag.«

So geht's:

1. Öffne dein Wallet und suche die steckengebliebene Transaktion.
2. Suche nach **»Gebühr erhöhen«** oder **»Replace-by-Fee«** (der Name hängt von deinem Wallet ab).
3. Setze eine neue Gebühr — in der Regel reicht der aktuelle Marktpreis.
4. Bestätige — und die neue Transaktion ersetzt die alte.

**Wichtig:** RBF muss aktiviert sein, bevor du die erste Transaktion sendest. Wenn du eine Transaktion ohne RBF-Flag gesendet hast — kannst du sie über diesen Mechanismus nicht ersetzen.

Wallets mit RBF-Unterstützung:

- Electrum — volle Unterstützung;
- Bitcoin Core — ja;
- BlueWallet — ja;
- Exodus — ja;
- Trust Wallet — nein (Stand heute).

> Wenn dein Wallet RBF nicht unterstützt — probiere Option 2 oder 3.

---

### 2. Einen Transaktionsbeschleuniger nutzen

**Funktioniert bei:** Bitcoin (eingeschränkt)

Einige Mining-Pools bieten Transaktionsbeschleunigungsdienste an. Du reichst den Hash deiner steckengebliebenen Transaktion ein, zahlst eine Gebühr — und der Pool nimmt sie in den nächsten Block auf, den er schürft.

Beliebte Dienste:

- [Viabtc Accelerator](https://www.viabtc.com/tools/txaccelerator) — kostenlos für bis zu 100 Transaktionen pro Stunde, aber keine Garantie;
- [BTC.com Accelerator](https://pushtx.btc.com/) — kostenlos.

**Nachteile:**

- sie funktionieren nicht immer;
- kostenlose Plätze sind schnell belegt;
- bezahlte Versionen kosten Geld (oft mehr als eine normale Gebühr).

Nutze dies nur, wenn RBF nicht verfügbar ist und du nicht länger warten kannst.

---

### 3. Per Double-Spend stornieren (Child-Pays-For-Parent / CPFP)

**Funktioniert bei:** Bitcoin, Ethereum und anderen Netzwerken

CPFP ist ein Mechanismus, bei dem du eine **neue Transaktion** sendest, die die Outputs (UTXOs) der steckengebliebenen Transaktion ausgibt. Die neue hat eine höhere Gebühr — Miner nehmen beide mit, denn ohne die erste ist die zweite ungültig.

So geht's:

1. Finde die steckengebliebene Transaktion in deinem Wallet.
2. Wenn dein Wallet CPFP unterstützt — wähle **»Mit Kind-Transaktion beschleunigen«**.
3. Setze die Gebühr für die Kind-Transaktion.
4. Bestätige.

**Für Ethereum (MetaMask):**

1. Öffne in MetaMask die steckengebliebene Transaktion.
2. Klicke auf **»Speed up«** — das Wallet sendet dieselbe Transaktion mit einer höheren Gebühr erneut.
3. Oder klicke auf **»Cancel«** — MetaMask sendet eine »leere« Transaktion (0 ETH), die die alte überschreibt.

> **Wichtig:** Das Stornieren auf Ethereum ist ebenfalls eine Transaktion mit Gebühr. Du zahlst, um die steckengebliebene zu ersetzen.

---

### 4. Einfach warten

Ja, das ist auch eine Option.

Bei Bitcoin können Transaktionen mit niedrigen Gebühren stunden- oder tagelang hängen. Aber früher oder später — wenn das Netzwerk sich leert oder jemand die Gebühr in diesem Block erhöht — kommt deine Transaktion durch.

Voraussichtliche Wartezeiten:

- **Bitcoin:** von 1 Stunde bis 3–7 Tage in Extremfällen (wenn der Mempool voll und deine Gebühr minimal ist).
- **Ethereum:** von 1 Minute bis zu ein paar Stunden.
- **Solana / TRON:** bleiben selten hängen, aber wenn doch — bis zu einer Stunde.

> Wenn mehr als 3 Tage vergangen sind und die Transaktion immer noch »Ausstehend« ist — probiere eine der oben genannten Methoden.

---

### 5. Erneut senden, nachdem die Transaktion aus dem Mempool gefallen ist

Wenn die Transaktion aus dem Mempool entfernt wurde (in der Regel nach 2–7 Tagen bei Bitcoin, schneller bei anderen Netzwerken) — kommen die Coins automatisch auf deine Adresse zurück.

Du kannst einfach eine neue Transaktion senden — mit einer angemessenen Gebühr und in einer ruhigen Phase.

Es gibt einen Haken: Nicht alle Wallets zeigen die Rückkehr korrekt an. Es könnte immer noch so aussehen, als wären deine Gelder »gesperrt«. Überprüfe deinen Saldo in einem Blockchain-Explorer — wenn die Transaktion aus dem Mempool verschwunden ist, gehören die Coins wieder dir.

---

## Kurzreferenz: Was tun in jeder Situation

| Situation | Bitcoin | Ethereum | Andere Netzwerke |
|-----------|---------|----------|------------------|
| Niedrige Gebühr, RBF aktiviert | **RBF** — mit Aufschlag ersetzen | **Speed up** in MetaMask | Abhängig vom Wallet |
| Niedrige Gebühr, RBF deaktiviert | **CPFP** oder Beschleuniger | **Cancel** + neue Transaktion | Neue mit höherer Nonce senden |
| Netzüberlastung | Warten oder Beschleuniger | Warten — Gas fällt wieder | Warten |
| Transaktion aus Mempool gefallen | Neu senden | Neu senden | Neu senden |
| Wallet zeigt falschen Status | Explorer prüfen | Explorer prüfen | Explorer prüfen |
| Muss sofort durchgehen | Beschleuniger (bezahlt) | Speed up mit hohem Gas | Gebühr erhöhen |

---

## Wie du steckengebliebene Transaktionen in Zukunft vermeidest

### 1. Prüfe den Mempool vor dem Senden

Bevor du eine Transaktion sendest, checke die Netzauslastung:

- Bitcoin: [mempool.space](https://mempool.space)
- Ethereum: [etherscan.io/gastracker](https://etherscan.io/gastracker)

Wenn der Mempool voll ist — warte ein bis zwei Stunden oder erhöhe die Gebühr.

### 2. Setze deine Gebühr etwas über dem Durchschnitt

Fortgeschrittene Wallets bieten drei Gebührenstufen:

- **Slow (Langsam)** — du sparst Geld, aber das Risiko des Steckenbleibens ist höher;
- **Market / Normal (Marktüblich)** — ein ausgewogener Kompromiss;
- **Fast (Schnell)** — du zahlst mehr, aber die Transaktion kommt im nächsten Block durch.

Wähle in den meisten Fällen **Market**. Der Unterschied zwischen Slow und Market beträgt normalerweise 0,50–2 $, aber die Wartezeit ist 3- bis 5-mal kürzer.

### 3. RBF vorher aktivieren

Wenn dein Wallet RBF unterstützt — **schalte es in den Einstellungen ein, bevor du sendest.** Es ändert nichts an der Gebühr für die erste Transaktion, gibt dir aber die Möglichkeit, sie zu ersetzen, falls etwas schiefgeht.

### 4. Wähle das richtige Netzwerk

Bitcoin und Ethereum sind nicht die einzigen Optionen. Wenn du sie nicht zwingend brauchst:

- **Litecoin** — Blöcke alle 2,5 Minuten, Gebühren sind Centbeträge;
- **Solana** — sofortig, nahezu kostenlos;
- **TRON** — günstig und schnell für USDT;
- **Lightning Network** — Bitcoin, aber Bestätigung in Sekunden.

> Stelle nur sicher, dass der Empfänger das von dir gewählte Netzwerk unterstützt.

### 5. Nutze Layer-2-Netzwerke

Wenn du auf Ethereum unterwegs bist:

- Arbitrum;
- Optimism;
- Base;
- zkSync.

Die Gebühren sind 50- bis 100-mal niedriger als im Ethereum-Mainnet, bei gleicher Sicherheit.

---

## Eine wahre Geschichte

Vor einiger Zeit kaufte ich eine Domain für 0,5 ETH. Ich gab die Adresse ein, überprüfte sie, drückte auf Senden. Die Gebühr war auf »Slow« eingestellt — ich dachte, ich spare 3 $.

15 Minuten vergingen. Die Transaktion war ausstehend.

30 Minuten — ausstehend.

Eine Stunde — ausstehend.

Mir wurde ganz anders: Die Domain könnte weg sein, wenn ich nicht bald zahlte. Ich checkte Etherscan — der Mempool war voll (irgendein NFT-Verkauf lief gerade), die Basisgebühr hatte sich verdoppelt. Meine Transaktion war ganz unten in der Warteschlange.

Ich musste »Speed up« drücken und 22 $ Gebühr zahlen statt der geplanten 4 $.

**Fazit:** Ich bekam die Domain, aber der Versuch, 3 $ zu sparen, kostete mich am Ende 18 $ extra. Hätte ich von Anfang an eine angemessene Gebühr gesetzt, wäre die Transaktion in 2 Minuten durchgewesen.

> Seitdem setze ich nie die Mindestgebühr, wenn die Zeit eine Rolle spielt. 2 $ zu sparen ist keine Stunde Stress wert.

---

## Zusammenfassung

Eine steckengebliebene Transaktion ist ärgerlich, aber fast immer behebbar.

**Die wichtigsten Erkenntnisse:**

- Grund Nr. 1 — niedrige Gebühr und ein überlasteter Mempool;
- zuerst den Status in einem Blockchain-Explorer prüfen — die Transaktion ist vielleicht schon bestätigt;
- RBF (Bitcoin) oder Speed up (Ethereum) nutzen, um zu beschleunigen;
- wenn RBF nicht verfügbar ist — CPFP oder einen Beschleuniger versuchen;
- als letzte Möglichkeit — einfach warten, die Transaktion verschwindet nicht (Coins kommen zurück);
- in Zukunft — eine angemessene Gebühr setzen, den Mempool beobachten und RBF vorher aktivieren.

Krypto ist nicht »senden und vergessen.« Es geht darum, zu verstehen, wie das Netzwerk funktioniert. Und je besser du es verstehst — desto seltener siehst du »Ausstehend« auf deinem Bildschirm.

> Wie man so schön sagt: »Not your keys, not your coins. Not confirmed, not your transaction.«

---

## FAQ

### Warum hängt meine Transaktion bei »Ausstehend«?

Deine Transaktion befindet sich im Mempool, wurde aber noch nicht in einen Block aufgenommen. Die Ursache ist eine zu niedrige Gebühr, Netzüberlastung oder beides.

### Wie lange kann eine Transaktion hängen bleiben?

Bitcoin — von 1 Stunde bis 3–7 Tage. Ethereum — von 1 Minute bis zu mehreren Stunden. Solana, TRON — selten länger als eine Stunde.

### Kann ich eine steckengebliebene Transaktion stornieren?

Ja, wenn sie noch nicht bestätigt wurde. Bei Bitcoin — per RBF (ersetzen) oder CPFP. Bei Ethereum — per »Cancel« in MetaMask. Bei anderen Netzwerken — durch Senden einer Transaktion mit einer höheren Nonce.

### Verliere ich mein Geld, wenn die Transaktion stecken bleibt?

Nein. Wenn die Transaktion nicht in einen Block kommt, wird sie irgendwann aus dem Mempool entfernt, und die Coins kehren auf deine Adresse zurück. Wenn die Transaktion bereits in einem Block ist — ist das Geld beim Empfänger (kann nicht storniert werden).

### Was, wenn mein Wallet RBF nicht unterstützt?

Nutze CPFP (Child-Pays-For-Parent) oder Transaktionsbeschleunigungsdienste (Viabtc, BTC.com). Oder warte einfach.

### Wie überprüfe ich, ob RBF in meinem Wallet aktiviert ist?

Öffne die Einstellungen zum Senden von Transaktionen. Wenn du »RBF aktivieren« oder »Replace-by-Fee« siehst — schalte es ein. Wenn du es nicht siehst, unterstützt dein Wallet es wahrscheinlich nicht. Electrum und Bitcoin Core unterstützen es auf jeden Fall.

### Warum zeigt MetaMask nach der Bestätigung immer noch »Ausstehend« an?

Das ist ein Problem auf Wallet-Seite, nicht am Netzwerk. Überprüfe den Transaktions-Hash auf Etherscan — wenn der Status »Success« ist, ist alles in Ordnung. Aktualisiere MetaMask oder starte die Erweiterung neu.

### Kann ich eine Transaktion auf einer Börse beschleunigen?

In der Regel nicht. Börsen verwenden ihre eigenen internen Wallets und entscheiden selbst, wann sie die Transaktion senden. Wenn eine Börse bei einer Auszahlung trödelt — kontaktiere deren Support.

### Was, wenn meine Transaktion seit einer Woche feststeckt?

Prüfe, ob sie aus dem Mempool entfernt wurde. Wenn ja — sende sie mit einer angemessenen Gebühr neu. Wenn nicht — versuche RBF, CPFP oder einen Beschleuniger. Nach einer Woche bleiben nur noch »tote« Transaktionen im Mempool — fast niemand nimmt sie auf.
