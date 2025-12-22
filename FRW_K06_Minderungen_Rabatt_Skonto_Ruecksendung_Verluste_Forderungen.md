# FRW_K06_Minderungen_Rabatt_Skonto_Ruecksendung_Verluste_Forderungen.md

> Kapitel 6 (Minderungen). Kontext aus deinen Uploads: Arten von Minderungen, Verbuchung (inkl. Umkehrbuchung), Skonto als Zins, Rücksendungen, Verluste Forderungen, Betreibung (Kostenvorschuss, Verlustschein/Verlustausweis), Verzugszins.  
> Stil: **Antwort-Only**, kurz, klar, A2–B1 Wörter, viele Templates.

---

## 0) OUTPUT MODE (STRICT)

### 0.1 Antwort-Regel (immer)
- **Kein Intro. Keine “ich denke”.**
- Start immer so:
  - `Aufgabe {Nr}: {Kurzname}`
- Dann nur:
  - Resultate (CHF / % / Tage)
  - **Buchungssätze** und ggf. **Posting-Anweisung** (T-Konten)

### 0.2 Pflicht-Formate
**Buchungssatz (Standard):**
- `Soll / Haben / Betrag`

**Wenn T-Konten oder Tabelle gefordert:**
- Nach jedem Buchungssatz zusätzlich:
  - `Posting: Konto X -> Soll (links) +...`
  - `Posting: Konto Y -> Haben (rechts) +...`

**Wenn die Aufgabe Werte in eine Tabelle will (Journal, Kassenbuch, ER/Bilanz):**
- Zuerst: `Fill-in: Feldname = Wert`
- Dann: Buchungssätze (falls verlangt)

---

## 1) DEIN POSTING-SYSTEM (immer gleich)

### 1.1 Seiten
- **links = Soll**
- **rechts = Haben**

### 1.2 4 Kontoarten (Regelblock)
- **Aktivkonto**: `+` im **Soll**, `-` im **Haben**
- **Passivkonto**: `-` im **Soll**, `+` im **Haben**
- **Aufwandkonto**: `+` im **Soll**, `-` im **Haben**
- **Ertragkonto**: `-` im **Soll**, `+` im **Haben**

### 1.3 Mini-Merker
- **Soll = nimmt zu** (bei Aktiv/Aufwand)
- **Haben = nimmt zu** (bei Passiv/Ertrag)

---

## 2) RESPONSE TYPES (Index) – schnell erkennen

### RT-K06-1: Rabatt auf Rechnung schon drin (Nettobetrag)
**Typ:** Rabatt ist bereits in Rechnung/Total netto enthalten.  
**Output:**
- `Aufgabe {Nr}: Rabatt in Rechnung`
- `Buchung: nur Nettobetrag buchen`

### RT-K06-2: Nachträglicher Rabatt VOR Zahlung (Kreditkauf/-verkauf)
**Typ:** Rechnung wurde schon gebucht, Rabatt kommt danach, noch nicht bezahlt.  
**Output:**
- `Aufgabe {Nr}: Nachträglicher Rabatt vor Zahlung`
- `Buchung: Umkehrbuchung (Teil der Rechnungsbuchung)`

### RT-K06-3: Nachträglicher Rabatt NACH Zahlung (Rückerstattung)
**Typ:** Rechnung schon bezahlt, später Rabatt, Geld wird zurücküberwiesen.  
**Output:**
- `Aufgabe {Nr}: Rabatt nach Zahlung (Rückerstattung)`
- `Buchung: Zahlung Rabatt (Bank/Post/Kasse beteiligt)`

### RT-K06-4: Skonto bei Barkauf
**Typ:** Bar bezahlt und Skonto direkt ausgehandelt.  
**Output:**
- `Aufgabe {Nr}: Skonto Barkauf`
- `Buchung: nur effektiv bezahlter Betrag`

### RT-K06-5: Skonto bei Kreditkauf/-verkauf (Zahlung innerhalb Skontofrist)
**Typ:** Rechnung gebucht, Zahlung mit Skonto.  
**Output:**
- `Aufgabe {Nr}: Skonto Kredit`
- `Buchung: Umkehrbuchung (Skonto-Anteil) + Zahlung`

### RT-K06-6: Rücksendung VOR Zahlung
**Typ:** Ware/Leistung zurück, Rechnung noch offen.  
**Output:**
- `Aufgabe {Nr}: Rücksendung vor Zahlung`
- `Buchung: Umkehrbuchung (Teil der Rechnungsbuchung)`

### RT-K06-7: Rücksendung NACH Zahlung (Rückerstattung)
**Typ:** Schon bezahlt, dann Rücksendung, Geld zurück.  
**Output:**
- `Aufgabe {Nr}: Rücksendung nach Zahlung`
- `Buchung: Rückerstattung (Bank/Post/Kasse beteiligt)`

### RT-K06-8: Verlust Forderungen (Abschreibung)
**Typ:** Kunde zahlt nicht, Forderung wird abgeschrieben.  
**Output:**
- `Aufgabe {Nr}: Verlust Forderungen`
- `Verluste Forderungen / Forderungen aus LL / Betrag`

### RT-K06-9: Teilzahlung + Rest abschreiben
**Typ:** Kunde zahlt nur Teil, Rest wird erlassen/abgeschrieben.  
**Output:**
- `Aufgabe {Nr}: Teilzahlung + Abschreibung`
- `Bank/Post/Kasse / Forderungen aus LL / Teilbetrag`
- `Verluste Forderungen / Forderungen aus LL / Restbetrag`

### RT-K06-10: Betreibung – Kostenvorschuss (bar oder Rechnung)
**Typ:** Betreibungsamt verlangt Kostenvorschuss.  
**Output:**
- `Aufgabe {Nr}: Kostenvorschuss Betreibung`
- 2–3 Buchungen je nach Variante (siehe Templates)

### RT-K06-11: Betreibungserlös + Verlustschein/Verlustausweis
**Typ:** Betreibung bringt Teilgeld, Rest ist Verlustschein/Verlustausweis.  
**Output:**
- `Aufgabe {Nr}: Betreibungserlös + Verlust`
- `Bank / Forderungen aus LL / Erlös`
- `Verluste Forderungen / Forderungen aus LL / Rest`

### RT-K06-12: Nachträgliche Zahlung im gleichen Jahr (nach Verlustschein)
**Typ:** Im gleichen Jahr kommt doch noch Geld + evtl. Verzugszins.  
**Output:**
- `Aufgabe {Nr}: Nachträgliche Zahlung (gleiches Jahr)`
- `Storno: Forderungen aus LL / Verluste Forderungen / Betrag Verlustschein`
- `Bank / Forderungen aus LL / Betrag Verlustschein`
- `Bank / Zinsertrag / Betrag Verzugszins` (wenn Zins bisher unverbucht)

---

## 3) ENTSCHEIDUNGSRASTER (High ROI, 10 Sekunden)

1) **Einkauf oder Verkauf?**
- Einkauf: du hast **Verbindlichkeiten aus LL**
- Verkauf: du hast **Forderungen aus LL**

2) **Zeitpunkt?**
- Rabatt/Skonto/Rücksendung **vor Zahlung** → meist **Umkehrbuchung**
- **nach Zahlung** → meist **Rückerstattung (Bank/Post/Kasse)**

3) **Art?**
- Rabatt (Prozent / CHF / Naturalrabatt)
- Skonto
- Rücksendung
- Verlust Forderungen (Abschreibung / Betreibung)

4) **Dann Template nehmen** (Kapitel 4–6 unten).

---

## 4) RABATT / ABZÜGE – RECHNEN (wenn im Test gefragt)

### 4.1 Rabatt in % (normal)
- `Rabattbetrag = Listenpreis * Rabatt% / 100`
- `Rechnung reduziert = Listenpreis - Rabattbetrag`

### 4.2 Kaskadenrabatt (mehrere Rabatte nacheinander)
- **Nicht addieren. Schrittweise rechnen.**
- Beispiel-Form:
  - `nach Rabatt1: Preis1 = Listenpreis * (100% - r1)/100`
  - `nach Rabatt2: Preis2 = Preis1 * (100% - r2)/100`
  - `Rechnungsbetrag = Preis2`

### 4.3 Naturalrabatt (Gutgewicht) – rechnen
- `Abgangsgewicht = z.B. 800 kg`
- `Rabatt% vom Gewicht = Rabattkg = Abgangsgewicht * Rabatt%/100`
- `Verrechnetes Gewicht = Abgangsgewicht - Rabattkg`
- `Preis = verrechnetes Gewicht * Preis/kg`

### 4.4 Produktzugabe (z.B. 12. gratis)
- `Preis für alle Stück = Preis pro Stück * Anzahl bezahlt`
- `Tatsächlicher Preis pro Stück = Total bezahlt / (Anzahl bezahlt + gratis)`
- `Rabatt% = (1 - tatsächlicher Preis / normaler Preis) * 100`

### 4.5 Rundung
- Wenn verlangt: `auf 0.05 CHF` runden (5 Rappen).

---

## 5) SKONTO (inkl. Skonto als Zins)

### 5.1 Skonto – Definition (kurz)
- Skonto = Preisnachlass bei **schneller Zahlung**.

### 5.2 Skonto berechnen (Standard)
- `Skonto = Rechnungsbetrag * Skonto% / 100`
- `Zahlung = Rechnungsbetrag - Skonto`

### 5.3 Skonto als Zins (vereinfachte Rechnung)
- Idee: Skonto spart Geld für wenige Tage → hoher Jahreszins.
- **Dreisatz-Form (wie im Stoff):**
  - `Tage-Differenz = Nettofrist - Skontofrist`
  - `Tage-Differenz Tage = Skonto%`
  - `360 Tage = ?%`
- **Kurzform (gleiches Ergebnis):**
  - `Jahreszins% = Skonto% * 360 / (Nettofrist - Skontofrist)`

**Output-Format im Test:**
- `Aufgabe {Nr}: Skonto als Zins`
- `Tage-Differenz = ... Tage`
- `360 Tage = ... %`
- `Ergebnis: Jahreszins = ... %`

---

## 6) VERBUCHUNG – TEMPLATES (Buchungssatz + Posting)

> Nutze Kontonamen aus der Aufgabe. Hier stehen Platzhalter:
- `[AUFWAND]` = z.B. Einkauf, Einkauf Reisen, Materialaufwand
- `[ERTRAG]` = z.B. Produktionserlöse, Honorarertrag
- Zahlungskonto: Bank / Post / Kasse

---

### 6.1 RECHNUNG BUCHEN (Basis)

**Verkauf (Kunde bekommt Rechnung):**
- `Forderungen aus LL / [ERTRAG] / Betrag`
- Posting:
  - `Forderungen aus LL -> Soll (links) +Betrag`
  - `[ERTRAG] -> Haben (rechts) +Betrag`

**Einkauf (Lieferant schickt Rechnung):**
- `[AUFWAND] / Verbindlichkeiten aus LL / Betrag`
- Posting:
  - `[AUFWAND] -> Soll (links) +Betrag`
  - `Verbindlichkeiten aus LL -> Haben (rechts) +Betrag`

---

### 6.2 RABATT VOR ZAHLUNG = UMKEHRBUCHUNG (Teil der Rechnung)

**Verkauf: nachträglicher Kundenrabatt vor Zahlung**
- `[ERTRAG] / Forderungen aus LL / Rabattbetrag`
- Posting:
  - `[ERTRAG] -> Soll (links) +Rabatt` (Ertrag sinkt)
  - `Forderungen aus LL -> Haben (rechts) +Rabatt` (Forderung sinkt)

**Einkauf: nachträglicher Lieferantenrabatt vor Zahlung**
- `Verbindlichkeiten aus LL / [AUFWAND] / Rabattbetrag`
- Posting:
  - `Verbindlichkeiten aus LL -> Soll (links) +Rabatt` (Schuld sinkt)
  - `[AUFWAND] -> Haben (rechts) +Rabatt` (Aufwand sinkt)

---

### 6.3 SKONTO BEI ZAHLUNG (KREDIT) = UMKEHRBUCHUNG + ZAHLUNG

#### A) Verkauf: Kunde zahlt mit Skonto
1) **Skonto-Teil (Umkehrbuchung)**
- `[ERTRAG] / Forderungen aus LL / Skontobetrag`

2) **Zahlung**
- `Bank (oder Post/Kasse) / Forderungen aus LL / Zahlbetrag`

**Posting (Beispiel-Logik):**
- `Bank -> Soll (links) +Zahlbetrag`
- `Forderungen aus LL -> Haben (rechts) +Zahlbetrag`
- `[ERTRAG] -> Soll (links) +Skonto`
- `Forderungen aus LL -> Haben (rechts) +Skonto`

#### B) Einkauf: du zahlst mit Skonto
1) **Skonto-Teil (Umkehrbuchung)**
- `Verbindlichkeiten aus LL / [AUFWAND] / Skontobetrag`

2) **Zahlung**
- `Verbindlichkeiten aus LL / Bank (oder Post/Kasse) / Zahlbetrag`

**Posting:**
- `Verbindlichkeiten -> Soll (links) +Skonto`
- `[AUFWAND] -> Haben (rechts) +Skonto`
- `Verbindlichkeiten -> Soll (links) +Zahlbetrag`
- `Bank/Post/Kasse -> Haben (rechts) +Zahlbetrag`

---

### 6.4 RABATT / RÜCKSENDUNG NACH ZAHLUNG = RÜCKERSTATTUNG

#### A) Verkauf: du zahlst Geld zurück an Kunde
- `[ERTRAG] / Bank (oder Post/Kasse) / Betrag Rückerstattung`
Posting:
- `[ERTRAG] -> Soll (links) +Betrag` (Ertrag sinkt)
- `Bank/Post/Kasse -> Haben (rechts) +Betrag` (Geld raus)

#### B) Einkauf: Lieferant zahlt Geld zurück an dich
- `Bank (oder Post/Kasse) / [AUFWAND] / Betrag Rückerstattung`
Posting:
- `Bank/Post/Kasse -> Soll (links) +Betrag` (Geld rein)
- `[AUFWAND] -> Haben (rechts) +Betrag` (Aufwand sinkt)

---

## 7) VERLUSTE FORDERUNGEN (Kunden zahlen nicht)

### 7.1 Grundbuchung Abschreibung
- `Verluste Forderungen / Forderungen aus LL / Betrag`

**Wichtig (Merksatz):**
- Forderungen aus LL werden über **Verluste Forderungen** abgeschrieben (nicht über “Abschreibungen”).

### 7.2 Konto “Verluste Forderungen” (kurz)
- ist ein **Minusertragskonto**
- Buchungsregeln wie **Aufwandkonto**:
  - `+` im Soll, `-` im Haben
- In ER steht es als **Minus** auf der **Ertragsseite**.

### 7.3 Teilzahlung + Rest abschreiben
- `Bank/Post/Kasse / Forderungen aus LL / Teilbetrag`
- `Verluste Forderungen / Forderungen aus LL / Restbetrag`

---

## 8) BETREIBUNG (Kostenvorschuss, Erlös, Verlustschein)

### 8.1 Kostenvorschuss buchen (3 Varianten)

**Variante 1: Kostenvorschuss bar bezahlt**
- `Forderungen aus LL / Kasse / Betrag KV`

**Variante 2: Betreibungsamt stellt Rechnung**
- `Forderungen aus LL / Verbindlichkeiten aus LL / Betrag KV`

**Variante 3: Rechnung wird bezahlt (Bank/Post)**
- `Verbindlichkeiten aus LL / Bank (oder Post) / Betrag KV`

> Idee: Kostenvorschuss wird **Teil der Forderung** gegen den Schuldner.

### 8.2 Betreibungserlös + Verlustschein/Verlustausweis
- `Bank / Forderungen aus LL / Erlös`
- `Verluste Forderungen / Forderungen aus LL / Rest (inkl. KV, wenn so im Fall)`

**Hinweis (kurz):**
- Verlustausweis bei jur. Person (z.B. AG) = für immer verloren.
- Verlustschein bei nat. Person = evtl. später nochmals betreiben möglich.

### 8.3 Nachträgliche Zahlung im gleichen Jahr + Verzugszins (wenn unverbucht)
1) **Storno der Verlustschein-Buchung**
- `Forderungen aus LL / Verluste Forderungen / Betrag Verlustschein`

2) **Zahlung des früheren Restes**
- `Bank / Forderungen aus LL / Betrag Verlustschein`

3) **Verzugszins (bisher nicht verbucht)**
- `Bank / Zinsertrag (Finanzertrag) / Betrag Verzugszins`

### 8.4 Verzugszins – 2 Varianten (wenn Aufgabe das trennt)
- **Variante A: nur bei Zahlung buchen** (wenn vorher nie als Forderung gebucht)
  - `Bank/Post/Kasse / Zinsertrag / Zinsbetrag`
- **Variante B: zuerst als Guthaben buchen, dann Zahlung**
  1) `Forderungen aus LL / Zinsertrag / Zinsbetrag`
  2) `Bank/Post/Kasse / Forderungen aus LL / Zinsbetrag`

---

## 9) EINFLUSS AUF GEWINN & LIQUIDITÄT (falls gefragt)

> In Aufgaben kann stehen: Gewinn/Verlust (+ / −) und Liquiditätsgrad 2 (+ / − / 0 / X).

### 9.1 Gewinn/Verlust (Erfolg)
- **Aufwand steigt** → Gewinn **−**
- **Aufwand sinkt** → Gewinn **+**
- **Ertrag steigt** → Gewinn **+**
- **Ertrag sinkt** (Rabatt, Skonto bei Verkauf, Verluste Forderungen) → Gewinn **−**

### 9.2 Liquidität (Geld)
- **Bank/Post/Kasse steigt** → Liquidität **+**
- **Bank/Post/Kasse sinkt** → Liquidität **−**
- Nur Forderungen/Verbindlichkeiten ändern (ohne Geld) → Liquidität oft **0**
- Wenn Aufgabe Zahlen fehlen → **X**

---

## 10) “WO SCHREIBE ICH WAS HIN?” (prüfungspraktisch)

### 10.1 Wenn nur “Buchungssätze” gefragt sind
- Schreibe nur: `Soll / Haben / Betrag` (jede Buchung neue Zeile)

### 10.2 Wenn T-Konten gefordert sind
- Nach jedem Buchungssatz zusätzlich “Posting”
- Beispiel-Form (nur Format):
  - `Posting: Bank -> Soll (links) +500`
  - `Posting: Forderungen aus LL -> Haben (rechts) +500`

### 10.3 Wenn Abschluss / ER / Bilanz gefordert ist
- Erst Buchungen.
- Dann:
  - `Saldo Konto X = ...`
  - `ER: ...`
  - `Bilanz: ...`
- Wenn “Verluste Forderungen” vorkommt: in ER als **Minus** auf Ertragsseite zeigen.

---

## 11) FEHLERFALLEN (Punkte-Killer)

- Rabatt/Skonto **nach Zahlung** fälschlich als Umkehrbuchung.
- Bei Einkauf/Verkauf Konten vertauscht (Ford vs Verb).
- Skonto als Zins: falsche Tage (immer **Nettofrist - Skontofrist**).
- Teilzahlung: Rest vergessen abzuschreiben.
- Betreibung: Kostenvorschuss nicht in Forderungen einbezogen.
- MERKE ignoriert: Forderungen nicht über “Abschreibungen” abschreiben.

---
