# Aufgabe 10: Strukturen

Entwerfen Sie eine Struktur `Tabelleneintrag`, um eine Zeile der Vorrundentabelle der Gruppe E der Fußball-Weltmeisterschaft 2022 darzustellen:

![](https://i.imgur.com/AlJVrXP.png)

Wählen Sie dazu geeignet viele Komponenten für diese Struktur mit passenden Datentypen und gehen Sie möglichst speichereffizient vor (müssen Sie alle Spalten abspeichern?).

Legen Sie im Hauptprogramm einzelne Strukturvariablen jeweils für die vier Länder dieser Vorrundentabelle an und initialisieren Sie die zu Deutschland gehörende Strukturvariable sofort bei der Definition gemäß der obigen Abbildung.

Entwerfen Sie nun eine neue Version des Strukturdatentyps namens `NeuerTabelleneintrag`, der das Torverhältnis diesmal als Array `tore` der Länge 2 mit Werten eines geeigneten Standarddatentyps verwendet. Testen Sie auch diese Implementierung im Hauptprogramm.

Schreiben Sie für die Struktur `NeuerTabelleneintrag` eine Ein- und Ausgabefunktion, mit dem Sie die Übergabe von Strukturvariablen an Funktionen üben, indem Sie folgende Funktionsprototypen realisieren:

```c++
/* ANSI-C++-Prototypen */
void eingabe(NeuerTabelleneintrag & zeile);
void ausgabe(NeuerTabelleneintrag zeile);
```

Wird eine Übergabe oder Rückgabe für Strukturvariablen immer per _call by value_ oder per _call by reference_ gemacht? Begründen Sie Ihre Antwort, indem Sie im Programmcode Ihre Antwort nachweisen! Dürfte man bei der Eingabe auch eine konstante Referenz verwenden? Würde es Sinn machen bei der Ausgabe eine konstante Struktur zu übergeben? Begründe!
