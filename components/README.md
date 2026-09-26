# Komponentenliste

Diese Datei ist die zentrale Stück- und Dokumentationsliste für das Kamera-/Haspel-Projekt.

> Status: laufend ergänzen. Unbekannte oder noch nicht bestätigte Angaben sind ausdrücklich mit `offen` markiert.

| ID | Komponente | Hersteller / Typ | Menge | Funktion im Projekt | Wichtige Eigenschaften | Gekauft bei | Artikel / Link | Datenblatt | Status |
|---|---|---|---:|---|---|---|---|---|---|
| C001 | Mikrocontroller-Board | ESP32-C3 Super Mini | 1 | Auswertung der Hallsensoren, Richtungs- und Wegberechnung, Kommunikation | ESP32-C3, WLAN/Bluetooth, 3,3-V-Logik, kompakte Bauform | offen | offen | siehe Detailseite | vorhanden / zu bestätigen |
| C002 | DC/DC Step-Down-Modul | MP1584EN Mini Buck Converter | 1 | Versorgung der Elektronik aus höherer Batteriespannung | Step-Down-Wandler, einstellbare Ausgangsspannung, Modul typ. bis ca. 3 A beworben; reale Dauerlast abhängig von Kühlung | GTIWUNG / genaue Kaufquelle offen | „MP1584EN Mini Convertitore Buck Step-down“ | siehe Detailseite | vorhanden / zu bestätigen |
| C003 | Video-Encoder | iVCAN Video Encoder Board | 1 | Analogvideo digitalisieren und per Netzwerk/RTSP bereitstellen | TCP/JSON-Steuerung, OSD, Port 8866, RTSP; exaktes Modell offen | offen | offen | vorhandene API-Dokumentation im Projekt | vorhanden |
| C004 | Hallsensor A | Typ noch festzulegen | 1 | Impulserfassung und Richtungserkennung | Digitaler Hallsensor bevorzugt; 3,3-V-kompatible Auswertung prüfen | offen | offen | offen | Auswahl offen |
| C005 | Hallsensor B | Typ noch festzulegen | 1 | Zweite Phase für Richtungserkennung | Wie C004; mechanisch versetzt montiert | offen | offen | offen | Auswahl offen |
| C006 | Permanentmagnete | Typ/Abmessungen offen | 5 | Impulsgeber an der Haspel | Gleichmäßige Montage; ausreichende Feldstärke bei geplantem Luftspalt | offen | offen | nicht erforderlich | Auswahl offen |
| C007 | Li-Ion-Akku | 3S, 12,6 V voll, 3000 mAh | 1 | Mobile Stromversorgung | 3 Zellen in Serie, Nennenergie ca. 37,8 Wh bei 12,6 V × 3 Ah als Maximalspannungsbezug; tatsächliche Nennenergie je Zellchemie prüfen | offen | offen | offen | vorhanden / zu bestätigen |
| C008 | Analog-Kameramodul | Typ offen | 1 | Bildaufnahme im Kamin/Rohr | Analoges Videosignal; mechanische Bauform und Versorgung noch dokumentieren | offen | offen | offen | vorhanden / zu bestätigen |

## Pflichtangaben pro Komponente

Für jede wichtige Komponente soll eine eigene Detailseite unter `components/details/` angelegt werden. Dort erfassen wir möglichst:

- genaue Bezeichnung
- Hersteller
- Hersteller-Artikelnummer
- Händler / Shop
- Kaufdatum
- Bestellnummer
- Kaufpreis
- Produktlink
- Datenblatt-Link
- Versorgungsspannung
- Stromaufnahme
- Ein-/Ausgangspegel
- Pinbelegung
- Abmessungen
- Temperaturbereich
- Schnittstellen / Protokolle
- Einbauort im Projekt
- Anschluss an andere Baugruppen
- Besonderheiten / bekannte Probleme
- Ersatzteil oder mögliche Alternative

## Statusbegriffe

- **vorhanden** – Bauteil liegt physisch vor
- **bestellt** – bestellt, aber noch nicht eingetroffen
- **Auswahl offen** – Bauteiltyp noch nicht festgelegt
- **zu bestätigen** – Information stammt aus bisherigen Projektangaben und soll noch anhand des realen Bauteils geprüft werden
