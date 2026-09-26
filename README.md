# CAM Project

Kamera- und Haspelprojekt zur Inspektion von Kaminen und Abgaswegen.

## Ziel

Das System soll ein analoges Kamerasignal drahtlos auf ein Smartphone übertragen und gleichzeitig die eingefahrene Kameratiefe messen und als OSD-Text in das Videobild einblenden.

## Systemübersicht

- Analogkamera an GFK-Schubstange
- iVCAN Video-Encoder für Videostream
- WLAN-Verbindung zum Smartphone
- Anzeige des Videostreams z. B. mit VLC
- ESP32-C3 Super Mini für Sensorik und Steuerung
- Zwei Hallsensoren zur Richtungserkennung der Haspel
- Mehrere Magnete an der Haspel zur robusten Impulserfassung
- Berechnung der ausgefahrenen Länge / Tiefe
- Übergabe der Meteranzeige an das OSD des Video-Encoders

## Aktuell geplante Hardware

- ESP32-C3 Super Mini
- iVCAN Video-Encoder
- 2 × Hallsensor
- 5 × Magnet an der Haspel
- DC/DC-Abwärtswandler, z. B. MP1584EN
- 3S Li-Ion-Akku, 12,6 V voll geladen

## Kommunikation mit dem Encoder

Der iVCAN-Encoder unterstützt eine TCP/JSON-Schnittstelle.

- TCP-Port: `8866`
- OSD-Funktion: `setVideoOsdTextInfo`
- Auslesen: `getVideoOsdTextInfo`
- Videowiedergabe: RTSP / VLC

Siehe [docs/osd-protocol.md](docs/osd-protocol.md).

## Tiefenmessung

Die Haspel erhält mehrere Magnete. Zwei versetzte Hallsensoren erfassen die Impulse und ermöglichen neben der Wegmessung auch die Erkennung der Drehrichtung.

Siehe [docs/distance-measurement.md](docs/distance-measurement.md).

## Projektstruktur

```text
cam-project/
├── README.md
├── firmware/
│   └── esp32/
├── hardware/
│   ├── kicad/
│   ├── wiring/
│   └── components/
├── docs/
│   ├── video-encoder.md
│   ├── osd-protocol.md
│   └── distance-measurement.md
└── mechanical/
    └── sensor-holder/
```

## Nächste Schritte

1. Hallsensor-Typ festlegen.
2. Mechanische Position von Magneten und Sensoren bestimmen.
3. Umfang bzw. wirksamen Messdurchmesser der Haspel messen.
4. ESP32-Testprogramm zur Richtungs- und Impulserkennung erstellen.
5. Kalibrierung in mm pro Impuls durchführen.
6. OSD-Meteranzeige automatisch über TCP/JSON aktualisieren.
7. KiCad-Schaltplan erstellen.

## Sicherheit / Zugangsdaten

Keine WLAN-Passwörter, Tokens, privaten IP-Zugangsdaten oder sonstige Geheimnisse direkt im Repository speichern. Solche Werte gehören später in eine lokale Konfigurationsdatei, die über `.gitignore` ausgeschlossen wird.
