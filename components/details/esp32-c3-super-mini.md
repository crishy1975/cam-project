# ESP32-C3 Super Mini – DUBEUYEW

## Einkauf

- **Produkt:** DUBEUYEW Scheda di Sviluppo ESP32-C3 Super Mini ESP32 C3 Mini
- **Packungsgröße:** 6 Stück
- **Shop:** Amazon.it
- **ASIN:** B0F65P46HZ
- **Produktlink:** https://www.amazon.it/dp/B0F65P46HZ
- **Kaufpreis:** offen
- **Kaufdatum:** offen

## Kurzbeschreibung

Kompaktes ESP32-C3-Entwicklungsboard für Steuerungs-, Sensor- und Kommunikationsaufgaben im Kamera-/Haspel-Projekt.

## Technische Eckdaten

Typische Eigenschaften des ESP32-C3 Super Mini:

- **Mikrocontroller:** ESP32-C3
- **CPU:** 32-Bit RISC-V, bis 160 MHz
- **WLAN:** 2,4 GHz, IEEE 802.11 b/g/n
- **Bluetooth:** Bluetooth LE 5
- **Flash:** typischerweise 4 MB bei gängigen Super-Mini-Modulen
- **Logikspannung:** 3,3 V
- **Versorgung:** 5 V über USB-C oder 5-V-Pin; 3,3-V-Regler auf dem Board
- **USB:** USB-C
- **GPIOs:** u. a. GPIO0–GPIO10 sowie GPIO20 und GPIO21, abhängig vom konkreten Boardlayout
- **Boardgröße:** typische Super-Mini-Bauform ca. 22 × 18 mm; mit überstehender USB-C-Buchse ca. 24 × 18 mm
- **Stiftleistenraster:** typischerweise 2,54 mm

> Hinweis: ESP32-C3-Super-Mini-Boards werden von mehreren Herstellern angeboten. Pinout, Bestückung und mechanische Details des konkret gekauften DUBEUYEW-Boards müssen am Original geprüft werden.

## Geplante Funktion im Kamera-Projekt

- Auswertung der Hallsensoren
- Richtungsbestimmung der Haspel
- Weg-/Tiefenberechnung
- Kommunikation mit weiteren Baugruppen
- mögliche Ausgabe bzw. Übergabe der berechneten Tiefe an die OSD-Steuerung

## Typisches Pinout

Gängige ESP32-C3-Super-Mini-Boards führen folgende Anschlüsse heraus:

- 3V3
- 5V
- GND
- GPIO0
- GPIO1
- GPIO2
- GPIO3
- GPIO4
- GPIO5
- GPIO6
- GPIO7
- GPIO8
- GPIO9
- GPIO10
- GPIO20
- GPIO21

Besondere Vorsicht bei Strapping-/Boot-Pins, insbesondere GPIO2, GPIO8 und GPIO9. Die endgültige Pinbelegung unseres Projekts wird erst nach Prüfung des konkreten Boards festgelegt.

## KiCad

Für den ESP32-C3 Super Mini existieren bereits KiCad-Dateien mit:

- Schaltplansymbol
- Through-Hole-Footprint
- 3D-Modell

Ein geeignetes Paket stammt ursprünglich aus SnapMagic/SnapEDA und wird unter **CC BY-SA 4.0 mit Design Exception 1.0** bereitgestellt.

Vor Verwendung muss das Footprint wie beim MP1584EN mechanisch mit dem Originalboard geprüft werden:

- Gesamtbreite
- Gesamtlänge
- Abstand der beiden Pinreihen
- 2,54-mm-Raster innerhalb der Pinreihe
- Position der USB-C-Buchse
- Antennenbereich freihalten

## Quellen

- Espressif ESP32-C3 Produktfamilie: https://www.espressif.com/en/products/socs/esp32-c3
- Amazon-Artikel: https://www.amazon.it/dp/B0F65P46HZ
- KiCad/SnapMagic-Dateien: https://www.snapeda.com/parts/ESP32-C3%20SuperMini_TH/Espressif%20Systems/view-part/

## Noch zu prüfen

- [ ] Kaufpreis
- [ ] Kaufdatum
- [ ] exakte Abmessungen des DUBEUYEW-Boards
- [ ] genaue Beschriftung der Pins am Original
- [ ] Boardrevision / Bestückungsvariante
- [ ] Footprint 1:1 ausdrucken und mit Original vergleichen
- [ ] endgültige GPIO-Zuordnung für Hallsensoren und OSD-Kommunikation
