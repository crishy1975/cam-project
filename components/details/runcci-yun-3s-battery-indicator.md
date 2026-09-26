# RUNCCI-YUN 3S Batterieanzeige

## Kurzbeschreibung

LED-Batterieanzeige für 3S-Lithium-Akkupacks. Das Modul zeigt den ungefähren Ladezustand über mehrere LED-Segmente an und wird direkt an Plus und Minus des Akkupacks angeschlossen.

## Identifikation

- **Marke:** RUNCCI-YUN
- **Produkt:** 3S Modulo Indicatore di Capacità Della Batteria Al Litio
- **Geeignet für:** 3S Li-Ion / 18650
- **Nennspannung des Akkupacks:** 11,1 V
- **volle Ladespannung:** 12,6 V
- **Anzeige:** blaue LED-Segmente
- **Lieferumfang:** 4 Stück
- **Geplante Funktion im Projekt:** sichtbare Restladungsanzeige des 3S-Akkus

## Einkauf

- **Shop:** Amazon.it
- **Produktbezeichnung:** RUNCCI-YUN 3S Modulo Indicatore di Capacità Della Batteria Al Litio 11.1V 12V 12.6V Blu Tester di Capacità Della Batteria Display A LED per batterie agli ioni di Litio 3S 18650(4PCS)
- **Preis:** ca. 8,99 € zum Zeitpunkt der Recherche
- **ASIN:** noch einzutragen
- **Produktlink:** noch einzutragen

## Elektrischer Anschluss

Das Modul wird mit zwei Leitungen direkt parallel zum Akkupack angeschlossen:

| Anschluss | Verbindung |
|---|---|
| `+` | Akku Plus |
| `-` | Akku Minus |

Es ist keine separate Versorgung nötig.

## Technische Eigenschaften

Für baugleiche 3S-Anzeigemodule werden typischerweise folgende Werte angegeben:

- 3S-Lithium-Akku
- 11,1 V Nennspannung
- 12,6 V voll geladen
- 4-stufige LED-Anzeige
- Stromaufnahme typischerweise im Bereich weniger Milliampere bis einiger 10 mA
- Anzeige basiert auf der gemessenen Packspannung und ist daher eine grobe Ladezustandsanzeige, keine echte Coulomb-Counter-Messung

## Mechanische Daten

**Noch am realen RUNCCI-YUN-Modul prüfen.**

Im Handel existieren mindestens zwei ähnlich aussehende Bauformen:

- kleine nackte Leiterplatte etwa **29,5 × 15 mm**
- größere Anzeigeeinheit etwa **43,5–45 × 20 mm**

Deshalb werden die Abmessungen für unser konkretes RUNCCI-YUN-Modul nicht geraten.

## KiCad

Für genau die RUNCCI-YUN-Version wurde kein verlässliches fertiges KiCad-Footprint gefunden.

Ob überhaupt ein Footprint nötig ist, hängt von der Montage ab:

- bei Kabelanschluss / Frontplattenmontage: im Haupt-PCB meist **kein Footprint nötig**
- bei direkter Montage auf einer Trägerplatine: eigenes Footprint anhand der realen Maße erstellen

### Für ein eigenes Footprint benötigen wir

- Außenmaß Länge × Breite
- Position der `+`- und `-`-Lötpads
- Padgröße
- eventuell Befestigungsbohrungen
- Abstand Display zur Platinenkante

## Noch zu prüfen

- [ ] ASIN / direkter Amazon-Link
- [ ] exakte Abmessungen des gelieferten Moduls
- [ ] Position und Größe der beiden Anschluss-Pads
- [ ] eventuelle Befestigungsbohrungen
- [ ] tatsächliche Stromaufnahme
- [ ] LED-Schaltschwellen
- [ ] Foto Vorder- und Rückseite
- [ ] Entscheidung: Kabelmontage oder PCB-Footprint

## Referenzwerte ähnlicher Module

Ähnliche 3S-Module werden mit 4 LED-Segmenten und direktem 2-Draht-Anschluss angeboten. Je nach Bauform unterscheiden sich die mechanischen Maße deutlich; daher müssen die realen Maße vor Erstellung eines Footprints geprüft werden.
