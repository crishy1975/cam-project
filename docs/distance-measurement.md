# Tiefenmessung der Haspel

## Prinzip

Die Drehbewegung der Haspel wird kontaktlos mit Magneten und zwei Hallsensoren erfasst.

Geplant sind:

- 5 Magnete gleichmäßig über den Umfang verteilt
- 2 Hallsensoren mit mechanischem Versatz
- Auswertung durch einen ESP32-C3 Super Mini

## Warum zwei Sensoren?

Mit nur einem Sensor lässt sich zuverlässig zählen, aber nicht eindeutig erkennen, ob die Haspel vorwärts oder rückwärts bewegt wird.

Zwei versetzte Sensoren liefern eine Phasenfolge. Je nachdem, welcher Sensor zuerst schaltet, kann die Drehrichtung bestimmt werden.

Beispiel:

- Sensor A vor Sensor B → Ausfahren
- Sensor B vor Sensor A → Einfahren

Die tatsächliche Zuordnung wird beim Aufbau geprüft und kann in der Firmware umgedreht werden.

## Wegberechnung

Bei fünf Magneten entstehen theoretisch fünf Messereignisse pro vollständiger Umdrehung.

```text
Weg_pro_Impuls = Umfang_der_Messbahn / Anzahl_Magnete
```

Praktisch wird ein Kalibrierfaktor verwendet:

```text
Tiefe_mm = Impulszaehler × mm_pro_Impuls
```

Der Kalibrierfaktor wird nicht nur geometrisch berechnet, sondern anschließend mit einer bekannten realen Strecke eingemessen.

## Mechanische Punkte

- Magnetabstände möglichst gleichmäßig
- Sensorhalter verwindungssteif
- kleiner, definierter Luftspalt zwischen Magnet und Sensor
- Sensoren gegen Stöße schützen
- Kabel zugentlasten
- Magnete mechanisch sichern

## Zu beachten

Bei einer aufgewickelten Schubstange ändert sich der wirksame Radius der Wicklung. Falls die Messung direkt aus der Haspeldrehung erfolgt, kann dadurch ein systematischer Fehler entstehen.

Für die gewünschte robuste Lösung kann dieser Fehler zunächst akzeptiert und durch Kalibrierung minimiert werden. Falls später höhere Genauigkeit nötig ist, kann eine separate Messrolle vorgesehen werden, die direkt auf der GFK-Stange läuft.
