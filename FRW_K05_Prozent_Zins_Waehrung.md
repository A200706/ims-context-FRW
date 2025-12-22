# FRW_K05_Prozent_Zins_Waehrung.md

> Zweck: Schnell-Context für AI. Kapitel 5 aus dem Upload: Prozentrechnen (inkl. vermind./vermehrter Grundwert), Prozentsatz als Bruch, Einstieg Zinsrechnen (Begriffe).  
> Stil: kurz, prüfungsnah, einfache Wörter (A2–B1), **Antwort-Only**.

---

## 0) OUTPUT MODE (STRICT)

### 0.1 Antwort-Regel (immer)
- **Kein Intro. Keine langen Erklärungen.**
- Starte immer so:
  - `Aufgabe {Nr}: {Kurzname}`
- Dann **nur** das, was man in die Lösung schreibt: Zahl/Einheit, evtl. 1 Formelzeile.

### 0.2 Rechner-Format
- Brüche als Text: `1/2`, `3/4`, `2/5`
- Prozent mit `%`
- Geld mit `CHF` (wie im Blatt)

### 0.3 “Wo schreibe ich das hin?”
- Wenn die Aufgabe **eine Zeile** hat: nur `Ergebnis: ...`
- Wenn die Aufgabe **Felder** hat (z.B. „Preis Jahr 20-2:“): schreibe das Ergebnis **direkt hinter das Feld**.
- Wenn die Aufgabe **Tabelle** hat: schreibe den Wert **in die passende Spalte** (Netto/Brutto/%).

### 0.4 Mini-Format-Bausteine (nur wenn nötig)
- `Gegeben: ...`
- `Gesucht: ...`
- `Formel: ...`
- `Rechnung: ...`
- `Ergebnis: ...`

---

## 1) RESPONSE TYPES (Index)

### RT-K05-1: Prozentsatz gesucht (p)
**Typ-Frage:** „Welchem Prozentsatz entspricht …?“  
**Output:**
- `Aufgabe {Nr}: Prozentsatz`
- `p = (100 * W) / G`
- `Ergebnis: p = ... %`

### RT-K05-2: Prozentwert gesucht (W)
**Typ-Frage:** „Wie viel CHF sind … % von …?“  
**Output:**
- `Aufgabe {Nr}: Prozentwert`
- `W = (G * p) / 100`
- `Ergebnis: W = ... (Einheit)`

### RT-K05-3: Grundwert gesucht (G)
**Typ-Frage:** „… sind … %; wie viel sind 100%?“  
**Output:**
- `Aufgabe {Nr}: Grundwert`
- `G = (100 * W) / p`
- `Ergebnis: G = ... (Einheit)`

### RT-K05-4: Verminderter Grundwert (unter 100%)
**Typ-Frage:** „Nach Abzug …% bleibt … CHF. Brutto?“  
**Output:**
- `Aufgabe {Nr}: Verminderter Grundwert`
- `Rest% = 100% - Abzug%`
- `100% = (100 * Restwert) / Rest%`
- `Ergebnis: Grundwert = ... CHF`

### RT-K05-5: Vermehrter Grundwert (über 100%)
**Typ-Frage:** „Nach Erhöhung …% ist es … CHF. Vorher?“  
**Output:**
- `Aufgabe {Nr}: Vermehrter Grundwert`
- `Neu% = 100% + Zuschlag%`
- `100% = (100 * Neuwert) / Neu%`
- `Ergebnis: Grundwert = ... CHF`

### RT-K05-6: Kettenänderung (mehrere % nacheinander)
**Typ-Frage:** „Erst +15%, dann −30%“  
**Output (Dreisatz oder Faktor, beides ok):**
- `Aufgabe {Nr}: Kettenänderung`
- Variante Dreisatz:
  - `nach +15%: 115% = ...`
  - `nach −30%: 70% von neu = ...`
- Variante Faktor (kurz):
  - `neu = alt * 1.15`
  - `aktion = neu * 0.70`
- `Ergebnis: ...`

### RT-K05-7: Prozentsatz als Bruch (für MC / Kontrolle)
**Typ-Frage:** „Schreibe …% als Bruch“ oder „Kontrolle“  
**Output:**
- `Aufgabe {Nr}: Prozent als Bruch`
- `...% = .../100 = (gekürzt) = a/b`
- `Ergebnis: a/b`

### RT-K05-8: Zinsrechnen (nur Begriffe im Upload)
**Wichtig:** Im Upload sind bei 5.3 vor allem **Begriffe** (Z, K, p, t) und das **360-Tage-Jahr** erwähnt.  
**Output (wenn nur Begriffe gefragt):**
- `Aufgabe {Nr}: Zinsgrössen`
- `Z = Zins (CHF), K = Kapital (CHF), p = Zinssatz (%/Jahr), t = Laufzeit (Tage)`
- `Hinweis: oft 360 Tage/Jahr`

---

## 2) KAPITEL 5.2 PROZENTRECHNEN (Kern)

### 2.1 Grundbegriffe (immer kennen)
- **Grundwert (G)** = 100% (absolute Zahl)
- **Prozentsatz (p)** = % (relative Zahl)
- **Prozentwert (W)** = Teil vom Grundwert (absolute Zahl)

### 2.2 Standard-Formeln (High ROI)
- `p = (100 * W) / G`
- `W = (G * p) / 100`
- `G = (100 * W) / p`

### 2.3 Dreisatz-Template (wie im Heft)
**Regel:** Gleiche Einheiten untereinander, gleiche Spalte.
- Wenn `100% = G`, dann:
  - `p% = W`
- Rechnen:
  - `W = (G * p) / 100`

**Wenn 1% gebraucht:**
- `1% = G / 100`
- `p% = 1% * p`

### 2.4 Typische Aufgabenmuster (aus Übungen)
**Muster A: „Welchem Prozentsatz entspricht CHF …?“**
- RT-K05-1

**Muster B: „Teuerungszulage 1.5% von Lohn“**
- RT-K05-2

**Muster C: „Abzüge sind 11.5%; wie viel CHF?“**
- RT-K05-2 (W gesucht)

---

## 3) 5.2.2 PROZENTSATZ ALS BRUCH (MC / Kontrolle)

### 3.1 Idee
- Prozent = „von 100“
- `p% = p/100` und dann **kürzen**

### 3.2 Häufige Umwandlungen (rechnerfreundlich)
- `50% = 50/100 = 1/2`
- `25% = 25/100 = 1/4`
- `75% = 75/100 = 3/4`
- `20% = 20/100 = 1/5`
- `10% = 10/100 = 1/10`
- `5% = 5/100 = 1/20`
- `12.5% = 12.5/100 = 1/8` (wenn erlaubt; sonst als Dezimal)

**Output immer als:** `Ergebnis: a/b`

---

## 4) 5.2.3 VERMINDERTER & VERMEHRTER GRUNDWERT (Prüfungs-Magnet)

### 4.1 Begriffe
- **Verminderter Grundwert**: Wert **< 100%** (nach Abzug)
- **Vermehrter Grundwert**: Wert **> 100%** (nach Zuschlag)

### 4.2 Standard-Schrittfolge (immer gleich)
**Vermindert:**
1) `Rest% = 100% - Abzug%`
2) `100% = (100 * Restwert) / Rest%`

**Vermehrt:**
1) `Neu% = 100% + Zuschlag%`
2) `100% = (100 * Neuwert) / Neu%`

### 4.3 Output-Template (wie Lösungen, kurz)
- `Aufgabe {Nr}: Verminderter Grundwert`
- `Rest% = ... %`
- `100% = (100 * ... ) / ...`
- `Ergebnis: ... CHF`

oder

- `Aufgabe {Nr}: Vermehrter Grundwert`
- `Neu% = ... %`
- `100% = (100 * ... ) / ...`
- `Ergebnis: ... CHF`

### 4.4 Kontroll-Check (1 Zeile)
- Vermindert: Ergebnis (100%) muss **größer** sein als Restwert.
- Vermehrt: Ergebnis (100%) muss **kleiner** sein als Neuwert.

---

## 5) KETTENÄNDERUNGEN (z.B. Preis +15%, dann −30%)

### 5.1 Wichtig
- Prozent nacheinander = **nicht addieren**
- Erst Änderung 1, dann Änderung 2 auf dem neuen Wert.

### 5.2 Output-Template (kurz)
- `Aufgabe {Nr}: Kettenänderung`
- `Preis alt = (100 * Preis neu) / (100% + p1%)`  (wenn „neu“ gegeben)
- `Preis Aktion = Preis neu * (100% - p2%) / 100`
- `Ergebnis: Preis alt = ... CHF; Preis Aktion = ... CHF`

Oder Faktor-Variante:
- `Preis neu = Preis alt * 1.xx`
- `Preis Aktion = Preis neu * 0.xx`
- `Ergebnis: ...`

---

## 6) 5.3 ZINSRECHNEN (nur das, was im Upload steht)

### 6.1 Definition (kurz)
- Zins = Geld für geliehenes Kapital in einer Zeit.

### 6.2 Vier Grössen (merken)
- `Z` = Zins in CHF (oft gesucht)
- `K` = Kapital in CHF
- `p` = Zinssatz in % (meist pro Jahr)
- `t` = Laufzeit in Tagen

### 6.3 Zeit-Regel (steht im Upload)
- Oft: `360 Tage = 1 Jahr`
- Manchmal: `90 Tage = 1 Quartal`

### 6.4 Wenn im Test eine Zins-Aufgabe kommt
- Wenn im Blatt eine Formel steht: **genau diese nutzen**
- Wenn nur Begriffe gefragt: RT-K05-8

> Hinweis (sauber): Im Kapitel-5-Upload ist bei 5.3 vor allem der Begriffsteil sichtbar. Wenn der Test Zins-Berechnungen verlangt, fehlt hier die Formel-Seite im Upload.

---

## 7) FEHLERFALLEN (die dummen Punkte-Killer)

- % und CHF vertauscht (p vs W).
- Bei vermindert/vermehrt falsche Prozentbasis (Rest% / Neu%).
- Bei Kettenänderung Prozente addiert (falsch).
- Ergebnis ohne Einheit (% / CHF).
- Dreisatz-Spalten gemischt (Einheiten nicht untereinander).

---

## 8) MINI-CHECKLISTE (10 Sekunden vor Abgabe)
- Was ist gesucht? `p` / `W` / `G`
- Basis richtig? 100% oder Rest% oder Neu%
- Einheit dran? `%` oder `CHF`
- Plausibel? (vermindert: 100% > Restwert; vermehrt: 100% < Neuwert)
