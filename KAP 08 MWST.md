# FRW MWST MASTER CONTEXT (Schweiz - Kapitel 8)

[[SYSTEM_CONFIG]]
- **Currency:** CHF (Schweizer Franken).
- **Rounding:** 0.05 (5 Rappen).
- **Language:** Deutsch (Exam-Style, A2-B1 Level).
- **Date Format:** DD.MM.YYYY.

---

## 1. STEUERSÄTZE & OBJEKTE (Die Hard-Facts)

### [cite_start]1.1 Aktuelle Sätze (Stand 2024/PDF) [cite: 109]
| Satz | Name | Gilt für (Beispiele) |
| :--- | :--- | :--- |
| **8.1%** | **Normalsatz** | Alle übrigen Lieferungen/Dienstleistungen (Autos, Möbel, Beratung, Strom, Benzin, Alkohol/Gastro). |
| **2.6%** | **Reduzierter Satz** | Nahrungsmittel (Essen/Trinken ohne Gastro), Medikamente, Zeitungen, Bücher, Leitungswasser, Pflanzen, Dünger. |
| **3.8%** | **Sondersatz** | Beherbergung (Hotellerie: Übernachtung + Frühstück). |
| **0.0%** | **Steuerbefreit** | Exporte (Ausfuhr). **WICHTIG:** Vorsteuerabzug ist ERLAUBT! |
| **0.0%** | **Ausgenommen** | Banken, Versicherungen, Immobilienverkauf, Ärzte, Bildung. **WICHTIG:** Vorsteuerabzug ist VERBOTEN! |

### [cite_start]1.2 Begriffe [cite: 19, 20, 35, 38]
- **Umsatzsteuer:** Schuld gegenüber ESTV (auf Verkäufen).
- **Vorsteuer:** Guthaben gegenüber ESTV (auf Einkäufen).
- **Steuersubjekt:** Das Unternehmen (muss abrechnen).
- **Steuerobjekt:** Die Leistung (wird besteuert).

---

## [cite_start]2. KONTEN-LOGIK (Nettomethode) [cite: 245, 246, 252, 253]
**CRITICAL:** Du musst das richtige Vorsteuer-Konto wählen!

| Konto | Name | Verwendung (Regel) | Beispiele |
| :--- | :--- | :--- | :--- |
| **1170** | Vorsteuer Material/Waren | Alles, was **Klasse 4** (Aufwand für Produktion/Handel) betrifft. | Holz (Schreiner), Handelswaren, Rohstoffe, Energie für Produktion. |
| **1171** | Vorsteuer Invest/Übriges | Alles, was **Klasse 1** (Investitionen) oder **Klasse 6** (Übriger Aufwand) betrifft. | Maschinen, Fahrzeuge, Büromaterial, Werbung, Beratung, Benzin für Firmenwagen. |
| **2200** | Umsatzsteuer (Passiv) | Geschuldete Steuer auf Verkäufen (Klasse 3). | Verkauf von Produkten, Dienstleistungen, Verkauf von Anlagevermögen. |

---

## 3. BUCHUNGS-TEMPLATES (Nettomethode)

### [cite_start]3.1 Einkauf (Rechnung erhalten) [cite: 198, 200, 201]
*Beispiel: Kauf Rohmaterial CHF 2'162 (inkl. 8.1%) auf Kredit.*
1. **Nettobetrag:** `Materialaufwand / VLL` : 2'000.00
2. **Vorsteuer:** `Vorsteuer 1170 / VLL` : 162.00

### [cite_start]3.2 Verkauf (Rechnung gestellt) [cite: 282, 286, 291]
*Beispiel: Verkauf Möbel CHF 4'324 (inkl. 8.1%) auf Kredit.*
1. **Nettobetrag:** `FLL / Produktionserlöse` : 4'000.00
2. **Umsatzsteuer:** `FLL / Umsatzsteuer` : 324.00

### [cite_start]3.3 Rabatte / Skonto / Rücksendungen [cite: 330, 367]
*Regel:* Buche genau **umgekehrt** zur Originalbuchung (Storno).
*Beispiel: Wir zahlen Einkauf unter Abzug von Skonto.*
1. **Nettoskonto:** `VLL / Materialaufwand`
2. **Steuerskonto:** `VLL / Vorsteuer 1170`
3. **Zahlung:** `VLL / Bank` (Restbetrag)

### [cite_start]3.4 Abrechnung ESTV (Quartalsende) [cite: 302, 311]
*Ziel: Vorsteuerkonten auf 0 setzen und Differenz zahlen.*
1. `Umsatzsteuer / Vorsteuer 1170` (Saldo 1170 ausbuchen)
2. `Umsatzsteuer / Vorsteuer 1171` (Saldo 1171 ausbuchen)
3. `Umsatzsteuer / Bank` (Restschuld überweisen)

---

## [cite_start]4. SALDOSTEUERSATZ-METHODE (SSS) [cite: 370, 372, 382]

### 4.1 Die Regeln
- **Kein Vorsteuerabzug!** (Weder Konto 1170 noch 1171 führen).
- **Abrechnung:** 2x pro Jahr (Semester).
- [cite_start]**Buchung:** Unter dem Jahr immer **BRUTTO** (inkl. MWST) in den Ertrag buchen[cite: 393].

### [cite_start]4.2 Die Branchen-Liste (SSS-Sätze) [cite: 382]
*Wenn die Aufgabe eine Branche nennt, nimm BLIND diesen Satz:*
- **0.1%**: Futtermittel, Kiosk, Zeitungen.
- **0.6%**: **Bäckerei**, **Buchhandlung**, Heizöl, Weinhandel.
- **1.3%**: (Selten in Aufgaben).
- **2.1% - 3.7%**: Bau, Schreiner, Handwerker.
- **5.3%**: **Tearoom**, **Coiffeur**, Hundesalon, Fotostudio, Fitness.
- **6.2%**: **Treuhand**, **Anwälte**, Architekten, Übersetzer (Dienstleister).
- **6.8%**: Personalverleih.

### [cite_start]4.3 SSS-Berechnung & Buchung [cite: 404, 408]
1. **Steuerschuld:** `Brutto-Semesterumsatz * SSS-Satz / 100`
2. **Buchung (Semesterende):** `Ertrag / Umsatzsteuer` (Nur der berechnete Betrag!)
3. **Zahlung:** `Umsatzsteuer / Bank`

---

## [cite_start]5. RECHEN-FORMELN (Der Spickzettel) [cite: 166, 188]

### 5.1 Von "Inklusive" (Brutto) rechnen
*Der Preis ist 100% + Satz (z.B. 108.1%).*
- **Netto suchen:** `Brutto / 1.081`
- **Steuer suchen:** `Brutto / 108.1 * 8.1`

### 5.2 Von "Exklusive" (Netto) rechnen
*Der Preis ist 100%.*
- **Brutto suchen:** `Netto * 1.081`
- **Steuer suchen:** `Netto * 0.081`

---

## [cite_start]6. BELEG-CHECKLISTE (Muss drauf sein) [cite: 144, 145, 146, 147, 148, 149]
1. **Wer leistet?** (Name, Ort, **MWST-Nr.**).
2. [cite_start]**Wer empfängt?** (Name, Ort) -> Ausnahme: Kassenzettel < 400 CHF[cite: 178].
3. **Wann?** (Datum/Zeitraum).
4. **Was?** (Art/Menge).
5. **Wieviel?** (Betrag).
6. **Steuer?** (Satz in % und Betrag, oder Vermerk "inkl. X% MWST").
