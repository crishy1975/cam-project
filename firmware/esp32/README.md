# ESP32-Firmware

Hier entsteht die Firmware für den ESP32-C3 Super Mini.

## Geplante Aufgaben

- Hallsensor A einlesen
- Hallsensor B einlesen
- Drehrichtung erkennen
- Impulse zählen
- Tiefe in Metern berechnen
- Nullpunkt setzen
- Kalibrierfaktor speichern
- Verbindung zum iVCAN-Encoder herstellen
- OSD-Meterwert per TCP/JSON aktualisieren

## Entwicklungsreihenfolge

1. Beide Sensoren im seriellen Monitor anzeigen.
2. Richtungslogik testen.
3. Impulszähler implementieren.
4. Kalibrierung ergänzen.
5. Meterwert berechnen.
6. TCP-Verbindung ergänzen.
7. OSD-Kommandos anbinden.

Der eigentliche Programmcode wird kommentiert abgelegt, damit die einzelnen Schritte später leicht nachvollziehbar und änderbar bleiben.
