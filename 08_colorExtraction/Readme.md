# Aufgabe 08: Farb-Extraktion

![Untitled-2](https://user-images.githubusercontent.com/20336567/153413692-cd388015-ffc2-4a82-b921-7ac4a5194a3f.png)

Schreiben Sie ein ein Programm, welches die Anzahl verschiedener Farben in einem `.ppm`-Bild errechnet und in der Konsole ausgeben kann. Außerdem soll es möglich sein die extrahierten Farben in 15x300 Pixel langen Streifen in einem neuen `.ppm`-Bild zur Kontrolle auszugeben.


### Anregungen / Tipps

- Prüfen Sie zunächst, ob das Einlesen erfolgreich war (d.h. ob sie die Datei öffnen konnten und ob es ein korrektes `PPM` im P3-Standard ist)!
- Nutzung der Klasse **Farbe** aus Aufgabe 07 ist hilfreich und gewünscht, wenn auch nicht zwingend notwendig.
- es ist hilfreich für die Klasse Farbe einen eigenen Vergleichs-Comparator (`operator==`) zu schreiben. Dies kann sowohl als Objektmethode innerhalb der Klasse oder als Hilfsfunktion außerhalb der Klasse realisiert werden.
- um eine RGB-Farbe als int darzustellen könnte man die Formel `rgb_int = R*2562 + G*256 + B` benutzen.

### Bonus

Nutzen Sie den STL-Container `<set>` oder `<unordered_set>` und erläutern Sie dessen Funktionsweise!
