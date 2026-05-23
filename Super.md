# SUPER-MD — FRW KAP 4 + KAP 11 (Mehrwertsteuer + Offenposten-Buchhaltung)

---

## QR — QUICK ROUTER

Lies die Aufgabe → erkenne den Typ → springe zum Block:

| Schluesselwoerter | Typ | Block |
|---|---|---|
| MWST, Vorsteuer, Umsatzsteuer, Steuersatz, 8.1%, 2.6%, 3.8% | MWST-Buchung (Netto/Brutto) | T-MWST |
| Brutto, Netto, exkl., inkl., MWST berechnen, MWST-Betrag | MWST-Rechnung | T-MWST-CALC |
| Fahrzeug, Maschine, Investition, Konto 1171, Mobiliar, EDV | Investitions-Buchung | T-FAHR |
| Offenposten, Rechnungen nicht verbucht, Abschluss, Eroeffnung | Offenposten-Methode | T-OP |
| Abschreibung, Abschreibungssatz, kalkulatorisch, definitiv | Abschreibung mit MWST | T-ABSCH |
| T-Konto, Kontodarstellung, Saldo, Abschluss Konto | T-Konto zeichnen | T-KONTOP |
| Saldosteuersatz, SSS, vereinfacht, keine Vorsteuer | Saldosteuersatz-Methode | T-MWST (SSS) |
| Rabatt, Skonto, Gutschrift, Rueckgabe, Preisminderung | MWST bei Korrekturen | T-MWST |
| MWST-Abrechnung, Formular, Umsatz deklarieren, Zahllast | Abrechnung erstellen | T-MWST |

**METHODEN-CHECK** (vor dem Buchen!):
- Aufgabe sagt "Nettomethode" oder zeigt 2 Buchungssaetze → **MODUS-NETTO**
- Aufgabe sagt "Bruttomethode" oder zeigt 1 Buchungssatz → **MODUS-BRUTTO**
- Aufgabe sagt "Saldosteuersatz" oder "keine Vorsteuer" → **MODUS-SSS**
- Wenn nicht angegeben → Standard = **MODUS-NETTO**

---

## MI — MICRO INDEX

- QR: Quick Router
- X-MWST: Steuersaetze-Referenz
- X-CONTEN: Kontenplan-Referenz
- T-MWST-CALC: MWST-Berechnungsschema
- T-MWST: Buchungssaetze (Netto / Brutto / SSS / Abrechnung)
- T-FAHR: Fahrzeuge und Investitionen
- T-OP: Offenposten-Buchhaltung
- T-ABSCH: Abschreibungen mit MWST
- T-KONTOP: T-Konten-Darstellung
- X-TRAP: Fallen und haeufige Fehler

---

## WF — WORKFLOW (fuer jede Aufgabe)

```
1) Aufgabe lesen → Typ erkennen (QR)
2) Methode bestimmen (Netto / Brutto / SSS)
3) Steuersatz bestimmen (X-MWST)
4) Relevante Konten identifizieren (X-CONTEN)
5) MWST-Betrag berechnen (T-MWST-CALC)
6) Buchungssatz aufstellen (T-MWST / T-FAHR / T-OP)
7) Kontrolle: Soll = Haben? MWST korrekt?
```

---

## AR — ANSWER RULES

### Formatregeln (STRIKT)
- PLAIN TEXT ONLY. Kein LaTeX. Kein Markdown.
- Jede Zeile beginnt nummeriert: 1) 2) 3) ...
- Buchungssatz-Format: Soll-Konto / Haben-Konto / Betrag
- Brueche als Wortbruch: "a btel" (z.B. "8.1 Hundertstel")
- Jede Rechenoperation mit Tag am Ende: [*1.081], [:108.1], [*8.1], etc.
- Keine Meta-Texte, kein "Zusammenfassend"
- Maximal 1 Buchung pro Zeile

---

## X-MWST — STEUERSAETZE-REFERENZ

$\textbf{Aktuelle Saetze (ab 2024):}$
$\text{Normalsatz} = 8{,}1\%$
$\text{Reduzierter Satz} = 2{,}6\%$
$\text{Sondersatz (Beherbergung)} = 3{,}8\%$

$\textbf{Fruehere Saetze (bis 2023):}$
$\text{Normalsatz} = 7{,}7\%$
$\text{Reduzierter Satz} = 2{,}5\%$
$\text{Sondersatz (Beherbergung)} = 3{,}7\%$

$\textbf{Saldosteuersaetze (Beispiele):}$
$\text{Branchenabhaengig, z.B. } 0{,}1\% \text{ bis } 6{,}5\%$
$\text{Typisch in Aufgaben: } 3{,}7\% \text{ oder } 6{,}5\%$

$\textbf{Befreit / Ausgenommen:}$
$\text{Befreit (Art. 23 MWSTG):} \quad 0\% \text{, Vorsteuer-Abzug moeglich}$
$\text{Ausgenommen (Art. 21 MWSTG):} \quad \text{keine MWST, KEIN Vorsteuer-Abzug}$

$\textbf{Umrechnungsfaktoren (Normalsatz 8.1\%):}$
$\text{Netto} \to \text{Brutto:} \quad \times 1{,}081$
$\text{Brutto} \to \text{Netto:} \quad \div 1{,}081$
$\text{Brutto} \to \text{MWST:} \quad \times \frac{8{,}1}{108{,}1}$
$\text{Netto} \to \text{MWST:} \quad \times 0{,}081$

---

## X-CONTEN — KONTENPLAN-REFERENZ

$\textbf{MWST-Konten:}$
$\text{1170 Vorsteuer auf Materialaufwand (VST Material)} \quad \text{Aktiv, Guthaben bei ESTV}$
$\text{1171 Vorsteuer auf Investitionen/uebrigen Aufwand (VST Inv.)} \quad \text{Aktiv, Guthaben bei ESTV}$
$\text{2200 Umsatzsteuer (UST)} \quad \text{Passiv, Schuld gegenueber ESTV}$
$\text{2201 Umsatzsteuer auf vereinnahmtem Entgelt} \quad \text{Passiv (bei SSS)}$

$\textbf{Vorsteuer-Zuordnung:}$
$\text{1170 VST} \to \text{Kontenklasse 4 (Materialaufwand, Warenaufwand)}$
$\text{1171 VST} \to \text{Alle anderen Klassen (Personalaufwand, Raumaufwand, Fahrzeuge, Maschinen, Mobiliar)}$

$\textbf{Haeufig verwendete Konten:}$
$\text{1000 Kasse}$
$\text{1020 Bank}$
$\text{1100 Forderungen aus LL (Debitoren)}$
$\text{1200 Warenvorrat / Vorraete}$
$\text{1500 Maschinen und Apparate}$
$\text{1510 Mobiliar und Einrichtungen}$
$\text{1520 Bueromaschinen / EDV}$
$\text{1530 Fahrzeuge}$
$\text{2000 Verbindlichkeiten aus LL (Kreditoren)}$
$\text{3200 Warenaufwand}$
$\text{4000 Materialaufwand}$
$\text{4400 Energieaufwand}$
$\text{5000 Personalaufwand / Lohnaufwand}$
$\text{6000 Raumaufwand / Mietaufwand}$
$\text{6100 Unterhalt / Reparaturen}$
$\text{6200 Fahrzeugaufwand}$
$\text{6500 Verwaltungsaufwand}$
$\text{6600 Werbeaufwand}$
$\text{3000 Produktionsertrag / Warenertrag}$
$\text{3200 Handelsertrag (Warenertrag)}$
$\text{3400 Dienstleistungsertrag}$

---

## T-MWST-CALC — MWST-BERECHNUNGSSCHEMA

$\textbf{Netto → Brutto (Aufschlagen):}$
$\text{Brutto} = \text{Netto} \times 1{,}081 \quad \text{(bei 8.1\%)}$
$\text{Brutto} = \text{Netto} \times 1{,}026 \quad \text{(bei 2.6\%)}$
$\text{Brutto} = \text{Netto} \times 1{,}038 \quad \text{(bei 3.8\%)}$

$\textbf{Brutto → Netto (Herausrechnen):}$
$\text{Netto} = \frac{\text{Brutto}}{1{,}081} \quad \text{(bei 8.1\%)}$
$\text{Netto} = \frac{\text{Brutto}}{1{,}026} \quad \text{(bei 2.6\%)}$
$\text{Netto} = \frac{\text{Brutto}}{1{,}038} \quad \text{(bei 3.8\%)}$

$\textbf{MWST-Betrag aus Brutto:}$
$\text{MWST} = \text{Brutto} \times \frac{8{,}1}{108{,}1} \quad \text{(bei 8.1\%)}$
$\text{MWST} = \text{Brutto} \times \frac{2{,}6}{102{,}6} \quad \text{(bei 2.6\%)}$
$\text{MWST} = \text{Brutto} \times \frac{3{,}8}{103{,}8} \quad \text{(bei 3.8\%)}$

$\textbf{MWST-Betrag aus Netto:}$
$\text{MWST} = \text{Netto} \times 0{,}081 \quad \text{(bei 8.1\%)}$
$\text{MWST} = \text{Netto} \times 0{,}026 \quad \text{(bei 2.6\%)}$
$\text{MWST} = \text{Netto} \times 0{,}038 \quad \text{(bei 3.8\%)}$

$\textbf{Schema: Netto = 100\%, MWST = p\%, Brutto = (100+p)\%}$
$\text{Beispiel 8.1\%: Netto = 100\%, MWST = 8.1\%, Brutto = 108.1\%}$
$\text{Kontrolle: Netto + MWST = Brutto (immer pruefen!)}$

$\textbf{Rundung:}$
$\text{MWST-Betraege auf 5 Rappen runden (kaufmaennisch)}$

---

## T-MWST — BUCHUNGSSAETZE

### NETTOMETHODE (2 Buchungssaetze pro Transaktion)

$\textbf{Einkauf Waren (Material, Kontenklasse 4):}$
$\text{1) Warenaufwand (4000/3200)} \quad / \quad \text{Verb aus LL (2000)} \quad \text{Nettobetrag}$
$\text{2) VST Material (1170)} \quad / \quad \text{Verb aus LL (2000)} \quad \text{MWST-Betrag}$

$\textbf{Einkauf Investition/uebr. Aufwand (Klasse 1,5,6):}$
$\text{1) Aufwandkonto (z.B. 6000 Miete)} \quad / \quad \text{Verb aus LL (2000)} \quad \text{Nettobetrag}$
$\text{2) VST Investitionen (1171)} \quad / \quad \text{Verb aus LL (2000)} \quad \text{MWST-Betrag}$

$\textbf{Verkauf:}$
$\text{1) Ford aus LL (1100)} \quad / \quad \text{Ertragskonto (3000/3400)} \quad \text{Nettobetrag}$
$\text{2) Ford aus LL (1100)} \quad / \quad \text{UST (2200)} \quad \text{MWST-Betrag}$

$\textbf{Beispiel: Wareneinkauf CHF 5000 netto + 8.1\% MWST:}$
$\text{1) Warenaufwand / Verb aus LL \quad CHF 5000.00}$
$\text{2) VST 1170 / Verb aus LL \quad CHF 405.00} \quad [5000 \times 0.081]$
$\text{Kreditoren-Saldo total: CHF 5405.00}$

$\textbf{Beispiel: Warenverkauf CHF 12000 netto + 8.1\% MWST:}$
$\text{1) Ford aus LL / Warenertrag \quad CHF 12000.00}$
$\text{2) Ford aus LL / UST 2200 \quad CHF 972.00} \quad [12000 \times 0.081]$
$\text{Debitoren-Saldo total: CHF 12972.00}$

### BRUTTOMETHODE (1 Buchungssatz pro Transaktion)

$\textbf{Einkauf (inkl. MWST):}$
$\text{Warenaufwand (4000)} \quad / \quad \text{Verb aus LL (2000)} \quad \text{Bruttobetrag (inkl. MWST)}$

$\textbf{Verkauf (inkl. MWST):}$
$\text{Ford aus LL (1100)} \quad / \quad \text{Warenertrag (3000)} \quad \text{Bruttobetrag (inkl. MWST)}$

$\textbf{Periodenende — MWST herausloesen:}$
$\text{Einkauf: VST 1170 / Warenaufwand \quad MWST-Betrag} \quad [\text{Brutto} \times \frac{8.1}{108.1}]$
$\text{Verkauf: Warenertrag / UST 2200 \quad MWST-Betrag} \quad [\text{Brutto} \times \frac{8.1}{108.1}]$

$\textbf{Beispiel Brutto: Wareneinkauf CHF 5405 brutto (8.1\%):}$
$\text{Laufend: Warenaufwand / Verb aus LL \quad CHF 5405.00}$
$\text{Periodenende: VST 1170 / Warenaufwand \quad CHF 405.00} \quad [5405 \times 8.1 / 108.1]$

### SALDOSTEUERSATZ-METHODE (SSS)

$\textbf{Merkmale:}$
$\text{- Keine Vorsteuer wird verbucht (kein Konto 1170/1171)}$
$\text{- Einkauf IMMER brutto gebucht}$
$\text{- Verkauf brutto gebucht}$
$\text{- Halbjaehrliche Abrechnung}$
$\text{- Tieferer Saldosteuersatz (z.B. 6.5\%, 3.7\%)}$

$\textbf{Laufende Buchung (Einkauf):}$
$\text{Warenaufwand / Verb aus LL \quad Bruttobetrag}$

$\textbf{Laufende Buchung (Verkauf):}$
$\text{Ford aus LL / Warenertrag \quad Bruttobetrag (inkl. MWST)}$

$\textbf{Halbjahres-Abrechnung:}$
$\text{Warenertrag / UST 2200 \quad [Bruttoumsatz} \times \text{Saldosteuersatz]}$
$\text{Beispiel: Umsatz CHF 200000 brutto, SSS 6.5\%:}$
$\text{Warenertrag / UST 2200 \quad CHF 13000.00} \quad [200000 \times 0.065]$

### MWST-ABRECHNUNG (Effektive Methode)

$\textbf{Formel: Zahllast = UST - VST (1170 + 1171)}$

$\text{UST 2200 (Schuld) \quad - \quad VST 1170 + VST 1171 (Guthaben) \quad = \quad Zahllast}$

$\textbf{Fall 1: Zahllast (UST > VST) → Unternehmen schuldet ESTV:}$
$\text{1) VST 1170 saldieren: UST 2200 / VST 1170 \quad Saldo 1170}$
$\text{2) VST 1171 saldieren: UST 2200 / VST 1171 \quad Saldo 1171}$
$\text{3) Zahlung: UST 2200 / Bank 1020 \quad Restsaldo (= Zahllast)}$

$\textbf{Fall 2: Vorsteuer-Ueberschuss (VST > UST) → ESTV schuldet Unternehmen:}$
$\text{1) UST saldieren: UST 2200 / VST 1170 \quad Saldo 2200}$
$\text{2) Ggf. Rest: UST 2200 / VST 1171 \quad verbleibend}$
$\text{3) Gutschrift: Bank 1020 / VST 1170 (oder 1171) \quad Restsaldo}$

$\textbf{Beispiel:}$
$\text{UST 2200 = CHF 8100, VST 1170 = CHF 2025, VST 1171 = CHF 810}$
$\text{Zahllast = 8100 - 2025 - 810 = CHF 5265}$
$\text{1) UST 2200 / VST 1170 \quad CHF 2025}$
$\text{2) UST 2200 / VST 1171 \quad CHF 810}$
$\text{3) UST 2200 / Bank 1020 \quad CHF 5265}$

### RABATT / SKONTO MIT MWST

$\textbf{Rabatt auf Einkauf (Nettomethode):}$
$\text{1) Verb aus LL / Warenaufwand \quad Nettobetrag des Rabatts}$
$\text{2) Verb aus LL / VST 1170 \quad MWST auf Rabatt}$
$\text{(Umgekehrte Buchung des Einkaufs)}$

$\textbf{Skonto auf Einkauf (Nettomethode):}$
$\text{1) Verb aus LL / Bank \quad Zahlungsbetrag (nach Abzug Skonto)}$
$\text{2) Verb aus LL / Warenaufwand \quad Netto-Skonto}$
$\text{3) Verb aus LL / VST 1170 \quad MWST auf Skonto}$

$\textbf{Skonto auf Verkauf (Nettomethode):}$
$\text{1) Bank / Ford aus LL \quad Zahlungseingang}$
$\text{2) Warenertrag / Ford aus LL \quad Netto-Skonto}$
$\text{3) UST 2200 / Ford aus LL \quad MWST auf Skonto}$

---

## T-FAHR — FAHRZEUGE UND INVESTITIONEN

$\textbf{Kauf Fahrzeug (Nettomethode):}$
$\text{1) Fahrzeuge 1530 / Verb aus LL (2000) \quad Nettobetrag}$
$\text{2) VST 1171 / Verb aus LL (2000) \quad MWST-Betrag}$
$\text{Hinweis: VST 1171 (nicht 1170!) weil Kontenklasse 1}$

$\textbf{Kauf Maschine:}$
$\text{1) Maschinen 1500 / Verb aus LL (2000) \quad Nettobetrag}$
$\text{2) VST 1171 / Verb aus LL (2000) \quad MWST-Betrag}$

$\textbf{Kauf Mobiliar:}$
$\text{1) Mobiliar 1510 / Verb aus LL (2000) \quad Nettobetrag}$
$\text{2) VST 1171 / Verb aus LL (2000) \quad MWST-Betrag}$

$\textbf{Kauf EDV / Bueromaschinen:}$
$\text{1) EDV 1520 / Verb aus LL (2000) \quad Nettobetrag}$
$\text{2) VST 1171 / Verb aus LL (2000) \quad MWST-Betrag}$

$\textbf{Fahrzeugaufwand (Reparatur, Service, Benzin):}$
$\text{1) Fahrzeugaufwand 6200 / Verb aus LL (2000) \quad Nettobetrag}$
$\text{2) VST 1171 / Verb aus LL (2000) \quad MWST-Betrag}$
$\text{Hinweis: Fahrzeugaufwand = Klasse 6 → VST 1171}$

$\textbf{Merke: VST-Zuordnung bei Investitionen:}$
$\text{Kontenklasse 4 (Material/Waren) → VST 1170}$
$\text{Alle anderen Klassen (1,5,6,etc.) → VST 1171}$

$\textbf{Verkauf Fahrzeug (Nettomethode):}$
$\text{1) Ford aus LL (1100) / Fahrzeuge 1530 \quad Nettobetrag}$
$\text{2) Ford aus LL (1100) / UST 2200 \quad MWST-Betrag}$

---

## T-OP — OFFENPOSTEN-BUCHHALTUNG (KAP 11)

$\textbf{Grundprinzip:}$
$\text{Rechnungen werden NICHT verbucht wenn sie eintreffen.}$
$\text{NUR Zahlungen (Kasse/Bank) werden laufend gebucht.}$
$\text{Am Periodenende: Offene Rechnungen nachbuchen.}$

$\textbf{Laufende Buchungen (nur Zahlungen):}$
$\text{Einkauf bezahlt: Warenaufwand / Bank \quad Betrag}$
$\text{Verkauf erhalten: Bank / Warenertrag \quad Betrag}$

$\textbf{Abschluss (Periodenende) — Offene Rechnungen buchen:}$
$\text{Offene Lieferantenrechnungen (wir schulden):}$
$\text{Warenaufwand / Verb aus LL (2000) \quad Betrag}$
$\text{Offene Kundenrechnungen (Kunden schulden uns):}$
$\text{Ford aus LL (1100) / Warenertrag \quad Betrag}$

$\textbf{Eroeffnung (neue Periode) — Rueckbuchung:}$
$\text{Verb aus LL (2000) / Warenaufwand \quad Betrag}$
$\text{Warenertrag / Ford aus LL (1100) \quad Betrag}$
$\text{(Exakt umgekehrte Buchungen vom Abschluss)}$

$\textbf{Warum Rueckbuchung?}$
$\text{Wenn die Rechnung spaeter bezahlt wird, wird sie normal gebucht.}$
$\text{Ohne Rueckbuchung waere der Aufwand/Ertrag doppelt erfasst.}$

$\textbf{Offenposten + MWST:}$
$\text{Bei Offenposten-Methode → Abrechnung nach vereinnahmtem Entgelt.}$
$\text{MWST wird erst bei Zahlung geschuldet/abziehbar.}$
$\text{Haeufig kombiniert mit Saldosteuersatz-Methode.}$

$\textbf{Offenposten + Fremdwaehrung:}$
$\text{Zahlungen: Tageskurs am Zahlungstag}$
$\text{Offene Rechnungen am Jahresende: Bilanzkurs}$
$\text{Kursdifferenzen ueber Konto Kursdifferenzen buchen}$

$\textbf{Beispiel Offenposten-Zyklus:}$
$\text{1. Quartal laufend: Warenaufwand / Bank CHF 45000 (bezahlte Rechnungen)}$
$\text{Abschluss: Warenaufwand / Verb aus LL CHF 8000 (offene Rechnungen)}$
$\text{Eroeffnung Q2: Verb aus LL / Warenaufwand CHF 8000 (Rueckbuchung)}$
$\text{Q2 laufend: Warenaufwand / Bank CHF 52000 (inkl. der CHF 8000 von Q1)}$

---

## T-ABSCH — ABSCHREIBUNGEN MIT MWST

$\textbf{Kalkulatorische Abschreibung (geschaetzt, unterjaerig):}$
$\text{Abschreibung / Fahrzeuge (oder anderes Anlagekonto) \quad Betrag}$
$\text{Keine MWST bei Abschreibungen!}$

$\textbf{Definitive Abschreibung (effektiv, Jahresabschluss):}$
$\text{Abschreibung / Fahrzeuge \quad Betrag}$
$\text{Differenz kalkulatorisch vs. definitiv korrigieren}$

$\textbf{Wichtig: Abschreibungen sind MWST-frei.}$
$\text{Abschreibung ist kein Kauf/Verkauf → keine VST, keine UST.}$
$\text{VST faellt nur beim KAUF der Anlage an (→ T-FAHR).}$

$\textbf{Lineare Abschreibung:}$
$\text{Jaehrlicher Betrag} = \frac{\text{Anschaffungswert} - \text{Restwert}}{\text{Nutzungsdauer in Jahren}}$

$\textbf{Degressive Abschreibung (Buchwert-Methode):}$
$\text{Jaehrlicher Betrag} = \text{Buchwert} \times \text{Abschreibungssatz in \%}$

---

## T-KONTOP — T-KONTEN-DARSTELLUNG

$\textbf{T-Konto Grundstruktur:}$
$\text{Linke Seite = SOLL (Zunahme bei Aktiv/Aufwand)}$
$\text{Rechte Seite = HABEN (Zunahme bei Passiv/Ertrag)}$

$\textbf{T-Konto VST 1170 (Aktivkonto):}$
$\text{SOLL: Vorsteuer aus Einkauf Material}$
$\text{HABEN: Saldierung an UST 2200 (bei Abrechnung)}$

$\textbf{T-Konto VST 1171 (Aktivkonto):}$
$\text{SOLL: Vorsteuer aus Investitionen/uebr. Aufwand}$
$\text{HABEN: Saldierung an UST 2200 (bei Abrechnung)}$

$\textbf{T-Konto UST 2200 (Passivkonto):}$
$\text{SOLL: Saldierung VST 1170, VST 1171, Zahlung an ESTV}$
$\text{HABEN: Umsatzsteuer aus Verkauf}$

$\textbf{Beispiel T-Konto UST 2200:}$
$\text{SOLL: VST 1170 \quad CHF 2025}$
$\text{SOLL: VST 1171 \quad CHF 810}$
$\text{SOLL: Bank 1020 \quad CHF 5265 (Zahllast)}$
$\text{HABEN: Aus Verkaeufen \quad CHF 8100}$
$\text{Saldo: 0 (ausgeglichen)}$

$\textbf{T-Konto Verb aus LL 2000 (Passivkonto):}$
$\text{SOLL: Zahlungen (Bank), Rabatte, Skonti}$
$\text{HABEN: Einkaufsrechnungen (Netto + MWST)}$

$\textbf{T-Konto Ford aus LL 1100 (Aktivkonto):}$
$\text{SOLL: Verkaufsrechnungen (Netto + MWST)}$
$\text{HABEN: Zahlungseingaenge, Skonti, Gutschriften}$

---

## X-TRAP — FALLEN UND HAEUFIGE FEHLER

| # | Falle | Fix |
|---|---|---|
| 1 | VST 1170 statt 1171 (oder umgekehrt) | Kontenklasse 4 = 1170, alles andere = 1171 |
| 2 | MWST auf Brutto statt Netto berechnet | Netto × 0.081 ODER Brutto × 8.1/108.1 |
| 3 | Bruttomethode: MWST nicht herausgeloest | Am Periodenende IMMER VST/UST separieren |
| 4 | SSS: Vorsteuer verbucht | Bei Saldosteuersatz gibt es KEINE Vorsteuer |
| 5 | Abrechnung: Reihenfolge falsch | Erst 1170 an 2200, dann 1171 an 2200, dann Rest an Bank |
| 6 | Rabatt/Skonto: MWST vergessen | Rabatt reduziert auch die MWST proportional |
| 7 | Offenposten: Rueckbuchung vergessen | Neue Periode IMMER mit Rueckbuchung starten |
| 8 | Offenposten: Rechnung und Zahlung gebucht | Bei OP-Methode NUR Zahlungen laufend buchen |
| 9 | Rundung vergessen | MWST-Betraege auf 5 Rappen runden |
| 10 | Soll ≠ Haben | Jeder Buchungssatz: Soll-Summe = Haben-Summe |
| 11 | Netto/Brutto verwechselt | "exkl." = Netto, "inkl." = Brutto |
| 12 | Investition als Aufwand gebucht | Fahrzeug = Konto 1530, nicht 6200 |
| 13 | Steuersaetze gemischt (alt/neu) | Aufgabe genau lesen: 8.1% (neu) oder 7.7% (alt) |
| 14 | SSS auf Netto statt Brutto | Saldosteuersatz wird auf BRUTTO-Umsatz angewendet |
| 15 | Bei Verkauf: UST auf Soll gebucht | UST gehoert auf HABEN-Seite (Schuld = Passiv) |
