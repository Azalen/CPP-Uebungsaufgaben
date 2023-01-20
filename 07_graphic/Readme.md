# Aufgabe 07: Bild (Klassen)

![Untitled-2](https://user-images.githubusercontent.com/20336567/153412928-c1cce69c-01ff-4bfb-9801-5d72df891f6f.png)

Schreiben Sie ein simples, objektorientiertes Bildbearbeitungsprogramm! Schreiben Sie dazu die Klassen `Farbe` und `Bild`!

## Farbe

Schreiben Sie eine Klasse `Farbe`, die für die Objekte dieser Klasse die jeweiligen Rot-, Grün- und Blauanteile (RGB-Wert) speichern kann. Alle drei Werte sind ganze Zahlen zwischen 0 und 255, wobei bei den RGB-Werten der Wert 0 keinen Farbanteil und 255 vollen Farbanteil bedeutet. Der Standardwert für die Transparenz soll 255 (voll deckende Farbe) sein und 0 als Transparenzwert soll eine völlig durchsichtige Farbe bedeuten.

**Beispiele** 
```
schwarz     0   0   0
weiß      255 255 255
rot       255   0   0
grün        0 255   0
blau        0   0 255
gelb      255 255   0
```

**Anforderungen:**

1. Entwerfen Sie einen Konstruktor und `get`- und `set`-Methoden.
2. An allen Stellen, an denen im Sourcecode die Datenelemente für die Farbanteile und die Transparenz gesetzt werden, soll verhindert werden, dass Werte kleiner als 0 oder größer als 255 eingetragen werden können.

## Bild

Schreiben Sie eine Klasse `Bild`, welche die Klasse `Farbe` benutzt. Ein `Bild` ist eine 2D-Matrix aus Instanzen der Klasse `Farbe`. Die Dimensionen dieser Matrix sind die Höhe und Breite des Bildes. 

**Anforderungen:**

1. Entwerfen Sie einen Konstruktor, welcher ein einfarbiges Bild mit vorgegebener Höhe und Breite realisiert.
2. Schreiben Sie eine Methode um das `Bild` im `.ppm`-Format auszugeben, sodass man es im Betriebssystem zur Kontrolle anzeigen kann.

    Bonus: Realisieren Sie eine Methode//Algorithmus, welcher ein Bild mit 4 gleich großen Farbstreifen (suchen Sie die Farben selber aus) realisiert.


### Anregungen / Tipps

- Achten sie auf `const`-Correctness!
- Um eine 2D-Matrix zu realisieren stehen Ihnen sowohl statische wie dynamische Arrays, die Vector-Klasse oder direkt STL-Konstrukte für Matrix/Array zur Verfügung.
- Ein Bild im `.ppm`-Format ist eine Text-Datei (nutzen Sie also den nicht-binären `ofstream`) mit einem speziell vorgegebenen Header und darauffolgend die RGB-Farbwerte. **Beispiel:** 

```
# Ein Farbbild der Größe 3 × 2 Pixel im PPM P3-Format mit maximalem Farbwert 255.
# Darauf folgen die RGB-Tripel.

P3
3 2
255
255   0   0     0 255   0     0   0 255
255 255   0   255 255 255     0   0   0
```

Ist gezoomt:

![](https://upload.wikimedia.org/wikipedia/commons/5/57/Tiny6pixel.png)
