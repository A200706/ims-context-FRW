  # FRW_K08_MWST.md
> Zweck: Schnell-Context für AI. Kapitel 8 aus dem Upload: Mehrwertsteuer (MWST) Theorie und Aufgaben.
> Stil: kurz, prüfungsnah, einfache Wörter (A2–B1), **Antwort-Only**.

---

## 0) OUTPUT MODE (STRICT)

### 0.1 Antwort-Regel (immer)
- **Kein Intro. Keine langen Erklärungen.**
- Starte immer so:
  - `Aufgabe {Nr}: {Kurzname}`
- Dann **nur** das, was man in die Lösung schreibt: Zahl/Einheit, evtl. 1 Formelzeile.

### 0.2 Rechner-Format
- Beträge in `CHF`
- Prozentsätze mit `%`
- Steuersätze als Dezimalzahlen (z.B., `8.1%`)

### 0.3 "Wo schreibe ich das hin?"
- Wenn die Aufgabe **eine Zeile** hat: nur `Ergebnis: ...`
- Wenn die Aufgabe **Felder** hat (z.B. „MWST-Betrag:“): schreibe das Ergebnis **direkt hinter das Feld**.
- Wenn die Aufgabe **Tabelle** hat: schreibe den Wert **in die passende Spalte** (Netto/Brutto/%).

### 0.4 Mini-Format-Bausteine (nur wenn nötig)
- `Gegeben: ...`
- `Gesucht: ...`
- `Formel: ...`
- `Rechnung: ...`
- `Ergebnis: ...`

---

## 1) RESPONSE TYPES (Index)

### RT-K08-1: MWST-Betrag berechnen
**Typ-Frage:** „Berechnen Sie die MWST für einen Betrag von CHF X.“ oder „Wie hoch ist die MWST für CHF X?“
**Output:**
- `Aufgabe {Nr}: MWST-Betrag`
- `MWST = Betrag * Steuersatz`
- `Ergebnis: MWST = ... CHF`

### RT-K08-2: Bruttobetrag berechnen
**Typ-Frage:** „Wie hoch ist der Bruttobetrag inkl. MWST?“
**Output:**
- `Aufgabe {Nr}: Bruttobetrag`
- `Bruttobetrag = Nettobetrag * (1 + Steuersatz)`
- `Ergebnis: Bruttobetrag = ... CHF`

### RT-K08-3: Nettobetrag berechnen
**Typ-Frage:** „Wie hoch ist der Nettobetrag exkl. MWST?“
**Output:**
- `Aufgabe {Nr}: Nettobetrag`
- `Nettobetrag = Bruttobetrag / (1 + Steuersatz)`
- `Ergebnis: Nettobetrag = ... CHF`

### RT-K08-4: Vorsteuerabzug
**Typ-Frage:** „Wie hoch ist der Vorsteuerabzug?“
**Output:**
- `Aufgabe {Nr}: Vorsteuerabzug`
- `Vorsteuer = Eingangsrechnung * Steuersatz`
- `Ergebnis: Vorsteuer = ... CHF`

### RT-K08-5: MWST-Abrechnung
**Typ-Frage:** „Berechnen Sie die abzuliefernde MWST.“
**Output:**
- `Aufgabe {Nr}: MWST-Abrechnung`
- `Abzuliefernde MWST = Umsatzsteuer - Vorsteuer`
- `Ergebnis: Abzuliefernde MWST = ... CHF`

### RT-K08-6: Steuersatz bestimmen
**Typ-Frage:** „Welcher Steuersatz gilt für ...?“
**Output:**
- `Aufgabe {Nr}: Steuersatz`
- `Steuersatz = ... %`
- `Ergebnis: ... %`

### RT-K08-7: MWST-konformer Beleg
**Typ-Frage:** „Ist dieser Beleg MWST-konform? Fehlende Elemente?“
**Output:**
- `Aufgabe {Nr}: MWST-konformer Beleg`
- `Fehlende Elemente: Name und Adresse des Leistenden, MWST-Nummer, Datum der Leistung, Art und Umfang der Leistung, Entgelt für die Leistung, Steuersatz und Steuerbetrag`
- `Ergebnis: Fehlende Elemente: ...`

---

## 2) KAPITEL 8.1 & 8.2 MWST-GRUNDLAGEN (Kern)

### 2.1 Grundbegriffe (immer kennen)
- **Steuersubjekt**: Unternehmen, die MWST abrechnen müssen.
- **Steuerobjekt**: Steuerpflichtige Umsätze (Lieferungen und Dienstleistungen).
- **Vorsteuer**: MWST auf Einkäufen (kann zurückgefordert werden).
- **Umsatzsteuer**: MWST auf Verkäufen (muss an ESTV abgeführt werden).

### 2.2 Steuersätze
- **Normalsatz**: `8.1%`
- **Reduzierter Satz**: `2.6%` (z.B. Nahrungsmittel, Medikamente)
- **Sondersatz**: `3.8%` (z.B. Hotellerie für Übernachtung und Frühstück)
- **Von der Steuer befreit**: Exporte (Vorsteuerabzug erlaubt)
- **Von der Steuer ausgenommen**: z.B. Versicherungen, Geld- und Kapitalverkehr (kein Vorsteuerabzug erlaubt)

### 2.3 Standard-Formeln (High ROI)
- `MWST = Nettobetrag * Steuersatz`
- `Bruttobetrag = Nettobetrag * (1 + Steuersatz)`
- `Nettobetrag = Bruttobetrag / (1 + Steuersatz)`

---

## 3) TYPISCHE AUFGABENMUSTER

### 3.1 MWST-Berechnung
**Muster A: „Berechnen Sie die MWST für CHF X.“**
- RT-K08-1

**Muster B: „Wie hoch ist der Bruttobetrag?“
- RT-K08-2

**Muster C: „Wie hoch ist der Nettobetrag?“
- RT-K08-3

### 3.2 Vorsteuer und Umsatzsteuer
**Muster D: „Berechnen Sie die Vorsteuer.“**
- RT-K08-4

**Muster E: „Berechnen Sie die abzuliefernde MWST.“**
- RT-K08-5

---

## 4) MWST-KONFORME BELEGE

### 4.1 Pflichtangaben
- Name und Adresse des Leistenden
- MWST-Nummer des Leistenden
- Name und Adresse des Empfängers
- Datum der Leistung
- Art und Umfang der Leistung
- Entgelt für die Leistung
- Steuersatz und Steuerbetrag

---

## 5) BUCHUNG DER MWST (NETTOMETHODE)

### 5.1 Konten
- **Vorsteuer 1170**: Vorsteuer aus Material, Waren, Dienstleistungen
- **Vorsteuer 1171**: Vorsteuer aus Investitionen und übrigem Betriebsaufwand
- **Umsatzsteuer**: Umsatzsteuer aus Verkäufen

### 5.2 Buchungssätze
- **Einkauf**: `Materialaufwand / Vorsteuer 1170`
- **Verkauf**: `Forderungen aus LL / Umsatzsteuer`

---

## 6) SALDOSTEUERSATZMETHODE

### 6.1 Anwendung
- Für Unternehmen mit Jahresumsatz bis CHF 5,024,000
- Abrechnung halbjährlich

### 6.2 Berechnung
- `MWST-Schuld = (Steuerbarer Gesamtumsatz * Saldosteuersatz) / 100`

---

## 7) FEHLERFALLEN
- Verwechslung von Vorsteuer und Umsatzsteuer.
- Falsche Anwendung der Steuersätze.
- Fehlende Angaben auf Belegen.
- Falsche Berechnung der abzuliefernden MWST.

---

## 8) MINI-CHECKLISTE
- Steuersubjekt und Steuerobjekt korrekt identifiziert?
- Richtiger Steuersatz angewendet?
- Vorsteuerabzug korrekt berechnet?
- Beleg enthält alle Pflichtangaben?
- Buchungssätze korrekt?

---

## 9) BEISPIELE AUS DEN AUFGABEN

### Beispiel 1: MWST-Berechnung
**Frage:** „Berechnen Sie die MWST für einen Betrag von CHF 1000.“
**Antwort:**
