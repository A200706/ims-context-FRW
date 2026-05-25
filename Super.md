# SUPER-MD — KAP 4 (MWST) & KAP 11 (Offenposten-Buchhaltung)
# Finanzielle Rechnungslegung (FRW) — Buchungssätze & MWST-Logik

---

## 0) Output-Style (LaTeX-SAFE)

Wenn ein Viewer LaTeX nur dann rendert, wenn die ZEILE komplett LaTeX ist, benutze dieses Template:

- Jede Ausgabelinie ist GENAU ein LaTeX-Block:
  - beginnt mit `$`
  - endet mit `$`
- Nummerierung steht IN LaTeX:
  - `\text{1) }`, `\text{2) }`, ...
- Kontonamen, Wörter, Hinweise IMMER in `\text{...}`
- Buchungssätze mit `/` trennen: `\text{Soll} / \text{Haben}`
- Beträge als Zahlen mit Apostroph-Tausender: `15'000.00`
- Beträge am Ende mit `\quad`: `\quad 15'000.00`
- Hinweise am Ende als `\text{[| ...]}`
- Maximal 1 Buchungssatz pro Zeile
- **KB** = Kein Buchungssatz: `$\text{KB}$`

### Beispiel Ausgabe (Nettomethode, Einkauf inkl. 8.1%)

$\text{Berechnung:}$
$\text{Netto} = 16'215 \div 108.1 \times 100 = 15'000.00$
$\text{MWST} = 16'215 \div 108.1 \times 8.1 = 1'215.00$

$\text{1) } \text{Warenaufwand} / \text{Verb aus LL} \quad 15'000.00$
$\text{1) } \text{VST 1170} / \text{Verb aus LL} \quad 1'215.00$

### Beispiel Ausgabe (Offenposten — Rechnung erhalten)

$\text{1) KB} \quad \text{[| Offenposten: Buchung erst bei Zahlung]}$

### Beispiel Ausgabe (Ausgenommene Leistung)

$\text{3) } \text{Versicherungsaufwand} / \text{Bank} \quad 3'200.00 \quad \text{[| ausgenommen, keine MWST]}$

---

## 1) MWST-Steuersätze

| Satz   | Rate   | Anwendung                                    |
|--------|--------|----------------------------------------------|
| Normal | 8.1%   | Standard (Waren, DL, Anlagevermögen)         |
| Reduz. | 2.6%   | Nahrungsmittel, Bücher, Zeitungen, Medikamente |
| Sonder | 3.8%   | Beherbergung (Hotels)                        |

---

## 2) MWST-Berechnungsformeln (KRITISCH — ANTI-FEHLER)

### Brutto → Netto & MWST:
```
Netto = Brutto / (100 + Rate) × 100
MWST  = Brutto / (100 + Rate) × Rate
```
Beispiel: CHF 10'810 inkl. 8.1%
→ Netto = 10'810 / 108.1 × 100 = 10'000
→ MWST  = 10'810 / 108.1 × 8.1  = 810

### Netto → MWST:
```
MWST = Netto × Rate / 100
```

### 5-Rappen-Rundung:
```
Gerundet = ROUND(Betrag × 20) / 20
```

⚠️ **NIEMALS** den Bruttobetrag direkt als MWST-Basis verwenden!
⚠️ **IMMER** zuerst Netto berechnen, dann MWST daraus ableiten.

---

## 3) Vorsteuer-Kontenzuordnung

| Konto      | Zuordnung                                          |
|------------|-----------------------------------------------------|
| **VST 1170** | Materialaufwand, Warenaufwand, Energieaufwand (KK 4) |
| **VST 1171** | Sonstiger BetriebsAu (KK 5–8), Anlagevermögen-Käufe |
| **UMST 2200** | Umsatzsteuer auf Verkäufe / Erträge                |

---

## 4) Quick Router — KAP 4 Methoden

### A) Effektive Methode + Nettomethode (Standard)

**Einkauf auf Rechnung (inkl. MWST):**
$\text{Aufwandkonto} / \text{Verb aus LL} \quad \text{[Netto]}$
$\text{VST 1170 oder 1171} / \text{Verb aus LL} \quad \text{[MWST]}$

**Verkauf auf Rechnung (inkl. MWST):**
$\text{Ford aus LL} / \text{Ertragskonto} \quad \text{[Netto]}$
$\text{Ford aus LL} / \text{Umsatzsteuer 2200} \quad \text{[MWST]}$

**Barkauf / Barverkauf:** Gleich, aber Kasse statt Ford/Verb aus LL.

### B) Effektive Methode + Bruttomethode

**Einkauf:** `Aufwandkonto 8.1% / Verb aus LL [Brutto]`
**Verkauf:** `Ford aus LL / Ertragskonto 8.1% [Brutto]`

**Periodenende — VST ausbuchen:**
$\text{VST 1170} / \text{Aufwandkonto 8.1\%} \quad \text{[VST KK4]}$
$\text{VST 1171} / \text{Aufwandkonto 8.1\%} \quad \text{[VST KK5-8 + AV]}$

**Periodenende — UMST ausbuchen:**
$\text{Ertragskonto 8.1\%} / \text{Umsatzsteuer} \quad \text{[UMST]}$

### C) Saldosteuersatzmethode (+ Bruttomethode)

- Keine separate VST-Buchung, keine VST-Rückforderung
- Abrechnung: halbjährlich

**Periodenende:**
$\text{Ertragskonto} / \text{Umsatzsteuer} \quad \text{[Saldosteuersatz} \times \text{Umsatz]}$
$\text{Umsatzsteuer} / \text{Bank} \quad \text{[gleicher Betrag]}$

⚠️ Bei Saldosteuersatz: Umsatz = Saldo Ertragskonto (100%), NICHT 108.1%!

---

## 5) MWST-Abrechnung mit ESTV

$\text{Umsatzsteuer} / \text{VST 1170} \quad \text{[Saldo VST 1170]}$
$\text{Umsatzsteuer} / \text{VST 1171} \quad \text{[Saldo VST 1171]}$
$\text{Umsatzsteuer} / \text{Bank oder Post} \quad \text{[Restschuld]}$

---

## 6) Rücksendungen, Rabatte, Skonti MIT MWST

### Grundregel (Nettomethode):
> Die zwei Buchungssätze der Rechnung werden **umgekehrt** (Soll↔Haben).

**Kundenrabatt/-skonto (vorher Rechnung verbucht):**
$\text{Ertragskonto} / \text{Ford aus LL} \quad \text{[Netto-Reduktion]}$
$\text{Umsatzsteuer} / \text{Ford aus LL} \quad \text{[MWST-Reduktion]}$

**Lieferantenrabatt/-skonto (vorher Rechnung verbucht):**
$\text{Verb aus LL} / \text{Aufwandkonto} \quad \text{[Netto-Reduktion]}$
$\text{Verb aus LL} / \text{VST 1170 oder 1171} \quad \text{[MWST-Reduktion]}$

**Zahlung nach Skonto (Kunde):**
$\text{Ertragskonto} / \text{Ford aus LL} \quad \text{[Skonto Netto]}$
$\text{Umsatzsteuer} / \text{Ford aus LL} \quad \text{[Skonto MWST]}$
$\text{Bank} / \text{Ford aus LL} \quad \text{[Zahlbetrag]}$

**Zahlung nach Skonto (Lieferant):**
$\text{Verb aus LL} / \text{Aufwandkonto} \quad \text{[Skonto Netto]}$
$\text{Verb aus LL} / \text{VST 1170/1171} \quad \text{[Skonto MWST]}$
$\text{Verb aus LL} / \text{Bank} \quad \text{[Zahlbetrag]}$

---

## 7) MWST-Ausnahmen (KRITISCH)

| Typ                  | UMST? | VST-Abzug? | Beispiele                                   |
|----------------------|-------|------------|----------------------------------------------|
| **Ausgenommen** (Art. 21) | Nein  | Nein       | Versicherungen, Miete Wohnungen, Zinsen, Ärzte, Bildung |
| **Befreit** (Art. 23)     | Nein  | **Ja**     | Exporte, Lieferungen ins Ausland             |

→ Versicherungsprämien: kein VST, kein UMST → `Aufwandkonto / Verb aus LL [Brutto]`
→ Zinsen, Bankspesen: ausgenommen → `Finanzaufwand / Bank`
→ Löhne: kein MWST-Bezug → `Lohnaufwand / Bank`

---

## 8) Verkauf/Kauf von Anlagevermögen & Kreditkarten

**Kauf AV:** `AV-Konto / Kasse|Bank|Verb LL [Netto]` + `VST 1171 / ... [MWST]`
**Verkauf AV:** `Kasse|Bank|Ford LL / AV-Konto [Buchwert]` + `... / Umsatzsteuer [MWST]`

**Kreditkarten-Tageseinnahmen:** `Kk und Dk / Ertrag [Netto]` + `Kk und Dk / UMST [MWST]`
**KK-Gutschrift:** `Bank / Kk und Dk [Gutschrift]` + `Finanzaufwand / Kk und Dk [Kommission]`

---

# ═══════════════════════════════════════════
# KAP 11 — OFFENPOSTEN-BUCHHALTUNG
# ═══════════════════════════════════════════

## 9) Kernregel Offenposten

> **Rechnungen werden NICHT bei Erhalt/Versand gebucht, sondern NUR bei Zahlung.**

- Eingangsrechnung erhalten → **KB**
- Ausgangsrechnung versendet → **KB**
- Erst bei **Zahlung** wird gebucht

---

## 10) Buchung bei Zahlung (Offenposten + Nettomethode)

**Kundenzahlung:**
$\text{Bank} / \text{Ertragskonto} \quad \text{[Netto]}$
$\text{Bank} / \text{Umsatzsteuer} \quad \text{[MWST]}$

**Lieferantenzahlung:**
$\text{Aufwandkonto} / \text{Bank} \quad \text{[Netto]}$
$\text{VST 1170 oder 1171} / \text{Bank} \quad \text{[MWST]}$

**MIT Skonto (Offenposten):** Skonto direkt abgezogen — kein vorheriger Buchungssatz existiert!
$\text{Bank} / \text{Ertragskonto} \quad \text{[Netto} - \text{Skonto-Netto]}$
$\text{Bank} / \text{Umsatzsteuer} \quad \text{[MWST} - \text{Skonto-MWST]}$

---

## 11) Jahresabschluss — Offene Posten umbuchen

**Offene Kundenrechnungen (31.12.):**
$\text{Ford aus LL} / \text{Ertragskonto} \quad \text{[Netto]}$
$\text{Ford aus LL} / \text{Umsatzsteuer} \quad \text{[MWST]}$

**Offene Lieferantenrechnungen (31.12.):**
$\text{Aufwandkonto} / \text{Verb aus LL} \quad \text{[Netto]}$
$\text{VST 1170/1171} / \text{Verb aus LL} \quad \text{[MWST]}$

**Wiedereröffnung 01.01.:** Umbuchungen umkehren (Soll↔Haben).

---

## 12) Forderungsverlust bei Offenposten

Da keine Rechnung gebucht wurde → kein Ford-aus-LL-Saldo → Verlust direkt gegen Ertrag:
$\text{Verluste Ford} / \text{Ertragskonto} \quad \text{[Netto]}$

⚠️ Keine MWST-Korrektur nötig (MWST wurde nie gebucht — vereinnahmtes Entgelt).

---

## 13) Gelöste Musterbeispiele (LaTeX-Format)

### Beispiel A: Nettomethode — Einkauf

Warenrechnung CHF 10'810 (inkl. 8.1%) auf Rechnung:

$\text{Berechnung: Netto} = 10'810 \div 108.1 \times 100 = 10'000.00 \quad \text{MWST} = 810.00$
$\text{1) } \text{Warenaufwand} / \text{Verb aus LL} \quad 10'000.00$
$\text{1) } \text{VST 1170} / \text{Verb aus LL} \quad 810.00$

### Beispiel B: Nettomethode — Verkauf + 10% Rabatt + 2% Skonto

Verkauf CHF 30'808.50 (inkl. 8.1%) auf Rechnung. Dann 10% Rabatt, dann Zahlung −2% Skonto.

$\text{1) } \text{Ford aus LL} / \text{Produktionserlöse} \quad 28'500.00$
$\text{1) } \text{Ford aus LL} / \text{Umsatzsteuer} \quad 2'308.50$
$\text{2) } \text{Produktionserlöse} / \text{Ford aus LL} \quad 2'850.00 \quad \text{[| 10\% Rabatt Netto]}$
$\text{2) } \text{Umsatzsteuer} / \text{Ford aus LL} \quad 230.85 \quad \text{[| 10\% Rabatt MWST]}$
$\text{3) } \text{Produktionserlöse} / \text{Ford aus LL} \quad 513.00 \quad \text{[| 2\% Skonto Netto]}$
$\text{3) } \text{Umsatzsteuer} / \text{Ford aus LL} \quad 41.55 \quad \text{[| 2\% Skonto MWST]}$
$\text{3) } \text{Bank} / \text{Ford aus LL} \quad 27'173.10$

### Beispiel C: Offenposten — KB + Zahlung

Kundenrechnung CHF 6'756.25 (inkl. 8.1%) versendet. Zahlung mit 2% Skonto.

$\text{1) KB} \quad \text{[| Offenposten]}$
$\text{2) } \text{Bank} / \text{Transportertrag} \quad 6'125.00 \quad \text{[| 6'250} - \text{125 Skonto]}$
$\text{2) } \text{Bank} / \text{Umsatzsteuer} \quad 496.10 \quad \text{[| 506.25} - \text{10.15 Skonto]}$

### Beispiel D: Saldosteuersatzmethode

Honorarertrag CHF 138'000 (inkl. 8.1%), Saldosteuersatz 6.2%.

$\text{1) } \text{Honorarertrag} / \text{Umsatzsteuer} \quad 8'556.00 \quad \text{[| 6.2\%} \times \text{138'000]}$
$\text{2) } \text{Umsatzsteuer} / \text{Bank} \quad 8'556.00$

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

## 14) Häufige Fehler (ANTI-FEHLER-LISTE)

1. ❌ MWST auf Versicherungsprämien → **ausgenommen**
2. ❌ MWST auf Löhne/Zinsen/Bankspesen → **ausgenommen / kein Bezug**
3. ❌ Bruttobetrag als Netto verwenden → **IMMER Brutto → Netto umrechnen**
4. ❌ VST 1170 für AV-Kauf → AV geht auf **VST 1171**
5. ❌ Bei Offenposten Rechnung buchen → **KB!**
6. ❌ Bei Saldosteuersatz VST buchen → **Keine VST**
7. ❌ Saldosteuersatz auf Netto anwenden → Basis ist **Brutto (inkl. MWST)**
8. ❌ Rundung vergessen → **5-Rappen-Rundung**
9. ❌ Skonto nur auf Netto → Skonto auf **Netto UND MWST**
10. ❌ Nummerierung ausserhalb von `$...$` → **Verboten**
