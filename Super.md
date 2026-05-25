# SUPER-MD — FRW PRÜFUNG KAP 4 (Mehrwertsteuer) + KAP 11 (Offenposten-Buchhaltung)
# Buchungssätze: Schweizer Rechnungswesen (LaTeX-SAFE)

---

## 0) Output-Style (LaTeX-SAFE)

Jede Ausgabelinie ist GENAU ein LaTeX-Block:
- beginnt mit `$` und endet mit `$`
- Nummerierung steht IN LaTeX: `\text{1) }`, `\text{2) }`, ...
- Wörter/Hinweise IMMER in `\text{...}`
- Kontonamen in `\text{...}` (z.B. `\text{MaterialAu}`)
- Beträge als normale Zahlen mit Apostroph-Tausender: `6'761.75`
- Hinweise am Ende als `\text{[| ...]}`

### Beispiel-Output (Einkauf mit MWST Nettomethode)

$\text{OCR: Kauf Rohmaterial CHF 4'924.80 inkl. 8.1\% auf Rg}$

$\text{Buchungssatz 1}$

$\text{1) MaterialAu / Verb aus LL 8.1\% Betrag: } 4'555.80$

$\text{2) VST 1170 / Verb aus LL 8.1\% Betrag: } 369.00$

---

## 1) MWST-Grundlagen (KAP 4)

### 1.1 Steuersätze
- Normalsatz: **8.1%** (Kleider, Elektronik, Reparaturen, Alkohol, Benzin, Diesel, Handyabo, Elektrizität, Wasser)
- Reduzierter Satz: **2.6%** (Lebensmittel, Medikamente, Zeitungen/Zeitschriften, Bücher, Wasser in Leitungen)
- Sondersatz: **3.8%** (Beherbergung/Hotel inkl. Frühstück)
- **0% befreit** (Exporte) → Vorsteuerabzug erlaubt
- **Ausgenommen** (Versicherungen, Ärzte, Bildung, Kultur, Wohnungsvermietung) → KEIN Vorsteuerabzug

### 1.2 Steuersubjekt & Steuerobjekt
- Steuersubjekt: Unternehmen mit Jahresumsatz ≥ CHF 100'000 (steuerpflichtig)
- Unter CHF 100'000: befreit, kann freiwillig versteuern
- Sportvereine/gemeinnützige: Grenze CHF 250'000
- Steuerobjekt: steuerbare Leistungen im Inland + Importe

### 1.3 Vorsteuer & Umsatzsteuer
- **Vorsteuer** = Guthaben gegenüber ESTV (bei Einkäufen bezahlt)
  - Konto **1170**: Vorsteuer auf Material, Handelswaren, DL, Energie (Kontenklasse 4)
  - Konto **1171**: Vorsteuer auf Investitionen + übriger Betriebsaufwand (Kontenklassen 1, 5–8)
- **Umsatzsteuer** (Konto **2200**) = Schuld gegenüber ESTV (bei Verkäufen kassiert)
- Abzuliefernde MWST = Umsatzsteuer − Vorsteuer (Normalfall: Schuld)

### 1.4 MWST-Berechnung
- Betrag exkl. MWST = 100%
- Betrag inkl. MWST = 108.1% (bzw. 102.6% / 103.8%)
- Von inkl. → exkl.: Betrag / 108.1 × 100
- Von inkl. → MWST: Betrag / 108.1 × 8.1
- Auf 5 Rappen runden

### 1.5 MWST-konformer Beleg
Pflichtangaben: Name+Ort Leistender, UID-Nr. + "MWST", Name+Ort Empfänger, Datum/Zeitraum, Art der Leistung, Entgelt, Steuersatz + Steuerbetrag.
Ohne → kein Vorsteuerabzug.
Ausnahme: Kassenzettel bis CHF 400 → Name Kunde nicht nötig.

---

## 2) Abrechnungs- & Verbuchungsmethoden (KAP 4)

### 2.1 Abrechnungsmethoden
| Methode | Vorsteuerabzug | Abrechnung |
|---|---|---|
| **Effektive Methode** | JA (VST rückforderbar) | quartalsweise |
| **Saldosteuersatz (SSS)** | NEIN | halbjährlich |

### 2.2 Verbuchungsmethoden
| Methode | Buchungen pro GF | MWST sichtbar |
|---|---|---|
| **Nettomethode** | 2 BS (Netto + MWST separat) | laufend |
| **Bruttomethode** | 1 BS (Brutto inkl. MWST) | erst Ende Quartal |

### 2.3 Abrechnungsarten
- **Vereinbartes Entgelt**: Rechnungsdatum massgebend (Standard)
- **Vereinnahmtes Entgelt**: Zahlungsdatum massgebend (bei Offenposten-Buchhaltung)

---

## 3) Effektive Methode + Nettomethode — Buchungsregeln (KAP 4)

### 3.1 Einkäufe (2 Buchungssätze)

**Material/Waren auf Rechnung (Kontenklasse 4):**
```
MaterialAu / Verb aus LL    [Nettobetrag]
VST 1170 / Verb aus LL      [MWST-Betrag]
```

**Investitionen/übriger Aufwand auf Rechnung (Kontenklassen 1, 5–8):**
```
Büromaschinen / Verb aus LL    [Nettobetrag]
VST 1171 / Verb aus LL         [MWST-Betrag]
```

**Bareinkauf Material:**
```
VerwaltungsAu / Kasse    [Nettobetrag]
VST 1171 / Kasse         [MWST-Betrag]
```

### 3.2 Verkäufe (2 Buchungssätze)

**Verkauf produzierte Güter auf Kredit:**
```
Ford aus LL / ProdER       [Nettobetrag]
Ford aus LL / UMST 2200    [MWST-Betrag]
```

**Barverkauf:**
```
Kasse / ProdER         [Nettobetrag]
Kasse / UMST 2200      [MWST-Betrag]
```

**Verkauf Anlagevermögen (z.B. Fahrzeug zum Buchwert):**
```
Kasse / Fahrzeuge      [Buchwert]
Kasse / UMST 2200      [MWST auf Buchwert]
```

### 3.3 Minderungen (Rabatte, Skonti, Rücksendungen)
**Regel: Umkehr der ursprünglichen Buchungssätze (2 BS)**

**Lieferantenrabatt/-skonto (Einkaufsseite):**
```
Verb aus LL / MaterialAu     [Netto-Minderung]
Verb aus LL / VST 1170       [MWST-Minderung]
Verb aus LL / Bank           [Zahlbetrag]
```

**Kundenrabatt/-skonto (Verkaufsseite):**
```
ProdER / Ford aus LL         [Netto-Minderung]
UMST 2200 / Ford aus LL      [MWST-Minderung]
Bank / Ford aus LL            [Zahlbetrag]
```

### 3.4 Kreditkarten-/Debitkarten-Verkäufe
```
Kk und Dk / WarenEr         [Nettobetrag]
Kk und Dk / UMST 2200       [MWST-Betrag]
```
Bei Gutschrift durch Kartengesellschaft:
```
Bank / Kk und Dk             [Gutschrift]
FinanzAu / Kk und Dk         [Kommission]
```
**WICHTIG: Kommission berechtigt NICHT zur UMST-Reduktion!**

### 3.5 Zahlung von Rechnungen (kein MWST-Effekt)
```
Verb aus LL / Bank           [Bruttobetrag]
Bank / Ford aus LL           [Bruttobetrag]
```

### 3.6 Abrechnung MWST mit ESTV (Ende Quartal)
```
UMST 2200 / VST 1170        [Saldo VST 1170]
UMST 2200 / VST 1171        [Saldo VST 1171]
UMST 2200 / Bank (oder Post) [Restschuld]
```
→ Alle 3 Konten (VST 1170, VST 1171, UMST) haben danach Saldo 0.

### 3.7 Von der MWST ausgenommene Leistungen
- Versicherungsprämien, Miete Wohnungen → KEIN VST/UMST
- Buchung nur 1 BS: z.B. `FahrzeugAu / Verb aus LL [Brutto = Netto]`

---

## 4) Effektive Methode + Bruttomethode (KAP 4)

### 4.1 Während Quartal
- Alles inkl. MWST in EINEM Buchungssatz:
```
WarenAu 8.1% / Verb aus LL    [Bruttobetrag]
Ford aus LL / WarenEr 8.1%     [Bruttobetrag]
```
- Separate Konten nach Steuersatz (z.B. WarenEr 8.1%, WarenEr 2.6%)

### 4.2 Ende Quartal: Bereinigung
- Vorsteuer aus Aufwandkonten extrahieren:
```
VST 1170 / BetriebsAu 8.1%    [VST-Betrag aus KK4]
VST 1171 / BetriebsAu 8.1%    [VST-Betrag aus KK1,5-8]
```
- Umsatzsteuer aus Ertragskonten extrahieren:
```
ProdER 8.1% / UMST 2200       [UMST-Betrag]
```
- Dann normale Abrechnung wie bei Nettomethode (3.6)

### 4.3 Berechnung VST aus Bruttokonto
- Bruttobetrag / 108.1 × 8.1 = Vorsteuer
- Aufteilen: KK4-Anteil → VST 1170, Rest → VST 1171

---

## 5) Saldosteuersatzmethode (SSS) — KAP 4

### 5.1 Merkmale
- Kein Vorsteuerabzug
- Saldosteuersatz < normaler Satz (z.B. 2.1%, 3.7%, 5.3%)
- Bruttoumsatz = 100% für SSS-Berechnung
- Halbjährliche Abrechnung
- Max. Jahresumsatz CHF 5'024'000 / max. Steuerlast CHF 108'000

### 5.2 Verbuchung (Bruttomethode, Standard bei SSS)
Während Semester: 1 Buchungssatz (Brutto)
```
Ford aus LL / ProdER    [Bruttobetrag inkl. 8.1%]
```
Ende Semester:
```
ProdER / UMST 2200      [Bruttoumsatz × SSS]
UMST 2200 / Post        [Zahlung an ESTV]
```

### 5.3 Auf Kundenbeleg
- Normaler Satz (8.1%) sichtbar → Kunde kann VST abziehen
- SSS ist intern, Kunde sieht ihn nicht

---

## 6) Offenposten-Buchhaltung (KAP 11)

### 6.1 Grundprinzip
- Rechnungen werden NICHT verbucht (weder Ein- noch Ausgangsrechnungen)
- Nur ZAHLUNGEN werden verbucht (anhand Zahlungsbeleg: Bank/Post/Kasse)
- Konten Ford aus LL und Verb aus LL: während Jahr = 0
- Eignung: kleine(re) Unternehmen
- Skonti, Rabatte, Rücksendungen: werden NICHT verbucht → "Kein Buchungssatz" / "KB"

### 6.2 Während des Jahres (nur Zahlungen buchen)

**Kundenzahlung eingeht:**
```
Bank / WarenEr (oder TransportEr, ProdER)    [Zahlbetrag]
```
→ Bei Skonto: nur der tatsächlich erhaltene Betrag wird als Ertrag gebucht.

**Lieferantenrechnung wird bezahlt:**
```
WarenAu / Bank    [Zahlbetrag]
Fahrzeuge / Bank  [Zahlbetrag]
VerwAu / Bank     [Zahlbetrag]
```

**Barverkauf:**
```
Kasse / WarenEr    [Barbetrag]
```

**NICHT verbucht (= KB):**
- Ausgestellte Kundenrechnungen
- Eingehende Lieferantenrechnungen
- Rabatte/Skonti/Rücksendungen (solange keine Zahlung)

### 6.3 Abschluss (31.12.) — Offene Rechnungen verbuchen

**Offene Kundenrechnungen:**
```
Ford aus LL / WarenEr (o. ProdER, TransportEr, HonorarEr)    [Betrag]
```

**Offene Lieferantenrechnungen:**
```
WarenAu / Verb aus LL           [Betrag für Waren]
MaterialAu / Verb aus LL        [Betrag für Material]
Fahrzeuge / Verb aus LL          [Betrag für Fahrzeuge]
VerwAu / Verb aus LL             [Betrag für Verwaltung]
EnergieAu LeistErst / Verb aus LL  [Betrag für Energie]
```

**Abschreibungen (gleich wie bei normaler Methode):**
```
Abschr / Fahrzeuge    [Betrag]
```

**Warenbestandsänderung (ohne laufende Inventur):**
```
WarenAu / WarenBest    [Bestandsabnahme]
WarenBest / WarenAu    [Bestandszunahme]
```

### 6.4 Wiedereröffnung (01.01.) — Rückbuchung

**Rückbuchung = Umkehr der Abschlussbuchungen:**

Offene Kundenrechnungen:
```
WarenEr / Ford aus LL    [Betrag]
```

Offene Lieferantenrechnungen:
```
Verb aus LL / WarenAu           [Betrag]
Verb aus LL / Fahrzeuge          [Betrag]
Verb aus LL / VerwAu             [Betrag]
Verb aus LL / EnergieAu LeistErst  [Betrag]
```
→ Danach: Ford aus LL = 0, Verb aus LL = 0

### 6.5 Bezahlung der vorjährig offenen Rechnungen (nach Rückbuchung)
- Wird wie normaler Zahlungsvorgang gebucht:
```
Bank / WarenEr (o. TransportEr)    [Kundenzahlung]
WarenAu / Bank                      [Lieferantenzahlung]
Fahrzeuge / Bank                     [Fahrzeugzahlung]
```

### 6.6 Forderungsverlust bei Offenposten
- Nur Nettobetrag (exkl. MWST) verbuchen, da Rechnung + UMST nie gebucht wurden:
```
Verluste Ford / ProdER (o. TransportEr)    [Nettobetrag]
```

### 6.7 Offenposten + MWST (Effektive Methode, Nettomethode, vereinnahmtes Entgelt)

**Während Jahr — Zahlungen mit MWST (2 BS):**
```
Bank / TransportEr       [Nettobetrag]
Bank / UMST 2200         [MWST-Betrag]
```
```
EnergieAu LeistErst / Bank    [Nettobetrag]
VST 1170 / Bank                [MWST-Betrag]
```

**Abschluss — Offene Rechnungen mit MWST:**
```
Ford aus LL / TransportEr    [Nettobetrag]
Ford aus LL / UMST 2200      [MWST-Betrag]
```
```
EnergieAu LeistErst / Verb aus LL    [Nettobetrag]
VST 1170 / Verb aus LL               [MWST-Betrag]
```

**Rückbuchung (01.01.):**
```
TransportEr / Ford aus LL    [Nettobetrag]
UMST 2200 / Ford aus LL      [MWST-Betrag]
```

**MWST-Abrechnung mit ESTV:**
```
UMST 2200 / VST 1170    [Saldo]
UMST 2200 / VST 1171    [Saldo]
UMST 2200 / Bank         [Restschuld]
```

---

## 7) Kontobezeichnungen & Abkürzungen

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

## 8) Häufige Fehler (Fallen)

1. **VST 1170 vs. 1171 verwechselt** → 1170 = Kontenklasse 4 (Material, Waren, Energie LeistErst), 1171 = alles andere
2. **Versicherungen mit MWST gebucht** → Versicherungen sind AUSGENOMMEN → kein VST/UMST
3. **Miete Wohnung mit MWST** → ausgenommen. Aber: Miete Büro kann optiert werden.
4. **Bei Offenposten: Rechnung verbucht** → FALSCH. Nur Zahlung buchen. Rechnung = KB.
5. **Skonto bei Offenposten verbucht** → FALSCH. Skonto = KB. Nur Zahlbetrag buchen.
6. **Forderungsverlust bei Offenposten mit MWST** → FALSCH. Nur Nettobetrag, da UMST nie gebucht.
7. **Rückbuchung vergessen** → Am 01.01. MÜSSEN alle Abschlussbuchungen umgekehrt werden.
8. **Kreditkarten-Kommission als UMST-Minderung** → FALSCH. Kommission ≠ Skonto.
9. **Bruttomethode: VST/UMST während Quartal buchen** → FALSCH. Erst Ende Quartal bereinigen.
10. **SSS: Vorsteuer zurückfordern** → FALSCH. Bei SSS gibt es KEINEN Vorsteuerabzug.

---

## 9) Safe-Mode Logik

- **1 Aufgabe sichtbar** → komplett lösen (alle Teilaufgaben)
- **Mehrere Aufgaben sichtbar** → nur die ERSTE lösen, Rest ignorieren
- **Markierte Aufgabe** → nur diese lösen
