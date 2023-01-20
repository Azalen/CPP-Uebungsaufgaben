# Aufgabe 06: Texteditor

Schreiben Sie einen simplen Texteditor als objektorientiertes Programm!

**Anforderungen:**

1. Ein Menü, welches die Auswahl verschiedener Funktionen (einlesen, ausgeben, bearbeiten ..) ermöglicht
2. Einen Bereich über dem Auswahlmenü, welcher den aktuellen Text anzeigt
3. Einen Bereich unter dem Auswahlmenü zur Eingabe für den Nutzen
4. Bei Auswahl einer Menüfunktionalität aktualisiert sich der Bereich, welcher den aktuellen Text enthält

**Menüfunktionalität**

1. Text einlesen aus einer Textdatei
2. Text speichern in eine Textdatei
3. Extraktion aller Großbuchstaben aus dem Text
4. Berechnung der Wortanzahl

**Anregungen / Tipps**

- Arbeiten Sie mit Methoden! Schon das Menü an sich sollte eine Objekt-Methode sein!
- Achten sie auf `const`-Correctness!
- Jedes OS hat eigene Möglichkeiten das Kommandofenster zu resetten. Linux bspw. `system("clear")`
- Um die Eingabe robust zu gestalten sollte der Eingabebuffer nach dem `cin` stets geleert werden
```c++
/// Eingabebuffer leeren
string temp;
getline(cin, temp);
```
- Um innerhalb einer Methode weitere Methoden desselben Objekts aufrufen können benötigen Sie den `this->`-Zeiger
- Wenn sie vollständig objektorientiert arbeiten sollte die main-Funktion nicht mehr als drei Zeilen Code enthalten
