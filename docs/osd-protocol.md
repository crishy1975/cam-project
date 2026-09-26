# OSD-Kommunikation mit dem iVCAN-Encoder

## Schnittstelle

Der Video-Encoder wird über TCP mit JSON-Kommandos angesprochen.

Bekannter Port:

```text
8866
```

## Relevante Funktionen

Für die Meteranzeige sind insbesondere diese Befehle vorgesehen:

```text
setVideoOsdTextInfo
getVideoOsdTextInfo
```

Die genaue JSON-Struktur wird anhand des vorhandenen API-Guides und getesteter Befehle dokumentiert.

## Geplantes Verhalten

Der ESP32 berechnet aus den Hallsensorimpulsen die aktuelle Kameratiefe.

Beispielanzeige:

```text
12.4 m
```

Diese Anzeige soll regelmäßig an einen freien OSD-Textindex des Encoders gesendet werden.

## Anforderungen an die Firmware

- TCP-Verbindung zum Encoder herstellen
- Verbindungsabbruch erkennen
- automatische Wiederverbindung
- OSD nur aktualisieren, wenn sich der angezeigte Wert ändert
- Update-Rate begrenzen, damit der Encoder nicht unnötig belastet wird
- Textindex, Position, Größe und Farbe konfigurierbar halten

## Bekannte OSD-Parameter

Aus bisherigen Tests sind mehrere Textindizes möglich, z. B.:

```text
TextIndex 0
TextIndex 1
TextIndex 2
```

Bekannte Größen:

```text
Small
Normal
Big
```

## Sicherheit

IP-Adresse, WLAN-Zugangsdaten oder andere lokale Zugangsdaten dürfen nicht fest im öffentlichen Repository gespeichert werden. Dafür wird später eine lokale Konfigurationsdatei verwendet.
