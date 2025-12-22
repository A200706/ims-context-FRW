# FRW_K07_VST_Zahlungsverkehr_Kontokorrent_Kasse_Karten.md

> Kapitel 7 aus Upload: Verrechnungssteuer (VST), Konten des Zahlungsverkehrs (Bank/Post/Kasse), Kontokorrent (KK) + Auszug, Kassenbuch/Kassendifferenz, Debit-/Kreditkarten (Verkäufer/Käufer), Zinsen + Spesen.  
> Stil: **Antwort-Only**, kurz, einfache Wörter (A2–B1), viele Templates, schnell lesbar.

---

## 0) OUTPUT MODE (STRICT)

### 0.1 Antwort-Regel (immer)
- **Kein Intro. Keine langen Erklärungen.**
- Start immer so:
  - `Aufgabe {Nr}: {Kurzname}`
- Danach nur:
  - `Fill-in:` (wenn Tabelle/Auszug ergänzt werden muss)
  - `Buchung:` (Soll/Haben/Betrag)
  - `Posting:` (nur wenn T-Konten verlangt sind)
  - kurze Stichworte (wenn Begründung gefragt ist)

### 0.2 Pflicht-Formate
**Buchungssatz:**
- `Soll / Haben / Betrag`

**Wenn T-Konten/Tabelle gefordert:**
- zusätzlich:
  - `Posting: Konto X -> Soll (links) +...`
  - `Posting: Konto Y -> Haben (rechts) +...`

**Wenn Kontoauszug/Kassenbuch ergänzt werden soll:**
- zuerst: `Fill-in: Feld = Wert`
- dann: Buchungen (falls verlangt)

---

## 1) DEIN POSTING-SYSTEM (immer gleich)

### 1.1 Seiten
- links = **Soll**
- rechts = **Haben**

### 1.2 4 Kontoarten (Regelblock)
- **Aktivkonto**: `+` Soll, `-` Haben
- **Passivkonto**: `-` Soll, `+` Haben
- **Aufwandkonto**: `+` Soll, `-` Haben
- **Ertragkonto**: `-` Soll, `+` Haben

---

## 2) RESPONSE TYPES (Index) – schnell erkennen

### RT-K07-1: VST Grundwissen (R/F, Definition)
- Output:
  - `Aufgabe {Nr}: VST Aussagen`
  - `1: R/F + Korrektur (kurz)`
  - `2: R/F + Korrektur (kurz)` usw.

### RT-K07-2: Zinsgutschrift mit VST (Habenzinsüberschuss)
- Output:
  - `Aufgabe {Nr}: Habenzins mit VST`
  - `Buchung: Bank / Finanzertrag / Nettozins`
  - `Buchung: Guthaben VST / Finanzertrag / VST`

### RT-K07-3: Rückerstattung VST
- Output:
  - `Aufgabe {Nr}: VST Rückerstattung`
  - `Buchung: Bank / Guthaben VST / Betrag`

### RT-K07-4: Sollzins (Zinsschuld an Bank)
- Output:
  - `Aufgabe {Nr}: Sollzins`
  - `Buchung: Finanzaufwand / Bank / Betrag`

### RT-K07-5: Bankspesen/Kommission
- Output:
  - `Aufgabe {Nr}: Spesen`
  - `Buchung: Finanzaufwand / Bank / Betrag`

### RT-K07-6: KK-Auszug ergänzen (Saldo/Beträge)
- Output:
  - `Aufgabe {Nr}: KK-Auszug Fill-in`
  - `Fill-in: fehlende Beträge/Saldo = ...`
  - (wenn verlangt) `Buchungen:` wichtige Zeilen (Zins/Spesen/Einzahlungen/Bezüge)

### RT-K07-7: Art des KK (ankreuzen + kurz begründen)
- Output:
  - `Aufgabe {Nr}: KK-Art`
  - `Antwort: Debitoren-KK / Kreditoren-KK / wechselnd`
  - `Begründung: Stichworte (Saldo + Zinsart)`

### RT-K07-8: Kassenbuch (eintragen + buchen)
- Output:
  - `Aufgabe {Nr}: Kassenbuch`
  - `Fill-in: Eintrag(e) + neuer Bestand`
  - `Buchung:` (falls verlangt)

### RT-K07-9: Kassendifferenz (Manko/Überschuss)
- Output:
  - `Aufgabe {Nr}: Kassendifferenz`
  - `Grund 1: ...`
  - `Grund 2: ...`
  - `Buchung: ...`

### RT-K07-10: Verkauf mit Debitkarte (Verkäufer)
- Output:
  - `Aufgabe {Nr}: Debitkartenverkauf`
  - `Buchung: Forderungen Debitkarten / Ertrag / Bruttobetrag`
  - später:
    - `Buchung: Bank / Forderungen Debitkarten / überwiesener Betrag`
    - `Buchung: Finanzaufwand / Forderungen Debitkarten / Kommission`

### RT-K07-11: Verkauf mit Kreditkarte (Verkäufer)
- Output:
  - `Aufgabe {Nr}: Kreditkartenverkauf`
  - `Buchung: Forderungen Kreditkarten / Ertrag / Bruttobetrag`
  - Abrechnung kommt: **keine Buchung** (kein Wertfluss)
  - Überweisung:
    - `Buchung: Bank / Forderungen Kreditkarten / überwiesener Betrag`
    - `Buchung: Finanzaufwand / Forderungen Kreditkarten / Kommission`

### RT-K07-12: Einkauf mit Debitkarte (Käufer)
- Output:
  - `Aufgabe {Nr}: Einkauf Debitkarte`
  - `Buchung: Aufwand/Anlagekonto / Bank / Betrag`

### RT-K07-13: Einkauf mit Kreditkarte (Käufer)
- Output:
  - `Aufgabe {Nr}: Einkauf Kreditkarte`
  - `Buchung: Aufwand/Anlagekonto / Verbindlichkeiten Kreditkarten / Betrag`
  - später Zahlung:
    - `Buchung: Verbindlichkeiten Kreditkarten / Bank / Betrag`

---

## 3) VST (Verrechnungssteuer) – das Prüfungszeug

### 3.1 Zweck (kurz)
- VST macht Steuerhinterziehung unattraktiv (bei gewissen Vermögenserträgen).

### 3.2 Was ist wichtig im Kapitel?
- VST ist **35%** auf gewissen Erträgen (im Stoff: Zinsen).
- Bei Kontokorrent mit wechselndem Kreditverhältnis:
  - Habenzins und Sollzins werden verrechnet.
  - **Nur Habenzinsüberschuss** ist VST-pflichtig.

### 3.3 Schnell-Rechnen mit 35%
- **Bruttozins = 100%**
- **Nettozins = 65%**
- **VST = 35%**

Wenn **Netto** gegeben ist:
- `Brutto = Netto / 0.65`
- `VST = Brutto * 0.35`  (oder `Netto / 0.65 * 0.35`)

### 3.4 Freigrenze (aus Aufgabenlösung)
- Bei **einmaliger jährlicher Zinsgutschrift** gibt es eine **Freigrenze CHF 200**.
- Wenn im Aufgabentext steht “quartalsweise Abrechnung / Kontoauszug”: dann VST nach Regel im Fall anwenden.

### 3.5 Verbuchung: Netto-Methode (empfohlen, 2 Zeilen, klar)
**Habenzins mit VST:**
1) `Bank / Finanzertrag / Nettozins`
2) `Guthaben VST / Finanzertrag / VST`

**Rückerstattung VST:**
- `Bank / Guthaben VST / Betrag`

**MERKE (aus Theorie):**
- Brutto- oder Nettoverbuchung ändert **nicht** die Salden (nur Darstellung).

---

## 4) KONTOKORRENT (KK) – Kippkonto + Auszug

### 4.1 Eigenschaften (kurz)
- Viele Ein- und Auszahlungen.
- Konto kann **überzogen** werden.
- Aus Sicht Unternehmen kann Bankkonto:
  - **Aktiv** sein (Guthaben)
  - **Passiv** sein (Schuld)

### 4.2 Zinsen im KK
- **Soll-Saldo** → **Sollzins** (Zinsschuld)
- **Haben-Saldo** → **Habenzins** (Zinsguthaben)
- Sollzins-Satz meist höher als Habenzins-Satz.

### 4.3 Spesen/Kommission (Bruttoprinzip)
- Spesen/Kommission sind **Aufwand**:
  - `Finanzaufwand / Bank / Betrag`
- **Nicht** als “Ertragsminderung” buchen.

### 4.4 KK-Arten (aus MERKE)
- **Debitoren-KK** (Bank hat Guthaben / Kunde hat Schuld) → Bank belastet Sollzins
- **Kreditoren-KK** (Bank hat Schuld / Kunde hat Guthaben) → Bank schreibt Habenzins gut
- **Wechselnd** → mal Guthaben, mal Schuld; Zinsen werden verrechnet; Habenzinsüberschuss evtl. VST

**Output bei MC/Begründung:**
- `Antwort: ...`
- `Begründung: Saldo + Sollzins/Habenzins (Stichworte)`

---

## 5) KK-AUSZUG ERGÄNZEN (Fill-in Algorithmus)

### 5.1 Saldo-Regel (für jede Zeile)
- Start: `Saldo neu = Saldovortrag`
- Für jede Buchungszeile:
  - wenn **Gutschrift**: `Saldo = Saldo + Gutschrift`
  - wenn **Belastung**: `Saldo = Saldo - Belastung`

### 5.2 Fill-in Output Format
- `Aufgabe {Nr}: KK-Auszug Fill-in`
- `Fill-in: Saldovortrag = ...`
- `Fill-in: Zeile X (Belastung/Gutschrift) = ...`
- `Fill-in: Saldo nach Zeile X = ...`
- am Ende:
  - `Fill-in: Saldo per ... = ...`

### 5.3 Häufige Buchungstexte → typische Buchung (wenn verlangt)
- Bareinzahlung aus Kasse am Bankschalter:
  - `Bank / Kasse / Betrag`
- Barbezug:
  - `Kasse / Bank / Betrag`
- Lohnzahlungen:
  - `Lohnaufwand / Bank / Betrag`
- Kundenzahlungen (bereits verbuchte Rechnungen):
  - `Bank / Forderungen aus LL / Betrag`
- Zahlung Lieferantenrechnung (bereits verbucht):
  - `Verbindlichkeiten aus LL / Bank / Betrag`
- Spesen/Kommission:
  - `Finanzaufwand / Bank / Betrag`
- Sollzins:
  - `Finanzaufwand / Bank / Betrag`
- Habenzins mit VST:
  - siehe RT-K07-2 (2 Buchungen)

---

## 6) KASSE + KASSENBUCH + KASSENDIFFERENZ

### 6.1 Kassenbuch (kurz)
- Einnahmen/Ausgaben werden im Kassenbuch erfasst.
- Bestand wird laufend gerechnet.

**Output (typisch):**
- `Fill-in: Datum, Text, Einnahme, Ausgabe, Bestand`

### 6.2 Kassensturz (Inventar) + Kassendifferenz
- Am Abschluss: Noten/Münzen zählen = **Inventarwert**.
- Vergleich:
  - Inventarwert vs. provisorischer Saldo Konto Kasse

**Kassenmanko** (Inventar < Buchsaldo):
- `Sonstiger Betriebsaufwand / Kasse / Differenz`

**Kassenüberschuss** (Inventar > Buchsaldo):
- `Kasse / Übriger Ertrag / Differenz`

**Wenn Gründe gefragt (2 Stück):**
- `Grund 1: Falschbuchung`
- `Grund 2: Diebstahl / Fehler beim Herausgeben von Geld`

**Output-Beispiel:**
- `Aufgabe {Nr}: Kassendifferenz`
- `Grund 1: ...`
- `Grund 2: ...`
- `Buchung: ...`

---

## 7) DEBITKARTE & KREDITKARTE (Verkäufer vs Käufer)

### 7.1 Verkäufer: Debitkartenverkauf
- Verkauf wird über **Forderungen Debitkarten** gebucht (z.B. mit Kassenbeleg).
- Später (Bankbeleg): Bankgutschrift + Kommission.

**Template:**
1) Verkauf:
- `Forderungen Debitkarten / Ertrag / Bruttobetrag`

2) Überweisung + Kommission:
- `Bank / Forderungen Debitkarten / überwiesener Betrag`
- `Finanzaufwand / Forderungen Debitkarten / Kommission`

### 7.2 Verkäufer: Kreditkartenverkauf
- Gleich wie Debit, aber Konto: **Forderungen Kreditkarten**.
- Abrechnung der Kreditkartengesellschaft: **keine Buchung** (noch kein Wertfluss).
- Bei Überweisung: Bank + Kommission buchen.

**Template:**
1) Verkauf:
- `Forderungen Kreditkarten / Ertrag / Bruttobetrag`

2) Abrechnung kommt:
- `Keine Buchung`

3) Überweisung + Kommission:
- `Bank / Forderungen Kreditkarten / überwiesener Betrag`
- `Finanzaufwand / Forderungen Kreditkarten / Kommission`

### 7.3 Käufer: Einkauf mit Debitkarte
- Belastung erfolgt schnell; meistens direkt über Bank.
- `Aufwand/Anlagekonto / Bank / Betrag`

### 7.4 Käufer: Einkauf mit Kreditkarte
- Zuerst Schuld an Kreditkartenanbieter:
  - `Aufwand/Anlagekonto / Verbindlichkeiten Kreditkarten / Betrag`
- Später Zahlung der Abrechnung:
  - `Verbindlichkeiten Kreditkarten / Bank / Betrag`

**MERKE (aus Theorie):**
- Kommission betrifft den **Verkäufer**, nicht den Käufer.

---

## 8) “WO SCHREIBE ICH WAS HIN?” (prüfungspraktisch)

### 8.1 Nur Buchungssätze gefragt
- nur: `Soll / Haben / Betrag` (jede Buchung neue Zeile)

### 8.2 T-Konten gefragt
- nach jeder Buchung zusätzlich Posting:
  - `Posting: Bank -> Soll (links) +500`
  - `Posting: Finanzaufwand -> Soll (links) +500`
  - `Posting: Bank -> Haben (rechts) +500` usw.

### 8.3 Kontoauszug/Kassenbuch ergänzt
- zuerst alle `Fill-in` Werte einsetzen
- danach (falls gefragt) Buchungen

---

## 9) FEHLERFALLEN (Punkte-Killer)

- VST falsch: **Netto (65%)** vs **VST (35%)** verwechselt.
- Habenzinsüberschuss nicht erkannt (bei wechselndem KK).
- Spesen fälschlich vom Ertrag abziehen (falsch, Bruttoprinzip).
- Kreditkarten-Abrechnung gebucht (obwohl kein Wertfluss).
- Bei Auszug: Saldo-Rechnung falsch (Gutschrift/Belastung vertauscht).
- Kassendifferenz falsch: Manko vs Überschuss vertauscht.

---
