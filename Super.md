# SUPER-MD — KAP 4 (MWST) & KAP 11 (Offenposten-Buchhaltung)
# FRW — Buchungssätze & MWST-Logik (LaTeX-SAFE)

---

## 0) Output-Style (LaTeX-SAFE)

- Jede Ausgabelinie: beginnt mit `$`, endet mit `$`
- Nummerierung IN LaTeX: `\text{1) }`
- Kontonamen in `\text{...}`, Trennung mit ` / `
- Betrag am Ende: `\quad 15'000.00`
- Tausender mit Apostroph: `15'000.00`
- Folgender BS gleicher Nr.: `$\quad\; \text{Soll} / \text{Haben} \quad ...$`
- KB = `$\text{n) } \text{KB}$`
- **NUR ausgeben was die Aufgabe verlangt. Keine Berechnungen zeigen, ausser explizit verlangt.**

### Beispiel (Buch-Stil):
$\text{1) } \text{Warenaufwand} / \text{Verb aus LL} \quad 10'000.00$
$\quad\; \text{VST 1170} / \text{Verb aus LL} \quad 810.00$
$\text{2) } \text{Ford aus LL} / \text{Warenertrag} \quad 18'000.00$
$\quad\; \text{Ford aus LL} / \text{Umsatzsteuer 2200} \quad 1'458.00$
$\text{3) } \text{Versicherungsaufwand} / \text{Bank} \quad 3'200.00$

---

## 1) MWST-Steuersätze (EXAKTE Divisoren)

| Satz | Divisor (Brutto→Netto) | Formel Netto | Formel MWST |
|------|------------------------|--------------|------------|
| **8.1%** | ÷ 108.1 × 100 | `Brutto ÷ 108.1 × 100` | `Brutto ÷ 108.1 × 8.1` |
| **2.6%** | ÷ 102.6 × 100 | `Brutto ÷ 102.6 × 100` | `Brutto ÷ 102.6 × 2.6` |
| **3.8%** | ÷ 103.8 × 100 | `Brutto ÷ 103.8 × 100` | `Brutto ÷ 103.8 × 3.8` |

### Berechnungsbeispiele (intern, NICHT anzeigen):

**8.1% auf CHF 16'215:**
- Netto = 16'215 ÷ 108.1 × 100 = **15'000.00**
- MWST = 16'215 ÷ 108.1 × 8.1 = **1'215.00**

**2.6% auf CHF 2'052:**
- Netto = 2'052 ÷ 102.6 × 100 = **2'000.00**
- MWST = 2'052 ÷ 102.6 × 2.6 = **52.00**

**⚠️ KRITISCH: 2.6% bedeutet ÷102.6 (NICHT ÷1.026!)**
- Falsch: 2'052 ÷ 1.026 = 2'002 (falsch!)
- Richtig: 2'052 ÷ 102.6 × 100 = 2'000 (korrekt!)

---

## 2) MWST-Berechnung Schritt-für-Schritt

**Bei "inkl. X% MWST":**

1. **Rate erkennen:** 8.1% → 108.1 | 2.6% → 102.6 | 3.8% → 103.8
2. **Brutto durch Rate teilen:** `Brutto ÷ Divisor`
3. **× 100 für Netto** (oder × Satz für MWST)
4. **Auf 5 Rappen runden:** `ROUND(Betrag × 20) / 20`

---

## 3) Vorsteuer-Kontenzuordnung

- **VST 1170** → Warenaufwand, Materialaufwand, Energieaufwand (Kontenklasse 4)
- **VST 1171** → Sonstiger BetriebsAu (KK 5–8), Anlagevermögen-Käufe
- **UMST 2200** → Umsatzsteuer auf Verkäufe / Erträge

---

## 4) Effektive Methode + Nettomethode

**Einkauf auf Rechnung:**
$\text{Aufwandkonto} / \text{Verb aus LL} \quad \text{[Netto]}$
$\text{VST 1170 oder 1171} / \text{Verb aus LL} \quad \text{[MWST]}$

**Verkauf auf Rechnung:**
$\text{Ford aus LL} / \text{Ertragskonto} \quad \text{[Netto]}$
$\text{Ford aus LL} / \text{Umsatzsteuer 2200} \quad \text{[MWST]$

**Bar:** Kasse statt Ford/Verb aus LL.

---

## 5) Effektive Methode + Bruttomethode

Einkauf: `Aufwandkonto 8.1% / Verb aus LL [Brutto]`
Verkauf: `Ford aus LL / Ertragskonto 8.1% [Brutto]`

Periodenende VST: `VST 1170 / Aufwandkonto 8.1%` + `VST 1171 / Aufwandkonto 8.1%`
Periodenende UMST: `Ertragskonto 8.1% / Umsatzsteuer`

---

## 6) Saldosteuersatzmethode

- Bruttomethode, keine VST-Buchung, halbjährliche Abrechnung
- `Ertragskonto / Umsatzsteuer [Saldosteuersatz × Umsatz]`
- `Umsatzsteuer / Bank [gleicher Betrag]`
- ⚠️ Basis = Brutto-Ertragssaldo (100%), NICHT 108.1%

---

## 7) MWST-Abrechnung ESTV

$\text{Umsatzsteuer} / \text{VST 1170} \quad \text{[Saldo]}$
$\text{Umsatzsteuer} / \text{VST 1171} \quad \text{[Saldo]}$
$\text{Umsatzsteuer} / \text{Bank oder Post} \quad \text{[Restschuld]$

---

## 8) Rücksendungen, Rabatte, Skonti

**Nettomethode:** Die 2 Buchungssätze der Rechnung werden umgekehrt.

Kundenrabatt/-skonto:
$\text{Ertragskonto} / \text{Ford aus LL} \quad \text{[Netto-Red.]}$
$\text{Umsatzsteuer} / \text{Ford aus LL} \quad \text{[MWST-Red.]}$

Lieferantenrabatt/-skonto:
$\text{Verb aus LL} / \text{Aufwandkonto} \quad \text{[Netto-Red.]}$
$\text{Verb aus LL} / \text{VST} \quad \text{[MWST-Red.]}$

Zahlung nach Skonto (3 BS): Skonto-Netto + Skonto-MWST + Zahlbetrag

---

## 9) MWST-Ausnahmen

| Typ | UMST? | VST? | Beispiele |
|-----|-------|------|-----------|
| **Ausgenommen** | Nein | Nein | Versicherungen, Miete Wohnungen, Zinsen, Bankspesen, Ärzte |
| **Befreit** | Nein | **Ja** | Exporte |
| **Kein Bezug** | — | — | Löhne, Gehälter |

→ Einfach: `Aufwandkonto / Bank [Bruttobetrag]` — keine MWST-Zeile.

---

## 10) AV-Kauf/-Verkauf & Kreditkarten

AV-Kauf: `AV-Konto / ... [Netto]` + `VST 1171 / ... [MWST]`
AV-Verkauf: `... / AV-Konto [Buchwert]` + `... / Umsatzsteuer [MWST]`
KK-Einnahmen: `Kk und Dk / Ertrag [Netto]` + `Kk und Dk / UMST [MWST]`
KK-Gutschrift: `Bank / Kk und Dk [Gutschrift]` + `Finanzaufwand / Kk und Dk [Kommission]`

---

# ═══════════════════════════════════════
# KAP 11 — OFFENPOSTEN-BUCHHALTUNG
# ═══════════════════════════════════════

## 11) Kernregel

> Rechnungen = **KB** (Kein Buchungssatz). Buchung erst bei **Zahlung**.

---

## 12) Buchung bei Zahlung (Offenposten + Nettomethode)

Kundenzahlung: `Bank / Ertragskonto [Netto]` + `Bank / Umsatzsteuer [MWST]`
Lieferantenzahlung: `Aufwandkonto / Bank [Netto]` + `VST / Bank [MWST]`
Mit Skonto: Netto−Skonto und MWST−Skonto direkt buchen.

---

## 13) Jahresabschluss Offenposten (31.12.)

Offene Kundenrechnungen:
$\text{Ford aus LL} / \text{Ertragskonto} \quad \text{[Netto]}$
$\text{Ford aus LL} / \text{Umsatzsteuer} \quad \text{[MWST]$

Offene Lieferantenrechnungen:
$\text{Aufwandkonto} / \text{Verb aus LL} \quad \text{[Netto]}$
$\text{VST} / \text{Verb aus LL} \quad \text{[MWST]$

Wiedereröffnung 01.01.: Umbuchungen umkehren.

---

## 14) Forderungsverlust Offenposten

$\text{Verluste Ford} / \text{Ertragskonto} \quad \text{[Netto]}$
Keine MWST-Korrektur (MWST wurde nie gebucht — vereinnahmtes Entgelt).

##  Kontobezeichnungen & Abkürzungen

| Abkürzung | Vollständig | Konto-Nr. |
|---|---|---|
| VST 1170 | Vorsteuer Material/Waren/DL/Energie | 1170 |
| VST 1171 | Vorsteuer Investitionen/übriger Aufwand | 1171 |
| UMST 2200 | Umsatzsteuer | 2200 |
| Ford aus LL | Forderungen aus Lieferungen und Leistungen | 1100 |
| Verb aus LL | Verbindlichkeiten aus Lieferungen und Leistungen | 2000 |
| MaterialAu | Materialaufwand | KK4 |
| WarenAu | Warenaufwand | KK4 |
| WarenEr | Warenertrag | KK3 |
| ProdER | Produktionserlöse | KK3 |
| TransportEr | Transportertrag | KK3 |
| HonorarEr | Honorarertrag | KK3 |
| VerwAu / VerwaltungsAu | Verwaltungsaufwand | KK6 |
| EnergieAu LeistErst | Energieaufwand zur Leistungserstellung | KK4 |
| FahrzeugAu | Fahrzeugaufwand | KK6 |
| RaumAu | Raumaufwand | KK6 |
| FinanzAu | Finanzaufwand | KK6/8 |
| SonstBetrAu | Sonstiger Betriebsaufwand | KK5-8 |
| Kk und Dk | Kreditkarten und Debitkarten | 1045 |
| Abschr | Abschreibungen | KK6 |
| URE | Unterhalt und Reparaturen | KK6 |
| WarenBest | Warenbestand | KK1 |
| AU | Aufwand (generisch) | — |


---

## 15) Häufige Fehler

1. ❌ MWST auf Versicherung/Zinsen/Löhne
2. ❌ Brutto als Netto verwenden
3. ❌ **2.6% falsch berechnen (÷1.026 statt ÷102.6)**
4. ❌ VST 1170 für AV-Kauf (→ 1171)
5. ❌ Bei Offenposten Rechnung buchen (→ KB)
6. ❌ VST bei Saldosteuersatz
7. ❌ Saldosteuersatz auf Netto (→ Brutto)
8. ❌ Rundung vergessen (→ 5 Rappen)
9. ❌ Skonto nur auf Netto (→ Netto UND MWST)
10. ❌ Berechnungen zeigen wenn nicht verlangt
11. ❌ Text ausserhalb von $...$
