## Geräte
 - 1x "Fenster- und Türkontakt" pro Raum
 - 2 Kanäle der "Modulplatine Open Collector - 8-fach" pro Raum

## Automatisierung

### Fenster auf
#### Auslöser
 - Fensterzustand=Geöffnet
#### Aktion
 - Schalten OUT(1) An
 - Schalten OUT(5) An: 10 Minuten

### Fenster Check
#### Auslöser
 - Schalten OUT(5) Aus
#### Zusatzbedingung
 - Fensterzustand=Geöffnet
#### Aktion
 - Push-Mitteilung
 - Schalten OUT(5) An: 10 Minuten

### Fenster zu
#### Auslöser
 - Fensterzustand=Geschlossen
#### Aktion
 - Schalten OUT(1) Aus
 - Schalten OUT(5) Aus
