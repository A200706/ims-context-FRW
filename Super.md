# FRW KONTEXT — KAP 8 (MWST) + KAP 9 (WARENHANDEL)
# Version: 1.0 | IMS GIBB | Semester 2
# Zweck: Einzige Wissensquelle für 7cal AI. Keine Internetquellen verwenden.

---

## ABKÜRZUNGEN (PFLICHT — immer verwenden)

| Vollständig | Abkürzung | Typ |
|---|---|---|
| Warenaufwand | WarenAu | Aufwand (ER) |
| Warenbestand | WarenBest | Aktiv (Bilanz) |
| Warenertrag | WarenEr | Ertrag (ER) |
| Verbindlichkeiten aus LL | Verb LL | Passiv (Bilanz) |
| Forderungen aus LL | Ford LL | Aktiv (Bilanz) |
| Vorsteuer 1170 | VS 1170 | Aktiv (Bilanz) |
| Vorsteuer 1171 | VS 1171 | Aktiv (Bilanz) |
| Umsatzsteuer | UmsST | Passiv (Bilanz) |
| Kasse | Kasse | Aktiv |
| Bank | Bank | Aktiv |
| Post | Post | Aktiv |
| ESTV | ESTV | — |
| Anfangsbestand | AB | — |
| Endbestand | EB | — |
| Bezugsspesen | BezSp | — |
| Rücksendungen | Rücksd | — |
| Bestandeskorrektur | BestKorr | — |
| Einstandspreis | EP | — |
| Verkaufspreis | VP | — |
| Bruttogewinn | BG | — |
| Erfolgsrechnung | ER | — |

---

## KAP 8: MEHRWERTSTEUER (MWST)

### 8.1 Grundlagen

**Steuersubjekt** = steuerpflichtige Unternehmen
- Bedingung: berufliche/gewerbliche Tätigkeit, selbstständig, nachhaltig, auf Einnahmen gerichtet
- Befreit: Jahresumsatz < CHF 100'000
- Nicht gewinnstrebige Vereine: < CHF 250'000

**Steuerobjekt** = steuerpflichtige Umsätze
- Inland-Leistungen (Lieferungen + Dienstleistungen)
- Einfuhr von Gegenständen aus dem Ausland

**Ausgenommene Leistungen** (keine MWST, kein VS-Abzug):
- Gesundheit, Bildung, Kultur, Versicherungen, Immobilien, Banken

**Befreite Leistungen** (0% MWST, aber VS-Abzug möglich):
- Exporte, Lieferungen ins Ausland

### 8.2 MWST-Sätze

| Satz | Prozent | Anwendung |
|---|---|---|
| Normalsatz | 8.1% | Standardmässig (die meisten Waren/DL) |
| Reduzierter Satz | 2.6% | Lebensmittel, Bücher, Zeitungen, Medikamente |
| Sondersatz | 3.8% | Beherbergungsleistungen (Hotels) |

### 8.3 Vorsteuer und Umsatzsteuer

**Vorsteuer (VS)** = MWST auf EINKÄUFEN
- Konto: Vorsteuer 1170 (Material/DL) oder 1171 (Investitionen/übr. Betriebsau)
- Aktivkonto → Umlaufvermögen → Guthaben gegenüber ESTV
- T-Konto: + links (AB, Zunahmen) | - rechts (Abnahmen, Saldo)

**Umsatzsteuer (US)** = MWST auf VERKÄUFEN
- Konto: Umsatzsteuer 2200
- Passivkonto → kurzfristiges FK → Schuld gegenüber ESTV
- T-Konto: - links (Abnahmen, Saldo) | + rechts (AB, Zunahmen)

**KERNFORMEL:**
```
Abzuliefernde MWST = Umsatzsteuer – Vorsteuer
```
- Normalfall: US > VS → Schuld an ESTV (zahlen)
- Selten: VS > US → Guthaben bei ESTV (zurückfordern)

### 8.4 MWST-Berechnung

**Nettomethode (Standard):**
- Exkl. MWST = 100% (Nettobetrag)
- MWST = 8.1% (oder 2.6% / 3.8%)
- Inkl. MWST = 108.1% (oder 102.6% / 103.8%)

**Umrechnungen:**
- Netto → Brutto: Netto × 1.081
- Brutto → Netto: Brutto / 1.081
- Brutto → MWST: Brutto × 8.1 / 108.1
- Netto → MWST: Netto × 0.081

**MERKE:**
- exkl. = 100% (Basis)
- inkl. > 100% (immer grösser)

### 8.5 Nettomethode — Buchungssätze

#### Einkauf (Beschaffung):
```
Aufwandkonto / Verb LL    [Nettobetrag]
VS 1170      / Verb LL    [MWST-Betrag]
```
Oder bei Barzahlung: Verb LL → Kasse/Bank/Post

#### Verkauf (Absatz):
```
Ford LL / Ertragskonto     [Nettobetrag]
Ford LL / UmsST            [MWST-Betrag]
```
Oder bei Barzahlung: Ford LL → Kasse/Bank/Post

#### Rabatt vom Lieferanten (Einkaufsrabatt):
```
Verb LL / Aufwandkonto     [Nettobetrag]
Verb LL / VS 1170          [MWST-Betrag]
```
(Umkehrbuchung des Einkaufs)

#### Rabatt an Kunden (Verkaufsrabatt):
```
Ertragskonto / Ford LL     [Nettobetrag]
UmsST        / Ford LL     [MWST-Betrag]
```
(Umkehrbuchung des Verkaufs)

#### Skonto bei Zahlung (gleiche Logik wie Rabatt):
- Einkauf-Skonto: Verb LL / Aufwandkonto + Verb LL / VS 1170
- Verkauf-Skonto: Ertragskonto / Ford LL + UmsST / Ford LL

#### MWST-Abrechnung bei ESTV (Nettomethode):
```
1. UmsST / VS 1170     [VS-Betrag]     (Verrechnung)
2. UmsST / Post|Bank   [Rest = US-VS]  (Zahlung)
```

### 8.6 Saldosteuersatzmethode

- Beträge werden BRUTTO gebucht (inkl. MWST)
- KEINE Vorsteuer-/Umsatzsteuer-Konten nötig
- Steuerschuld = Total Umsatz (inkl. MWST) × Saldosteuersatz
- Beispiel: Umsatz 748'000 inkl. 8.1%, Saldosteuersatz 3.7%:
  - 748'000 × 3.7% = 27'676

**Buchung Abrechnung (Saldosteuersatzmethode):**
```
Ertragskonto / UmsST      [Steuerbetrag]
UmsST        / Post|Bank  [Steuerbetrag]
```

---

## KAP 9: WARENHANDELSUNTERNEHMEN

### 9.1 Die 3 Schlüsselkonten

| Konto | Typ | Wo | Funktion |
|---|---|---|---|
| Warenbestand | Aktivkonto | Bilanz (Umlaufvermögen) | Lagerwert (EP) |
| Warenaufwand | Aufwandkonto | ER (Aufwand) | Einstandswert verkaufter Waren |
| Warenertrag | Ertragskonto | ER (Ertrag) | Nettoerlös aus Verkäufen |

**Bruttogewinn = Saldo WarenEr − Saldo WarenAu**

### 9.2 Methoden der Verbuchung

#### Methode OHNE laufende Inventur (Standard im Unterricht):
- WarenAu: Verbuchung der Einkäufe (zu EP)
- WarenEr: Verbuchung der Verkäufe (zu VP)
- WarenBest: RUHENDES KONTO → keine Buchungen während Periode
- Erst beim Abschluss: Bestandeskorrektur (Inventur)
- Bestand/Verbrauch NICHT laufend bekannt
- Geeignet bei: tiefem Lager, fehlendem Informatiksystem

#### Methode MIT laufender Inventur:
- WarenAu: Lagerabgang bei Verkäufen (zu EP)
- WarenEr: Verkäufe (zu VP)
- WarenBest: Einkäufe UND Lagerabgang (zu EP)
- Bestand/Verbrauch JEDERZEIT bekannt
- Geeignet bei: hohem Lager, Lagerbewirtschaftungssystem

### 9.3 Buchungssätze — OHNE laufende Inventur

#### Einkaufsseite (alles über WarenAu):
```
Wareneinkauf auf Kredit:    WarenAu  / Verb LL    [EP]
Bezugsspesen auf Rechnung:  WarenAu  / Verb LL    [Betrag]
Bezugsspesen bar:           WarenAu  / Kasse      [Betrag]
Rabatt von Lieferanten:     Verb LL  / WarenAu    [Betrag]
Rücksendung an Lieferant:   Verb LL  / WarenAu    [Betrag]
```

#### Verkaufsseite (alles über WarenEr):
```
Warenverkauf auf Kredit:    Ford LL  / WarenEr    [VP]
Warenverkauf bar:           Kasse    / WarenEr    [VP]
Versandkosten bar:          WarenEr  / Kasse      [Betrag]
Rabatte an Kunden:          WarenEr  / Ford LL    [Betrag]
Rücksendung von Kunden:     WarenEr  / Ford LL    [Betrag]
```

#### Bestandeskorrektur (Abschluss):
```
Abnahme (EB < AB):  WarenAu   / WarenBest   [AB − EB]
Zunahme (EB > AB):  WarenBest / WarenAu     [EB − AB]
```

**MERKE:** Bestandeskorrektur hat KEINE MWST!

### 9.4 Buchungssätze — OHNE laufende Inventur + MIT MWST

Kombination KAP 8 + KAP 9. Jede Buchung wird in Netto + MWST aufgeteilt:

#### Wareneinkauf auf Kredit (inkl. 8.1% MWST):
```
WarenAu  / Verb LL    [Netto = Brutto/1.081]
VS 1170  / Verb LL    [MWST = Brutto×8.1/108.1]
```

#### Bezugsspesen auf Rechnung (inkl. MWST):
```
WarenAu  / Verb LL    [Netto]
VS 1170  / Verb LL    [MWST]
```

#### Rabatt von Lieferanten (inkl. MWST):
```
Verb LL  / WarenAu    [Netto]
Verb LL  / VS 1170    [MWST]
```

#### Warenverkauf auf Kredit (inkl. 8.1% MWST):
```
Ford LL  / WarenEr    [Netto]
Ford LL  / UmsST      [MWST]
```

#### Rabatte/Rücksendungen von Kunden (inkl. MWST):
```
WarenEr  / Ford LL    [Netto]
UmsST    / Ford LL    [MWST]
```

#### Bestandeskorrektur (KEINE MWST!):
```
Abnahme: WarenAu   / WarenBest   [Differenz]
Zunahme: WarenBest / WarenAu     [Differenz]
```

### 9.5 T-Konten Aufbau

#### Warenbestand (Aktivkonto):
```
+  Warenbestand  −
AB          | Abnahme
Zunahme     | 
            | EB (Saldo)
```

#### Warenaufwand (Aufwandkonto):
```
+  Warenaufwand  −
Einkäufe    | Rabatte Lief.
BezSpesen   | Rücksd Lief.
Abnahme     | Zunahme
            | Saldo = Einstandswert
```

#### Warenertrag (Ertragskonto):
```
−  Warenertrag  +
VersandK    | Verkäufe
Rabatte Ku  | 
Rücksd Ku   | 
Saldo=Nettoerl |
```

### 9.6 Schlüsselformeln

```
Einstandswert eingekaufter Waren = Einkäufe + BezSpesen − Rabatte Lief.
Einstandswert verkaufter Waren   = Saldo WarenAu
Nettoerlös                       = Saldo WarenEr
Bruttogewinn                     = Saldo WarenEr − Saldo WarenAu
Bestandesänderung                = EB − AB
  → positiv = Zunahme (WarenBest / WarenAu)
  → negativ = Abnahme (WarenAu / WarenBest)
```

### 9.7 Beispiel komplett (ohne lfd. Inventur, ohne MWST)

Gegeben: AB=140, Einkäufe=930, BezSp=60, Rabatt Lief.=40, Verkäufe=1'510, VersandK=50, Rabatt Ku=30, Rücksd Ku=15, EB=110

| Nr | Buchung | Betrag |
|---|---|---|
| 1 | AB Waren | 140 |
| 2 | WarenAu / Verb LL | 930 |
| 3 | WarenAu / Verb LL | 60 |
| 4 | Verb LL / WarenAu | 40 |
| 5 | Ford LL / WarenEr | 1'510 |
| 6 | WarenEr / Kasse | 50 |
| 7 | WarenEr / Ford LL | 30 |
| 8 | WarenEr / Ford LL | 15 |
| 9 | WarenAu / WarenBest | 30 |

Abnahme = 140−110 = 30
Saldo WarenAu = 980, Saldo WarenEr = 1'415
BG = 1'415 − 980 = 435

### 9.8 Beispiel komplett (ohne lfd. Inventur, MIT MWST 8.1%)

Gegeben: AB=45'000, Einkäufe inkl.=345'920, Rabatt Lief. inkl.=17'296, Verkäufe inkl.=713'460, EB=68'000

| Nr | Buchung | Betrag |
|---|---|---|
| 1 | AB | 45'000 |
| 2 | WarenAu / Verb LL | 320'000 |
| 2 | VS 1170 / Verb LL | 25'920 |
| 3 | Verb LL / WarenAu | 16'000 |
| 3 | Verb LL / VS 1170 | 1'296 |
| 4 | Ford LL / WarenEr | 660'000 |
| 4 | Ford LL / UmsST | 53'460 |
| 5 | WarenBest / WarenAu | 23'000 |

Zunahme = 68'000−45'000 = 23'000 (keine MWST!)
Saldo WarenAu = 281'000, Saldo WarenEr = 660'000
BG = 660'000 − 281'000 = 379'000

---

## AUSGABEREGELN (FÜR AI)

### Format:
1. Zuerst: Aufgaben-Nr. (z.B. "A3)" oder "Nr.2")
2. Dann: Buchungssatz als Soll / Haben + Betrag
3. Dann: Stichpunkte falls nötig (Saldo, Bilanz/ER-Position)
4. Max 12 Zeilen pro Antwort

### Stil:
- Schreibe wie ein Schüler, nicht wie ein Lehrer
- Kein Erklärtext, keine Theorie, keine Motivation
- Nur Antworten die Punkte bringen
- Sprache: Deutsch (Schweizer FRW-Stil)

### Abkürzungen:
- IMMER die Tabelle oben verwenden
- Nie "Verbindlichkeiten aus Lieferungen und Leistungen" ausschreiben
- Nie "Warenaufwand" voll ausschreiben → "WarenAu"

### Bei Unsicherheit:
- Wenn Daten unklar → "Daten unklar" schreiben
- Nie raten oder erfinden
- Standardmässig Normalsatz 8.1% verwenden falls kein Satz angegeben
