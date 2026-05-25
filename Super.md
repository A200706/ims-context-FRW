# SUPER-MD — KAP 4 (MWST) & KAP 11 (Offenposten-Buchhaltung)
# Finanzielle Rechnungslegung (FRW) — Buchungssätze & MWST-Logik

---

## 0) Output-Style (Buchungssatz-Format)

Jede Lösung folgt diesem Template:

```
Nr. Buchungssatz                              Betrag
1   Soll-Konto / Haben-Konto                  XXXX.XX
    Soll-Konto / Haben-Konto                  XXXX.XX
```

- **Minimalistisch:** Kürzestmögliche Antwort, die noch vollständig ist.
- **KB** = "Kein Buchungssatz" (wenn keine Buchung nötig ist).
- Beträge IMMER auf **5 Rappen** runden.
- Kontonummern nur wenn im Aufgabentext verlangt.

---

## 1) MWST-Steuersätze (Stand aktuell im Lehrbuch)

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
Beispiel: CHF 10 810 inkl. 8.1%
→ Netto = 10 810 / 108.1 × 100 = 10 000
→ MWST  = 10 810 / 108.1 × 8.1  = 810

### Netto → MWST:
```
MWST = Netto × Rate / 100
```

### 5-Rappen-Rundung:
```
Gerundet = ROUND(Betrag × 20) / 20
```
Beispiel: 101.23 → 101.25 | 101.22 → 101.20

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
```
Aufwandkonto / Verb aus LL       [Nettobetrag]
VST 1170 oder 1171 / Verb aus LL [MWST-Betrag]
```

**Verkauf auf Rechnung (inkl. MWST):**
```
Ford aus LL / Ertragskonto       [Nettobetrag]
Ford aus LL / Umsatzsteuer 2200  [MWST-Betrag]
```

**Barkauf (inkl. MWST):**
```
Aufwandkonto / Kasse             [Nettobetrag]
VST 1170 oder 1171 / Kasse      [MWST-Betrag]
```

**Barverkauf (inkl. MWST):**
```
Kasse / Ertragskonto             [Nettobetrag]
Kasse / Umsatzsteuer 2200       [MWST-Betrag]
```

### B) Effektive Methode + Bruttomethode

**Einkauf:**
```
Aufwandkonto 8.1% / Verb aus LL  [Bruttobetrag]
```

**Verkauf:**
```
Ford aus LL / Ertragskonto 8.1%  [Bruttobetrag]
```

**Periodenende — VST ausbuchen:**
```
VST 1170 / Aufwandkonto 8.1%     [VST KK4]
VST 1171 / Aufwandkonto 8.1%     [VST KK5-8 + AV]
```

**Periodenende — UMST ausbuchen:**
```
Ertragskonto 8.1% / Umsatzsteuer [UMST-Betrag]
```

### C) Saldosteuersatzmethode (+ Bruttomethode)

- Keine separate VST-Buchung
- Keine VST-Rückforderung
- Abrechnung: halbjährlich (nicht quartalsweise)

**Periodenende:**
```
Ertragskonto / Umsatzsteuer      [Saldosteuersatz × Umsatz]
Umsatzsteuer / Bank              [gleicher Betrag]
```

⚠️ Bei Saldosteuersatz: Umsatz = Saldo Ertragskonto (100%), NICHT 108.1%!
→ Formel: Saldosteuersatz × (Saldo Ertragskonto nach Abzügen)

---

## 5) MWST-Abrechnung mit ESTV (Effektive Methode)

```
Umsatzsteuer / VST 1170          [Saldo VST 1170]
Umsatzsteuer / VST 1171          [Saldo VST 1171]
Umsatzsteuer / Bank oder Post    [Restschuld]
```

Restschuld = Saldo UMST − Saldo VST 1170 − Saldo VST 1171

Falls Guthaben (VST > UMST): ESTV überweist → `Bank / Umsatzsteuer`

---

## 6) Rücksendungen, Rabatte, Skonti MIT MWST

### Grundregel (Nettomethode):
> Die zwei Buchungssätze der Rechnung werden **umgekehrt** (Soll↔Haben).

**Kundenrabatt/-skonto (vorher Rechnung verbucht):**
```
Ertragskonto / Ford aus LL       [Netto-Reduktion]
Umsatzsteuer / Ford aus LL       [MWST-Reduktion]
```

**Lieferantenrabatt/-skonto (vorher Rechnung verbucht):**
```
Verb aus LL / Aufwandkonto       [Netto-Reduktion]
Verb aus LL / VST 1170 oder 1171 [MWST-Reduktion]
```

**Zahlung nach Skonto (Kunde zahlt Restschuld):**
```
Ertragskonto / Ford aus LL       [Skonto Netto]
Umsatzsteuer / Ford aus LL       [Skonto MWST]
Bank / Ford aus LL               [Zahlbetrag]
```

**Zahlung nach Skonto (wir zahlen Lieferant):**
```
Verb aus LL / Aufwandkonto       [Skonto Netto]
Verb aus LL / VST 1170/1171      [Skonto MWST]
Verb aus LL / Bank               [Zahlbetrag]
```

### Grundregel (Bruttomethode):
> Nur EIN Buchungssatz (Bruttobetrag), keine separate MWST-Korrektur.

---

## 7) MWST-Ausnahmen (KRITISCH)

| Typ                  | UMST? | VST-Abzug? | Beispiele                                   |
|----------------------|-------|------------|----------------------------------------------|
| **Ausgenommen** (Art. 21) | Nein  | Nein       | Versicherungen, Miete Wohnungen, Zinsen, Ärzte, Bildung |
| **Befreit** (Art. 23)     | Nein  | **Ja**     | Exporte, Lieferungen ins Ausland             |

→ Versicherungsprämien: **kein VST, kein UMST** → einfach `Aufwandkonto / Verb aus LL` (Bruttobetrag)
→ Zinsen, Bankspesen: **ausgenommen** → `Finanzaufwand / Bank`
→ Exporte: **kein UMST**, aber VST auf Einkäufe abziehbar
→ Löhne: **kein MWST-Bezug** → `Lohnaufwand / Bank`

---

## 8) Verkauf/Kauf von Anlagevermögen MIT MWST

**Verkauf AV (Nettomethode):**
```
Kasse/Bank/Ford LL / AV-Konto        [Buchwert oder Netto-Verkaufspreis]
Kasse/Bank/Ford LL / Umsatzsteuer    [MWST auf Verkaufspreis]
```
→ Falls Verkaufspreis > Buchwert: Differenz = a.o. Ertrag
→ Falls Verkaufspreis < Buchwert: Differenz = a.o. Aufwand

**Kauf AV (Nettomethode):**
```
AV-Konto / Kasse/Bank/Verb LL        [Nettobetrag]
VST 1171 / Kasse/Bank/Verb LL        [MWST-Betrag]
```

---

## 9) Kreditkarten mit MWST

**Tageseinnahmen verbuchen:**
```
Kk und Dk / Ertragskonto             [Nettobetrag]
Kk und Dk / Umsatzsteuer             [MWST-Betrag]
```

**Gutschrift von KK-Gesellschaft (mit Kommission):**
```
Bank / Kk und Dk                     [Gutschrift]
Finanzaufwand / Kk und Dk            [Kommission]
```

---

## 10) Verrechnungssteuer (VST 35%)

```
Bank / Finanzertrag                  [Habenzins brutto]
Finanzaufwand / Bank                 [Sollzins]
Guthaben VST / Bank                  [35% vom Habenzins]
Finanzaufwand / Bank                 [Spesen]
```

---

# ═══════════════════════════════════════════
# KAP 11 — OFFENPOSTEN-BUCHHALTUNG
# ═══════════════════════════════════════════

## 11) Kernregel Offenposten

> **Rechnungen werden NICHT bei Erhalt/Versand gebucht, sondern NUR bei Zahlung.**

- Eingangsrechnung erhalten → **KB** (Kein Buchungssatz) — Rechnung wird abgelegt
- Ausgangsrechnung versendet → **KB** (Kein Buchungssatz) — Rechnung wird abgelegt
- Erst bei **Zahlung** wird gebucht

---

## 12) Buchung bei Zahlung (Offenposten + Nettomethode)

### Kundenzahlung erhalten:
```
Bank / Ertragskonto                  [Nettobetrag]
Bank / Umsatzsteuer                  [MWST-Betrag]
```

### Lieferantenzahlung geleistet:
```
Aufwandkonto / Bank                  [Nettobetrag]
VST 1170 oder 1171 / Bank           [MWST-Betrag]
```

### Kundenzahlung MIT Skonto (Offenposten):
Skonto wird direkt bei Zahlung berücksichtigt — kein vorheriger Rechnungsbuchungssatz existiert!
```
Bank / Ertragskonto                  [Netto − Skonto-Netto]
Bank / Umsatzsteuer                  [MWST − Skonto-MWST]
```

### Lieferantenzahlung MIT Skonto (Offenposten):
```
Aufwandkonto / Bank                  [Netto − Skonto-Netto]
VST 1170/1171 / Bank                 [MWST − Skonto-MWST]
```

---

## 13) Offenposten + Bruttomethode (Saldosteuersatz)

### Kundenzahlung:
```
Bank / Ertragskonto                  [Bruttobetrag]
```

### Lieferantenzahlung:
```
Aufwandkonto / Bank                  [Bruttobetrag]
```

---

## 14) Jahresabschluss — Offene Posten umbuchen

Am **31.12.** müssen noch offene Rechnungen erfasst werden:

### Offene Kundenrechnungen (Nettomethode):
```
Ford aus LL / Ertragskonto           [Nettobetrag]
Ford aus LL / Umsatzsteuer           [MWST-Betrag]
```

### Offene Lieferantenrechnungen (Nettomethode):
```
Aufwandkonto / Verb aus LL           [Nettobetrag]
VST 1170/1171 / Verb aus LL          [MWST-Betrag]
```

### Offene Kundenrechnungen (Bruttomethode/Saldosteuersatz):
```
Ford aus LL / Ertragskonto           [Bruttobetrag]
```

### Offene Lieferantenrechnungen (Bruttomethode):
```
Aufwandkonto / Verb aus LL           [Bruttobetrag]
```

### Wiedereröffnung 01.01. (Rückbuchung):
Die Jahresabschlussbuchungen werden **umgekehrt** (Soll↔Haben).

---

## 15) Forderungsverlust bei Offenposten

Da bei Offenposten keine Rechnung gebucht wurde, gibt es keinen Ford-aus-LL-Saldo.
→ Verlust wird direkt gegen Ertrag gebucht:

```
Verluste Ford / Ertragskonto        [Nettobetrag]
```

⚠️ Keine MWST-Korrektur nötig, da MWST nie gebucht wurde (vereinnahmtes Entgelt).

Ausnahme: Wenn die Rechnung bereits bezahlt und MWST gebucht wurde:
```
Verluste Ford / Ertragskonto        [Nettobetrag]
Umsatzsteuer / Ertragskonto         [MWST-Betrag]  ← MWST-Korrektur
```

---

## 16) Vereinnahmtes vs. Vereinbartes Entgelt

| Kriterium              | Vereinbartes Entgelt                    | Vereinnahmtes Entgelt                 |
|------------------------|------------------------------------------|---------------------------------------|
| MWST-Zeitpunkt         | Bei Rechnungsstellung                    | Bei Zahlung                           |
| Typische Methode       | Laufende Verbuchung der Rechnungen       | Offenposten-Buchhaltung               |
| VST abziehbar ab       | Rechnungsdatum                           | Zahlungsdatum                         |
| UMST geschuldet ab     | Rechnungsdatum                           | Zahlungsdatum                         |

---

## 17) Offenposten + Bankkontoauszug (Gesamtaufgaben)

### Workflow:
1. Bankkontoauszug lesen → jede Zeile = ein Geschäftsfall
2. Für jede Zeile prüfen:
   - Ist MWST relevant? → Netto/MWST aufsplitten
   - Ist es MWST-ausgenommen? (Versicherung, Miete Wohnung, Zinsen) → kein VST/UMST
   - Welches VST-Konto? (1170 für KK4, 1171 für KK5-8 + AV)
3. Buchungssatz formulieren
4. Bei Skonto/Rabatt: Reduktion korrekt auf Netto UND MWST aufteilen

---

## 18) Gemischte Aufgaben — Entscheidungsbaum

```
Geschäftsfall erhalten
│
├── Rechnung erhalten/versendet?
│   ├── Offenposten-Methode → KB
│   └── Laufende Methode → Buchen (Netto oder Brutto)
│
├── Zahlung geleistet/erhalten?
│   ├── MWST-pflichtig?
│   │   ├── Ja → Netto + MWST aufsplitten
│   │   └── Nein (ausgenommen) → Bruttobetrag direkt
│   ├── Skonto/Rabatt?
│   │   ├── Ja → Reduktion auf Netto UND MWST
│   │   └── Nein → Voller Betrag
│   └── Buchen via Bank/Post/Kasse
│
├── MWST-Abrechnung?
│   ├── Effektiv → UMST / VST 1170 + VST 1171 + Rest Bank
│   └── Saldosteuersatz → Ertrag / UMST + UMST / Bank
│
└── Jahresabschluss?
    └── Offene Rechnungen → Ford LL / Ertrag + VST/UMST
```

---

## 19) Gelöste Musterbeispiele

### Beispiel A: Nettomethode — Einkauf + Zahlung mit Skonto

Rechnung CHF 10 810 (inkl. 8.1%) auf Rechnung, Zahlung mit 2% Skonto per Bank.

**Rechnung:**
```
Warenaufwand / Verb aus LL           10 000.00
VST 1170 / Verb aus LL                 810.00
```

**Zahlung mit 2% Skonto:**
```
Verb aus LL / Warenaufwand              200.00   (2% von 10 000)
Verb aus LL / VST 1170                   16.20   (2% von 810)
Verb aus LL / Bank                   10 593.80
```

### Beispiel B: Nettomethode — Verkauf + Rabatt + Skonto

Verkauf CHF 30 808.50 (inkl. 8.1%) auf Rechnung.
Dann 10% Rabatt, dann Zahlung mit 2% Skonto.

**Rechnung:**
```
Ford aus LL / Produktionserlöse      28 500.00
Ford aus LL / Umsatzsteuer            2 308.50
```

**10% Rabatt:**
```
Produktionserlöse / Ford aus LL       2 850.00
Umsatzsteuer / Ford aus LL             230.85
```

**Zahlung mit 2% Skonto auf Restschuld (27 727.65):**
```
Produktionserlöse / Ford aus LL         513.00   (2% von 25 650)
Umsatzsteuer / Ford aus LL              41.55   (2% von 2 077.65)
Bank / Ford aus LL                   27 173.10
```

### Beispiel C: Offenposten — Rechnung + Zahlung

Kundenrechnung CHF 6 756.25 (inkl. 8.1%) versendet. Zahlung mit 2% Skonto.

**Rechnung versendet:** KB

**Kundenzahlung mit 2% Skonto:**
```
Bank / Transportertrag                6 121.10   (= 6 250 − 125 − 4.90 Rundung)
Bank / Umsatzsteuer                     496.10   (= 506.25 − 10.15)
```
→ Netto 6 250, MWST 506.25, Skonto 2%: Netto−125, MWST−10.15

### Beispiel D: Offenposten — Jahresabschluss

Offene Kundenrechnungen am 31.12.: CHF 64 860 (inkl. 8.1%)

```
Ford aus LL / Ertragskonto           60 000.00
Ford aus LL / Umsatzsteuer            4 860.00
```

Offene Lieferantenrechnungen: CHF 4 324 (inkl. 8.1%)
```
Aufwandkonto / Verb aus LL            4 000.00
VST 1170 / Verb aus LL                  324.00
```

### Beispiel E: Saldosteuersatzmethode

Honorarertrag CHF 138 000 (inkl. 8.1%), Saldosteuersatz 6.2%.

```
Honorarertrag / Umsatzsteuer          8 556.00   (= 6.2% × 138 000)
Umsatzsteuer / Bank                    8 556.00
```

⚠️ Bei Saldosteuersatz: Basis = Brutto-Ertrag (100%), NICHT Netto!

### Beispiel F: Bruttomethode — Periodenende

Konten vor Bereinigung:
- Materialaufwand 8.1%: Saldo 90 240
- Sonst. BetriebsAu 8.1%: Saldo 35 560
- Produktionserlöse 8.1%: Saldo 287 720

**VST ausbuchen:**
```
VST 1170 / Materialaufwand 8.1%       6 761.75   (90 240 / 108.1 × 8.1)
VST 1171 / Sonst. BetriebsAu 8.1%     2 673.50   (35 560 / 108.1 × 8.1 — Rundung prüfen)
```

**UMST ausbuchen:**
```
Produktionserlöse 8.1% / Umsatzsteuer 21 559.05   (287 720 / 108.1 × 8.1)
```

**Abrechnung:**
```
Umsatzsteuer / VST 1170                6 761.75
Umsatzsteuer / VST 1171                2 673.50
Umsatzsteuer / Bank                   12 123.80
```

---

## 20) Häufige Fehler (ANTI-FEHLER-LISTE)

1. ❌ MWST auf Versicherungsprämien berechnen → Versicherungen sind **ausgenommen**
2. ❌ MWST auf Löhne berechnen → Löhne haben **keinen MWST-Bezug**
3. ❌ MWST auf Zinsen/Bankspesen → **ausgenommen**
4. ❌ Bruttobetrag als Netto verwenden → **IMMER zuerst Brutto → Netto umrechnen**
5. ❌ VST 1170 für AV-Kauf verwenden → AV-Käufe gehen auf **VST 1171**
6. ❌ Bei Offenposten die Rechnung buchen → **KB!** Nur bei Zahlung buchen
7. ❌ Bei Saldosteuersatz VST separat buchen → **Keine VST bei Saldosteuersatz**
8. ❌ Saldosteuersatz auf Netto (exkl.) anwenden → Basis ist **Brutto (inkl. MWST)**
9. ❌ Rundung vergessen → **IMMER auf 5 Rappen runden**
10. ❌ Skonto nur auf Netto, nicht auf MWST → Skonto gilt auf **Netto UND MWST**
