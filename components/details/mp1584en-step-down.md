# MP1584EN Step-Down Modul

## Kurzbeschreibung

Kompaktes DC/DC-Abwärtswandlermodul auf Basis des **MP1584EN**. Es wird im Kamera-Projekt verwendet, um aus einer höheren Batteriespannung eine niedrigere, stabile Versorgungsspannung für Elektronikkomponenten bereitzustellen.

## Identifikation

- **Bauteil / IC:** MP1584EN
- **Hersteller des ICs:** Monolithic Power Systems (MPS)
- **Modultyp:** einstellbarer Buck-/Step-Down-Wandler
- **Marke des gekauften Moduls:** GTIWUNG
- **Gekaufte Produktbezeichnung:** GTIWUNG 10 Pezzi MP1584EN Mini Convertitore Buck Step-down, Ultra Piccolo 3A Regolabile Alimentatore Step-Down Module, Convertitore buck DC-DC da 4,5-28V a 0,8-20V
- **Geplante Funktion im Projekt:** Spannungsreduzierung aus der Akkuversorgung

## Technische Eigenschaften

### Herstellerangaben zum MP1584

- Eingangsspannungsbereich des ICs: **4,5 V bis 28 V DC**
- Ausgangsstrom: **bis 3 A**
- Schaltfrequenz: programmierbar, bis **1,5 MHz**
- integrierter High-Side-MOSFET
- Stromregelung im Current-Mode-Verfahren
- interner Soft-Start
- interner Strombegrenzer
- thermische Abschaltung
- Pulse-Skipping bei kleiner Last zur Wirkungsgradverbesserung
- Gehäuse des ICs: **SOIC8E**

### Angaben des gekauften GTIWUNG-Mini-Moduls

Laut Produktbezeichnung des gekauften Artikels:

- Eingang: **4,5–28 V DC**
- Ausgang: **0,8–20 V DC, einstellbar**
- beworbener Ausgangsstrom: **bis 3 A**
- Bauform: **Mini / Ultra Piccolo**
- Ausgangsspannung über Trimmer/Potentiometer einstellbar
- Lieferumfang: **10 Stück**

> Hinweis: Die reale dauerhaft nutzbare Stromstärke eines sehr kleinen MP1584EN-Moduls hängt stark von Eingangsspannung, Ausgangsspannung, Kühlung, Leiterplattenlayout und Umgebungstemperatur ab. Die 3-Angabe ist daher nicht automatisch als dauerhaft zulässiger Praxisstrom zu verstehen.

## Anschluss des Moduls

Typischerweise besitzt das Modul vier Anschlüsse:

| Anschluss | Bedeutung |
|---|---|
| IN+ | positive Eingangsspannung |
| IN- | Masse / Eingang Minus |
| OUT+ | positive Ausgangsspannung |
| OUT- | Masse / Ausgang Minus |

Vor Anschluss der Kamera- oder ESP32-Elektronik muss die Ausgangsspannung mit einem Multimeter eingestellt und kontrolliert werden.

## Verwendung im Kamera-Projekt

Geplante Versorgung:

```text
3S Li-Ion Akku
12,6 V voll geladen
        │
        ▼
MP1584EN Step-Down
        │
        ├── niedrigere Versorgung für Elektronik
        └── genaue Ausgangsspannung je Verbraucher festlegen
```

## Einkauf

- **Händler / Shop:** Amazon.it
- **Marke:** GTIWUNG
- **Produkt:** GTIWUNG 10 Pezzi MP1584EN Mini Convertitore Buck Step-down, Ultra Piccolo 3A Regolabile Alimentatore Step-Down Module, Convertitore buck DC-DC da 4,5-28V a 0,8-20V
- **Stückzahl:** 10 Module
- **Produktlink:** noch einzutragen
- **Bestellnummer / ASIN:** noch einzutragen
- **Kaufpreis:** noch einzutragen
- **Kaufdatum:** noch einzutragen

## Datenblatt

Offizielles Hersteller-Datenblatt:

- Monolithic Power Systems – **MP1584, 3A, 1.5MHz, 28V Step-Down Converter**
- Herstellerseite: https://www.monolithicpower.com/en/products/power-management/switching-converters-controllers/step-down-buck/converters/mp1584.html
- Datenblatt: https://www.monolithicpower.com/en/documentview/productdocument/index/version/2/document_type/Datasheet/lang/en/sku/MP1584EN-LF-Z/

## Herstellerstatus

MPS kennzeichnet den MP1584 aktuell als **NRFND – Not Recommended For New Designs**. Für bestehende Anwendungen wird der Baustein weiterhin unterstützt; für neue Designs nennt MPS alternative Bausteine.

Für dieses Projekt ist das vorhandene MP1584EN-Modul trotzdem sinnvoll verwendbar, sofern Spannungsbereich, Strom und Erwärmung passen.

## Noch zu prüfen

- [ ] exakter Amazon-Produktlink / ASIN
- [ ] Kaufpreis und Kaufdatum
- [ ] exakte Abmessungen unseres Moduls
- [ ] tatsächliche Ausgangsspannung im Kamera-Projekt
- [ ] Dauerstrom des angeschlossenen Verbrauchers
- [ ] Erwärmung bei realer Last
- [ ] Wirkungsgrad im realen Betrieb
- [ ] Foto der Vorder- und Rückseite
- [ ] KiCad-Footprint für das komplette Modul

## Quellen

Technische IC-Daten basieren auf der Herstellerdokumentation von Monolithic Power Systems. Die Händlerangaben zum gekauften Modul stammen aus der Produktbezeichnung des bei Amazon.it gekauften GTIWUNG-10er-Sets.
