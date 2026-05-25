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

## 1) MWST-Steuersätze

- 8.1% = Normalsatz (Waren, DL, AV)
- 2.6% = Reduziert (Nahrungsmittel, Bücher, Medikamente, Wasser in Leitungen)
- 3.8% = Beherbergung (Hotels)

---

## 2) MWST-Berechnungsformeln (intern — NICHT anzeigen)

Brutto → Netto: `Netto = Brutto / (100 + Rate) × 100`
Brutto → MWST: `MWST = Brutto / (100 + Rate) × Rate`
Netto → MWST: `MWST = Netto × Rate / 100`
Rundung: auf 5 Rappen → `ROUND(Betrag × 20) / 20`

⚠️ NIEMALS Bruttobetrag direkt als MWST verwenden.

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
$\text{Ford aus LL} / \text{Umsatzsteuer 2200} \quad \text{[MWST]}$

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
$\text{Umsatzsteuer} / \text{Bank oder Post} \quad \text{[Restschuld]}$

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
$\text{Ford aus LL} / \text{Umsatzsteuer} \quad \text{[MWST]}$

Offene Lieferantenrechnungen:
$\text{Aufwandkonto} / \text{Verb aus LL} \quad \text{[Netto]}$
$\text{VST} / \text{Verb aus LL} \quad \text{[MWST]}$

Wiedereröffnung 01.01.: Umbuchungen umkehren.

---

## 14) Forderungsverlust Offenposten

$\text{Verluste Ford} / \text{Ertragskonto} \quad \text{[Netto]}$
Keine MWST-Korrektur (MWST wurde nie gebucht — vereinnahmtes Entgelt).

---

## 15) Häufige Fehler

1. ❌ MWST auf Versicherung/Zinsen/Löhne
2. ❌ Brutto als Netto verwenden
3. ❌ VST 1170 für AV-Kauf (→ 1171)
4. ❌ Bei Offenposten Rechnung buchen (→ KB)
5. ❌ VST bei Saldosteuersatz
6. ❌ Saldosteuersatz auf Netto (→ Brutto)
7. ❌ Rundung vergessen (→ 5 Rappen)
8. ❌ Skonto nur auf Netto (→ Netto UND MWST)
9. ❌ Berechnungen zeigen wenn nicht verlangt
10. ❌ Text ausserhalb von $...$
