# Fenster Reminder
Wenn ein Fenster 10 Minuten offen steht, wird eine Push-Nachricht gesendet. HomematicIP hat keine "Timer-Funktion", deshalb wird die Einschaltdauer eines Schaltausgangs als Timer verwendet. 

## Geräte
 - 1x "Fenster- und Türkontakt" pro Raum
 - 1 Kanal der "Modulplatine Open Collector - 8-fach" pro Raum

## Automatisierung

### Fenster auf
#### Auslöser
 - Fensterzustand=Geöffnet
#### Aktion
 - Schalten OUT(1) An: 10 Minuten

### Fenster Check
#### Auslöser
 - Schalten OUT(1) Aus
#### Zusatzbedingung
 - Fensterzustand=Geöffnet
#### Aktion
 - Push-Mitteilung
 - Schalten OUT(1) An: 10 Minuten

### Fenster zu
#### Auslöser
 - Fensterzustand=Geschlossen
#### Aktion
 - Schalten OUT(1) Aus
