# Video-Encoder

## Aufgabe

Der iVCAN-Encoder übernimmt die Digitalisierung des analogen Kamerasignals und stellt den Videostream über Netzwerk/WLAN bereit.

## Aktueller Stand

- Analoges Videosignal wird am PC korrekt dargestellt.
- Wiedergabe am Smartphone mit VLC ist grundsätzlich möglich.
- Die Latenz lag in bisherigen Tests bei ungefähr einigen Sekunden.
- Steuerung und OSD erfolgen über TCP/JSON.

## Zielzustand

Die Kameraeinheit soll möglichst autark arbeiten:

1. Kamera liefert das analoge Videosignal.
2. Encoder erzeugt den Netzwerkstream.
3. Smartphone verbindet sich per WLAN.
4. VLC oder eine spätere eigene App zeigt den Stream.
5. Der ESP32 misst die Haspelbewegung.
6. Die aktuelle Tiefe wird als OSD in das Videobild eingeblendet.

## Offene Punkte

- endgültige Netzwerkarchitektur festlegen
- WLAN-AP-Verhalten testen
- RTSP-URL sauber dokumentieren
- Startzeit nach Einschalten messen
- Stromverbrauch im Dauerbetrieb messen
- Verhalten bei Verbindungsabbruch testen
- Latenz weiter optimieren
