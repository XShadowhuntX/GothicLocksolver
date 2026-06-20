# Lock Puzzle Solver

Ein kleiner webbasierter Solver zum lösen von Gothic Schlössern.

Das Projekt hilft dabei, eine Lösung für ein Puzzle zu berechnen, bei dem mehrere Blöcke durch Bewegungen nach links oder rechts geschoben werden bis alle Pins aller Blöcke in der Mitte positioniert sind.

Die Eingaben werden reihenweise abgefragt, damit die Wirkung jedes Blocks übersichtlich eingetragen werden kann.


## Nutzung

1. Repository herunterladen oder klonen.
2. Alle Dateien in einem Ordner speichern.
3. index.html im Browser öffnen.
4. Anzahl der Blöcke eintragen.
5. Auf **Maske erstellen** klicken.
6. Aktuelle Positionen der Blöcke eintragen.
7. Reihenweise die Wirkung der Bewegungen auswählen.
8. Mit **Weiter** zur nächsten Reihe wechseln.
9. Mit **Zurück** kann man vorherige Reihen erneut bearbeiten.
10. Am Ende auf **Lösung Berechnen** klicken.


## Funktionen

* Anzahl der Blöcke einstellbar
* Eingabe der aktuellen Position jedes Blocks
* Reihenweise Eingabe der Bewegungswirkung
* Vor- und Zurück-Button zum Wechseln zwischen den Reihen
* Automatische Berechnung der Lösung
* Ausgabe als genaue Schritt-für-Schritt-Lösung
* Ausgabe als Kurzform mit zusammengefassten gleichen Bewegungen
* Mittelalterliches Design mit Hintergrund, Logo und Seitenbildern


## Projektstruktur

lock-puzzle-solver/
├── index.html
├── style.css
├── gothic.png
├── lockpick.png
├── chest.png
└── README.md


## Dateien

### index.html

Enthält die HTML-Struktur und die JavaScript-Logik für:

* Eingabemaske
* Reihenweise Abfrage
* Navigation zwischen den Eingaben
* Berechnung der Lösung
* Ausgabe des Ergebnisses

### style.css

Enthält das komplette Design für:

* Hintergrund
* Boxen
* Buttons
* Tabellen
* Eingabefelder
* Bilder
* responsive Verhalten

### Bilder

Die folgenden Bilder müssen im selben Ordner wie `index.html` liegen:

gothic.png
lockpick.png
chest.png


## Berechnung

Der Solver verwendet eine Breitensuche, um eine möglichst kurze Lösung zu finden.

Dabei werden mögliche Bewegungen getestet, bis alle Blöcke auf der Zielposition stehen.

Die Standardwerte sind:

js
const HOLE_COUNT = 7;
const TARGET_POSITION = 4;

Das bedeutet:

* Es gibt 7 Löcher pro Block.
* Die Zielposition ist die Mitte.
* Bei 7 Löchern ist die Mitte Position 4.


## Ausgabe

Nach der Berechnung zeigt der Solver zwei Varianten an.

### Genaue Lösung

Eine nummerierte Schritt-für-Schritt-Anleitung:

B3 nach links
B3 nach links
B1 nach links

### Kurzform

Gleiche Bewegungen hintereinander werden zusammengefasst:

B3 nach links x5
B6 nach rechts
B1 nach links


## Technik

Dieses Projekt verwendet:

* HTML
* CSS
* JavaScript


## GitHub Pages

Das Projekt wird direkt über GitHub Pages gehostet.
