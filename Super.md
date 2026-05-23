# SUPER-MD — FRW PRÜFUNG (Kap 4: MWST + Kap 11: Offenposten)
# Buchhaltung: Mehrwertsteuer & Offenposten-Methode (LaTeX-SAFE)

---

## 0) Output-Style (LaTeX-SAFE)

Wenn ein Viewer LaTeX nur dann rendert, wenn die ZEILE komplett LaTeX ist, benutze dieses Template:

- Jede Ausgabelinie ist GENAU ein LaTeX-Block:
  - beginnt mit `$`
  - endet mit `$`
- Nummerierung steht IN LaTeX:
  - `\text{1) }`, `\text{2a) }`, ...
- Wörter/Kontennamen IMMER in `\text{...}`
- Beträge: Apostroph-Tausender, 2 Dezimalen (z.B. `1'319.05`)
- Maximal 1 Buchungssatz pro Zeile

### Beispiel Buchungssatz (ohne MWST)

$\text{1) OCR: Monatslöhne CHF 10'500 per Bank}$

$\text{1) S: LohnAu 5000 / H: Bank 1020} \quad 10'500.00$

### Beispiel Buchungssatz (mit MWST Nettomethode)

$\text{2) OCR: Rg. Blumen CHF 1'319.05 inkl. 8.1\%}$

$\text{2) } 1'319.05 \div 1.081 = 1'220.21 \text{ exkl.} \quad \text{MWST } = 98.84$

$\text{2a) S: WarenAu 4200 / H: VLL 2000} \quad 1'220.21$

$\text{2b) S: VST 1170 / H: VLL 2000} \quad 98.84$

### Beispiel KB (Offenposten)

$\text{3) KB}$

### Beispiel R/F

$\text{a) F — Restaurant = Normalsatz 8.1\%, nicht reduziert}$

---

## 1) Kontenplan (Kernkonten)

### Aktiven (Klasse 1)
- 1000 Kasse
- 1010 Post
- 1020 Bank
- 1100 Forderungen aus LL (FLL / Debitoren)
- 1109 Delkredere (Wertberichtigung FLL)
- 1170 Vorsteuer Material/Handel (VST — Normalsatz)
- 1171 Vorsteuer Investition/Betriebsaufwand (VST — Normalsatz auf Kl. 1 + 6)
- 1176 Verrechnungssteuer (Guthaben)
- 1500 Maschinen
- 1510 Mobiliar
- 1520 Büromaschinen/Informatik
- 1530 Fahrzeuge

### Passiven (Klasse 2)
- 2000 Verbindlichkeiten aus LL (VLL / Kreditoren)
- 2200 Geschuldete MWST / Umsatzsteuer (UST)

### Erträge (Klasse 3)
- 3200 Handelserlös / Warenertrag (WarenER)
- 3400 Dienstleistungsertrag
- 3600 Übriger Ertrag
- 3900 Eigenleistungen / Eigenverbrauch

### Aufwände (Klasse 4)
- 4200 Handelswarenaufwand / Warenaufwand (WarenAu)
- 4400 Dienstleistungsaufwand

### Personalaufwand (Klasse 5)
- 5000 Lohnaufwand → **KEINE MWST**
- 5700 Sozialversicherungsaufwand → **KEINE MWST**

### Übriger Betriebsaufwand (Klasse 6)
- 6000 Raumaufwand / Miete
- 6100 Unterhalt/Reparaturen
- 6200 Fahrzeugaufwand
- 6260 Leasingaufwand (KFZ)
- 6300 Versicherungsaufwand → **KEINE MWST**
- 6400 Energieaufwand
- 6500 Verwaltungsaufwand / Büromaterial
- 6510 Telefonaufwand
- 6570 Informatikaufwand
- 6600 Werbeaufwand
- 6700 Übriger Betriebsaufwand
- 6800 Abschreibungen → **KEINE MWST**
- 6900 Finanzaufwand (Zinsen, Kommissionen)
- 6950 Finanzertrag (Zinsen) → **KEINE MWST (ausgenommen)**

### MWST-Kontenzuordnung (KRITISCH)
- **VST 1170**: Aufwände aus Kontenklasse **4** (Material, Waren, Handelsware, Energie, DL)
- **VST 1171**: Aufwände aus Kontenklasse **1** (Investitionen: Maschinen, Fahrzeuge, Mobiliar) + Kontenklasse **6** (übriger Betriebsaufwand: Büro, Telefon, Werbung, Reparaturen, IT, Raumaufwand)
- **UST 2200**: Auf alle Verkäufe/Erträge (Klasse 3)
- **KEIN MWST**: Lohn (5000), Sozialvers. (5700), Versicherungen (6300), Zinsen (6900/6950), Abschreibungen (6800)

---

## 2) MWST-Steuersätze

### Aktuelle Sätze (ab 01.01.2024)
| Satz | Prozent | Faktor inkl→exkl | Faktor exkl→inkl |
|------|---------|------------------|------------------|
| Normalsatz | 8.1% | ÷ 1.081 | × 1.081 |
| Reduzierter Satz | 2.6% | ÷ 1.026 | × 1.026 |
| Sondersatz (Beherbergung) | 3.8% | ÷ 1.038 | × 1.038 |

### Alte Sätze (vor 01.01.2024) — in älteren Aufgaben/Tests!
| Satz | Prozent | Faktor inkl→exkl | Faktor exkl→inkl |
|------|---------|------------------|------------------|
| Normalsatz | 7.7% | ÷ 1.077 | × 1.077 |
| Reduzierter Satz | 2.5% | ÷ 1.025 | × 1.025 |
| Sondersatz (Beherbergung) | 3.7% | ÷ 1.037 | × 1.037 |

### ACHTUNG: Immer den Steuersatz aus dem Aufgabentext verwenden! Nicht annehmen!

### Steuersatz-Zuordnung
- **Normalsatz (8.1%)**: Waren, Dienstleistungen, Elektronik, Möbel, Kleidung, Fahrzeuge, Benzin, Alkohol, Tabak, Restaurant/Gastgewerbe, Reparaturen, Büromaterial
- **Reduzierter Satz (2.6%)**: Lebensmittel (nicht Restaurant!), Medikamente, Bücher, Zeitungen, Wasser, Tierfutter, Saatgut, Pflanzen, alkoholfreie Getränke
- **Sondersatz (3.8%)**: Hotelübernachtung/Beherbergung (nur Übernachtung, NICHT Frühstück im Restaurant)
- **Befreit (0%, MIT Vorsteuerabzug)**: Exporte, Lieferungen ins Ausland
- **Ausgenommen (KEIN Vorsteuerabzug)**: Versicherungen, Krankenkasse, Bildung, Zinsen/Finanzdienstleistungen, Miete (Wohnraum), Gesundheit (ärztliche Leistungen), Kultur, Sport

### Wichtige Falle: Lebensmittel vs. Restaurant
- Sandwich MITNEHMEN = **2.6%** (Lebensmittel)
- Sandwich IM RESTAURANT essen = **8.1%** (Gastgewerbe-Normalsatz)
- Hotelübernachtung = **3.8%**, Frühstück im Hotel-Restaurant = **8.1%**

---

## 3) Quick Router

Lies die Aufgabe → erkenne Schlüsselwörter → springe zum Block:

| Schlüsselwörter | Typ | Block |
|-----------------|-----|-------|
| Geschäftsfall buchen, Buchungssatz, Nettomethode, Soll/Haben | MWST-Buchung | §4 T-MWST |
| inkl., exkl., Berechnungsschema, umrechnen | Berechnung | §5 T-BERECH |
| Rabatt, Skonto, Rücksendung, Gutschrift, Mängelrüge | Minderung | §6 T-MIND |
| MWST-Abrechnung, ESTV, Quartal, Zahllast, Guthaben | Abrechnung | §7 T-ABRECH |
| Saldosteuersatz, SSS, Bruttomethode, pauschal, halbjährlich | Saldosteuer | §8 T-SALDO |
| Offenposten, KB, kein Buchungssatz, laufende Verbuchung | Offenposten | §9 T-OP |
| 31.12, Abschluss, offene Rechnungen | OP-Abschluss | §9.3 |
| 01.01, Rückbuchung, Eröffnung, Wiedereröffnung | OP-Rückbuchung | §9.4 |
| Abschreibung, Verluste Ford., Delkredere | Abschreibung | §10 T-ABSCHR |
| Kreditkarte, Kommission, Wocheneinnahmen | Kreditkarte | §11 T-KREDIT |
| Bankkontoauszug, Sollzins, Habenzins, Spesen | Bankauszug | §12 T-BANK |
| Richtig/Falsch, R/F, wahr, Aussage | R/F-Frage | §13 T-RF |
| T-Konto, Saldo, Abschluss Konto | T-Konto | §14 T-KONTO |

### METHODE ERKENNEN (vor dem Lösen!)
1. Steht "Nettomethode" oder werden VST/UST getrennt? → **Nettomethode** (§4)
2. Steht "Saldosteuersatzmethode" oder "Bruttomethode"? → **SSS** (§8)
3. Steht "Offenposten" oder "KB"? → **Offenposten** (§9)
4. Kombination? z.B. "Offenposten + MWST" → §9 + §4 kombiniert

---

## 4) T-MWST — Nettomethode Buchungen

### Grundprinzip
- Beträge OHNE MWST (netto = 100%) auf Aufwand/Ertrag buchen
- MWST-Betrag SEPARAT auf VST (1170 oder 1171) oder UST (2200)
- Jeder MWST-pflichtige Geschäftsfall = ZWEI Buchungszeilen (oder Split-Buchung)

### Einkauf (Rechnung erhalten / wir bezahlen)

**Betrag inkl. MWST gegeben:**
- Netto = inkl. ÷ Faktor (z.B. ÷ 1.081)
- MWST = inkl. − netto
- S: Aufwandkonto (netto) / H: VLL 2000 oder Bank 1020 (inkl.)
- S: VST 1170 oder 1171 (MWST) / H: VLL 2000 oder Bank 1020

**Betrag exkl. MWST gegeben:**
- MWST = exkl. × Satz (z.B. × 0.081)
- Inkl. = exkl. + MWST
- S: Aufwandkonto (exkl.) / H: VLL 2000 oder Bank 1020 (inkl.)
- S: VST 1170 oder 1171 (MWST) / H: VLL 2000 oder Bank 1020

**LaTeX-Ausgabe-Muster:**
$\text{n) } \text{inkl.} \div 1.081 = \text{exkl.} \quad \text{MWST} = \text{Diff.}$
$\text{na) S: [AufwandKto] / H: VLL 2000} \quad \text{exkl.}$
$\text{nb) S: VST [1170/1171] / H: VLL 2000} \quad \text{MWST}$

### Verkauf (Rechnung ausgestellt / Kunde bezahlt)

**Betrag inkl. MWST:**
- Netto = inkl. ÷ Faktor
- MWST = inkl. − netto
- S: FLL 1100 oder Kasse 1000 oder Bank 1020 (inkl.) / H: Ertragskonto (netto)
- S: (gleich) / H: UST 2200 (MWST)

**LaTeX-Ausgabe-Muster:**
$\text{n) } \text{inkl.} \div 1.081 = \text{exkl.} \quad \text{MWST} = \text{Diff.}$
$\text{na) S: FLL 1100 / H: WarenER 3200} \quad \text{exkl.}$
$\text{nb) S: FLL 1100 / H: UST 2200} \quad \text{MWST}$

### Geschäftsfälle OHNE MWST (1 Zeile, keine VST/UST)
- Lohn: S: LohnAu 5000 / H: Bank 1020
- Sozialversicherung: S: SozVersAu 5700 / H: Bank 1020
- Versicherungsprämie: S: VersAu 6300 / H: Bank 1020
- Zinsaufwand (Sollzins): S: FinanzAu 6900 / H: Bank 1020
- Zinsertrag (Habenzins): S: Bank 1020 / H: FinanzER 6950
- Abschreibung: S: Abschreibung 6800 / H: Aktivkonto
- Privatbezug: S: Privat 2850 / H: Bank/Kasse

---

## 5) T-BERECH — Berechnungsschema

### inkl. → exkl. (Normalsatz 8.1%)
$\text{inkl. } 108.1\% = [Betrag]$
$\text{exkl. } 100\% = [Betrag] \div 1.081$
$\text{MWST } 8.1\% = \text{inkl.} - \text{exkl.}$

### exkl. → inkl. (Normalsatz 8.1%)
$\text{exkl. } 100\% = [Betrag]$
$\text{MWST } 8.1\% = [Betrag] \times 0.081$
$\text{inkl. } 108.1\% = \text{exkl.} + \text{MWST}$

### Für andere Sätze: gleiche Logik, Faktor anpassen
- 2.6%: ÷ 1.026 bzw. × 0.026
- 3.8%: ÷ 1.038 bzw. × 0.038
- 7.7%: ÷ 1.077 bzw. × 0.077

### ACHTUNG: Immer auf 5 Rappen runden (Schweizer Rundung)

---

## 6) T-MIND — Minderungen (Skonto, Rabatt, Rücksendung)

### Grundregel: Minderung = umgekehrter Buchungssatz + MWST-Korrektur

### Skonto auf EINKAUF (wir erhalten Skonto beim Bezahlen)
- Rechnungsbetrag war inkl. MWST
- Skonto wird auch auf MWST berechnet
- Skontobetrag inkl. → aufteilen in netto + MWST

$\text{S: VLL 2000} \quad \text{(voller Rg.-Betrag inkl.)}$
$\text{H: Bank 1020} \quad \text{(Zahlung = inkl. minus Skonto inkl.)}$
$\text{H: AufwandKto} \quad \text{(Skonto netto)}$
$\text{H: VST 1170/1171} \quad \text{(Skonto MWST)}$

Oder als Kompaktform:
$\text{n) Skonto inkl.} = \text{Rg. inkl.} \times \text{Skonto-\%}$
$\text{n) Skonto exkl.} = \text{Skonto inkl.} \div 1.081$
$\text{n) Skonto MWST} = \text{Skonto inkl.} - \text{Skonto exkl.}$
$\text{na) S: VLL 2000 / H: Bank 1020} \quad \text{Zahlung}$
$\text{nb) S: VLL 2000 / H: AufwandKto} \quad \text{Skonto exkl.}$
$\text{nc) S: VLL 2000 / H: VST 1170} \quad \text{Skonto MWST}$

### Skonto auf VERKAUF (Kunde erhält Skonto)
$\text{na) S: Bank 1020 / H: FLL 1100} \quad \text{Zahlung}$
$\text{nb) S: ErtragKto / H: FLL 1100} \quad \text{Skonto exkl.}$
$\text{nc) S: UST 2200 / H: FLL 1100} \quad \text{Skonto MWST}$

### Rabatt nachträglich / Gutschrift / Mängelrüge
- Gleiche Logik wie Skonto, einfach mit Rabattbetrag statt Skontobetrag
- Bei Einkauf: S: VLL / H: AufwandKto + H: VST
- Bei Verkauf: S: ErtragKto + S: UST / H: FLL

### Rücksendung
- Gleiche Logik: umgekehrter Buchungssatz der Original-Buchung (anteilig)
- MWST wird entsprechend zurückgebucht

---

## 7) T-ABRECH — MWST-Abrechnung (Nettomethode)

### Quartalsende: VST und UST verrechnen

**Schritt 1: Salden ermitteln**
- VST 1170 → Soll-Saldo = Guthaben
- VST 1171 → Soll-Saldo = Guthaben
- UST 2200 → Haben-Saldo = Schuld

**Schritt 2: Verrechnung**
- Zahllast = UST (H-Saldo) − VST 1170 (S-Saldo) − VST 1171 (S-Saldo)
- Wenn positiv → Zahllast an ESTV (wir schulden)
- Wenn negativ → Guthaben von ESTV (wir erhalten)

**Schritt 3: Buchungssätze**
$\text{a) S: UST 2200 / H: VST 1170} \quad \text{[ganzer VST 1170 Saldo]}$
$\text{b) S: UST 2200 / H: VST 1171} \quad \text{[ganzer VST 1171 Saldo]}$
$\text{c) S: UST 2200 / H: Bank 1020} \quad \text{[Restbetrag = Zahllast]}$

**LaTeX-Ausgabe-Muster:**
$\text{UST Saldo H: } [Betrag]$
$\text{- VST 1170 Saldo S: } [Betrag]$
$\text{- VST 1171 Saldo S: } [Betrag]$
$\text{= Zahllast ESTV: } [Betrag]$
$\text{a) S: UST 2200 / H: VST 1170} \quad [Betrag]$
$\text{b) S: UST 2200 / H: VST 1171} \quad [Betrag]$
$\text{c) S: UST 2200 / H: Bank 1020} \quad [Betrag]$

**Resultat:** VST 1170 Saldo = 0, VST 1171 Saldo = 0, UST 2200 Saldo = 0

---

## 8) T-SALDO — Saldosteuersatzmethode (SSS)

### Grundprinzip
- **Bruttomethode**: Alle Beträge INKL. MWST buchen (kein Netto-Split)
- **KEIN Vorsteuer-Konto** (kein 1170, kein 1171)
- Nur UST 2200 existiert
- Abrechnung HALBJÄHRLICH (nicht quartalsweise)

### Buchungen (Brutto)
- Einkauf: S: AufwandKto / H: VLL oder Bank (Betrag inkl. MWST!)
- Verkauf: S: FLL oder Kasse / H: ErtragKto (Betrag inkl. MWST!)
- Lohn: wie immer (kein MWST)
- Skonto/Rabatt: wie Nettomethode, aber Brutto-Beträge direkt

### MWST-Berechnung (Semesterende)
$\text{MWST-Schuld} = \text{Steuerbarer Umsatz (brutto)} \times \frac{\text{SSS}}{100}$

**Steuerbarer Umsatz = alle Ertrags-Konten (Klasse 3) zusammenzählen**
→ ACHTUNG: Minderungen (Skonto, Rabatt) bereits abgezogen!

### Buchung Saldosteuer
$\text{a) S: ErtragKto / H: UST 2200} \quad [MWST\text{-Schuld}]$
$\text{b) S: UST 2200 / H: Bank/Post} \quad [MWST\text{-Schuld}]$

### Beispiel SSS 6.2%
$\text{Steuerbarer Umsatz brutto: } 320'200.00$
$\text{MWST} = 320'200.00 \times 6.2 \div 100 = 19'852.40$
$\text{a) S: HonorarER / H: UST 2200} \quad 19'852.40$
$\text{b) S: UST 2200 / H: Post 1010} \quad 19'852.40$

### SSS: Typische Saldosteuersätze
- Werden in der Aufgabe angegeben (z.B. 6.2%, 5.1%, 6.7%)
- IMMER den Satz aus der Aufgabe verwenden!

---

## 9) T-OP — Offenposten-Buchhaltung (Kap 11)

### 9.1 Grundprinzip — Vergleich der zwei Methoden

**Methode mit laufender Verbuchung (Standard):**
- Rechnung erhalten/versandt → sofort buchen
- Zahlung → zweiter Buchungssatz

**Offenposten-Methode:**
- Rechnung erhalten/versandt → **KB** (Kein Buchungssatz!)
- Zahlung bar/Bank → buchen (direkt Aufwand/Ertrag an Bank/Kasse)
- Am 31.12: Alle OFFENEN (unbezahlten) Rechnungen buchen
- Am 01.01: Rückbuchungen der offenen Posten

### 9.2 KB-Regel (Wann "Kein Buchungssatz"?)

**KB gilt NUR bei Offenposten-Methode für:**
- Rechnung erhalten (Einkauf auf Kredit) → KB
- Rechnung versandt (Verkauf auf Kredit) → KB
- Gutschrift erhalten/versandt (auf Kredit) → KB

**KEIN KB bei:**
- Barzahlung / per Bank / per Post → IMMER buchen!
- Abschreibungen (kalkulatorisch) → IMMER buchen!
- Lohnzahlung → IMMER buchen (ist eine Zahlung!)

### LaTeX-Ausgabe KB:
$\text{n) KB}$

### 9.3 Abschluss per 31.12 (Offenposten-Methode)

**Am 31.12 werden ALLE unbezahlten Rechnungen gebucht:**

**Offene Kundenrechnungen (wir haben Guthaben):**
$\text{S: FLL 1100 / H: [ErtragKto]} \quad [Betrag]$

**Offene Lieferantenrechnungen (wir schulden):**
$\text{S: [AufwandKto] / H: VLL 2000} \quad [Betrag]$

**Bei mehreren offenen Rechnungen pro Konto:** Jede einzeln buchen ODER Summe pro Konto

**ACHTUNG: Der Betrag am 31.12 =**
- Originalrechnung MINUS bereits geleistete Teilzahlungen
- MINUS Skonto (falls schon gewährt)
- MINUS Gutschriften
- = Offener Restbetrag

### 9.4 Rückbuchung per 01.01 (Wiedereröffnung)

**Am 01.01 werden die 31.12-Buchungen UMGEKEHRT:**

**Für ehemalige Kundenforderungen:**
$\text{S: [ErtragKto] / H: FLL 1100} \quad [Betrag]$

**Für ehemalige Lieferantenschulden:**
$\text{S: VLL 2000 / H: [AufwandKto]} \quad [Betrag]$

**WICHTIG: Die Rückbuchung betrifft NUR Posten, die am 31.12 gebucht wurden!**

### 9.5 Offenposten + MWST (Kombination)

Wenn die Aufgabe Offenposten MIT MWST verlangt:
- KB bleibt KB (keine Änderung)
- Bei Barzahlung: Nettomethode-Split (Aufwand + VST oder Ertrag + UST)
- Am 31.12: Abschlussbuchung OHNE MWST-Split (Bruttobetrag)
  → S: FLL / H: ErtragKto (Brutto inkl. MWST)
  → S: AufwandKto / H: VLL (Brutto inkl. MWST)
- Am 01.01: Rückbuchung OHNE MWST-Split (gleicher Bruttobetrag)
  → Dann bei späterer Zahlung: Nettomethode-Split anwenden

### 9.6 Offenposten — Spezialfälle

**Teilzahlung:**
- Im OP: Nur die Zahlung buchen (S: AufwandKto / H: Bank)
- Am 31.12: Offener REST buchen (Original − Teilzahlung)

**Skonto bei Offenposten:**
- Im OP: Nur Zahlbetrag (nach Skonto) buchen als Aufwand/Ertrag
- Kein separater Skonto-Buchungssatz nötig (weil Original nie gebucht wurde!)

**Mahnung:**
- KB im Offenposten (Mahnung ist kein Zahlungsvorgang)

---

## 10) T-ABSCHR — Abschreibungen

### Kalkulatorische (planmässige) Abschreibung
$\text{S: Abschreibung 6800 / H: [Aktivkonto]} \quad [Betrag]$
- Gilt in BEIDEN Methoden (laufend + Offenposten)
- **KEINE MWST** auf Abschreibungen!

### Definitive Abschreibung (Verlust auf Forderungen)
$\text{S: Verluste FLL 3800 / H: FLL 1100} \quad [Betrag]$
Oder wenn Delkredere:
$\text{S: Verluste FLL 3800 / H: Delkredere 1109} \quad [Betrag]$

---

## 11) T-KREDIT — Kreditkartenabrechnung

### Wocheneinnahmen per Kreditkarte (inkl. MWST)
$\text{a) S: FLL KK / H: WarenER 3200} \quad \text{exkl.}$
$\text{b) S: FLL KK / H: UST 2200} \quad \text{MWST}$

### Kreditkartenabrechnung (Bank erhält Nettobetrag)
$\text{a) S: Bank 1020 / H: FLL KK} \quad \text{Auszahlungsbetrag}$
$\text{b) S: FinanzAu 6900 / H: FLL KK} \quad \text{Kommission}$

ACHTUNG: Kommission der Kreditkartengesellschaft = FinanzAu, KEINE MWST (Finanzdienstleistung = ausgenommen)

---

## 12) T-BANK — Bankkontoauszug buchen

### Sollzins (Bank belastet uns Zinsen)
$\text{S: FinanzAu 6900 / H: Bank 1020} \quad [Betrag]$
Keine MWST (Zinsen = ausgenommen)

### Habenzins (Bank schreibt uns Zinsen gut)
$\text{S: Bank 1020 / H: FinanzER 6950} \quad [Nettobetrag]$
$\text{S: Guthaben VST 1176 / H: FinanzER 6950} \quad [Verrechnungssteuer]$
Verrechnungssteuer = 35% des Bruttozinses
Keine MWST (Zinsen = ausgenommen)

### Spesen, Kommissionen (Bank belastet)
$\text{a) S: FinanzAu 6900 / H: Bank 1020} \quad \text{exkl.}$
$\text{b) S: VST 1171 / H: Bank 1020} \quad \text{MWST}$
→ Bankspesen können MWST-pflichtig sein! → VST 1171 (Klasse 6)

---

## 13) T-RF — Richtig/Falsch Fakten

### MWST-Fakten (Kap 4)
- Steuersubjekt = Unternehmen mit Umsatz > CHF 100'000/Jahr
- VST = Aktivkonto (Guthaben bei ESTV), UST = Passivkonto (Schuld an ESTV)
- VST 1170 = Klasse 4 (Waren/Material), VST 1171 = Klasse 1+6 (Investition/Betrieb)
- Nettomethode = Beträge exkl. MWST buchen
- Bruttomethode = Beträge inkl. MWST buchen
- SSS = kein Vorsteuerabzug, nur Umsatzsteuer pauschal
- Nettomethode = quartalsweise Abrechnung
- SSS = halbjährliche Abrechnung (semesterweise)
- Lohn, Zinsen, Versicherungen, Abschreibungen = KEINE MWST
- Lebensmittel zum Mitnehmen = 2.6%, im Restaurant = 8.1%
- Medikamente = 2.6%
- Hotel-Übernachtung = 3.8%, Frühstück im Restaurant = 8.1%
- Befreit (Export) ≠ Ausgenommen (Gesundheit, Bildung, Finanzen)
- Befreit: MIT Vorsteuerabzug; Ausgenommen: OHNE Vorsteuerabzug

### Offenposten-Fakten (Kap 11)
- Rechnungen auf Kredit = KB (bei Offenposten-Methode)
- Barzahlungen = immer buchen (auch bei Offenposten)
- 31.12 = offene Rechnungen buchen (FLL/VLL)
- 01.01 = Rückbuchungen (umgekehrt)
- Kalkulatorische Abschreibung = in beiden Methoden gleich
- Lohn = in beiden Methoden gleich (ist eine Zahlung)

---

## 14) T-KONTO — T-Konten führen

### Ausgabeformat T-Konto

$\text{--- [Kontoname] [Nr] ---}$
$\text{S: } [Betrag] \text{ (Ref)} \quad \text{H: } [Betrag] \text{ (Ref)}$
$\text{S: } [Betrag] \text{ (Ref)} \quad \text{H: } [Betrag] \text{ (Ref)}$
$\text{Total S: } [Summe] \quad \text{Total H: } [Summe]$
$\text{Saldo: } [Betrag] \text{ [S/H]}$

### VST 1170 (Aktivkonto, Soll-Saldo)
- Soll: Alle MWST-Beträge aus Einkäufen Klasse 4
- Haben: MWST-Abrechnung (Verrechnung mit UST) + Skonto-Korrekturen
- Endsaldo nach Abrechnung = 0

### VST 1171 (Aktivkonto, Soll-Saldo)
- Soll: Alle MWST-Beträge aus Investitionen/Betriebsaufwand Klasse 1+6
- Haben: MWST-Abrechnung (Verrechnung mit UST)
- Endsaldo nach Abrechnung = 0

### UST 2200 (Passivkonto, Haben-Saldo)
- Haben: Alle MWST-Beträge aus Verkäufen
- Soll: MWST-Abrechnung (VST 1170 + VST 1171 + Zahlung Bank)
- Endsaldo nach Abrechnung = 0

### FLL 1100 (Aktivkonto)
- Soll: Verkäufe auf Kredit, 31.12-Abschluss (OP)
- Haben: Zahlungseingänge, Skonto, 01.01-Rückbuchung (OP)

### VLL 2000 (Passivkonto)
- Haben: Einkäufe auf Kredit, 31.12-Abschluss (OP)
- Soll: Zahlungsausgänge, Skonto, 01.01-Rückbuchung (OP)

---

## 15) X-TRAP — Häufige Fehler / Fallen

1. **VST 1170 vs 1171 verwechselt**: 1170 = Klasse 4 (Waren), 1171 = Klasse 1+6 (Investition/Betrieb)
2. **Steuersatz nicht aus Aufgabe gelesen**: IMMER den angegebenen Satz verwenden (7.7% oder 8.1% etc.)
3. **Lohn mit MWST gebucht**: Lohn hat KEINE MWST!
4. **Restaurant vs. Mitnehmen verwechselt**: Restaurant = 8.1% (Normalsatz), Mitnehmen = 2.6%
5. **Skonto ohne MWST-Korrektur**: Skonto MUSS auch die MWST-Komponente korrigieren (VST/UST anpassen)
6. **Offenposten: Rechnung gebucht statt KB**: Bei OP-Methode KEINE Buchung für Rechnungen auf Kredit!
7. **Offenposten: Barzahlung als KB notiert**: Barzahlungen werden IMMER gebucht, auch bei OP!
8. **31.12 vergessen**: ALLE offenen Rechnungen am 31.12 buchen!
9. **01.01 Rückbuchung vergessen**: Am 01.01 MÜSSEN die 31.12-Buchungen umgekehrt werden!
10. **SSS: Vorsteuer abgezogen**: Bei Saldosteuersatzmethode gibt es KEIN Vorsteuer-Konto!
11. **SSS: Nettobetrag statt Brutto gebucht**: SSS = alles BRUTTO buchen!
12. **MWST-Abrechnung: Bank vergessen**: Nach VST-Verrechnung bleibt Rest = Zahlung an ESTV per Bank!
13. **Beträge nicht auf 2 Dezimalen**: IMMER CHF mit 2 Dezimalstellen!
14. **Soll/Haben vertauscht**: Aufwand/Aktivzunahme = SOLL, Ertrag/Passivzunahme = HABEN
15. **Befreit mit Ausgenommen verwechselt**: Befreit (Export) = MIT VST-Abzug; Ausgenommen = OHNE VST-Abzug
16. **Kreditkarten-Kommission mit MWST**: Kommission KK-Gesellschaft = Finanzdienstleistung = AUSGENOMMEN (keine MWST)
17. **Bankspesen ohne MWST**: Bankspesen KÖNNEN MWST enthalten → prüfen! (VST 1171)
18. **Verrechnungssteuer vergessen**: Habenzins → Bank erhält 65%, 35% = Guthaben VST 1176
