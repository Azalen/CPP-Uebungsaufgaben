# Aufgabe 09: Dünnbesetzte Matritzen (2D-Arrays, 1D-Arrays, Speichereffizienz)

Für viele IT-Anwendungen benötigt man große Matritzen. Sie haben etwa gelernt, dass jedes Bild im Computer letztendlich nichts als eine 2D-Pixelmatrix ist. Um diese effizient abzuspeichern - und so Speicherplatz zu sparen - existieren viele verschiedene Ansätze und Algorithmen (bspw. JPEG, PNG). In vielen Komprimierungsverfahren macht man sich zu nutze, dass in großen Teilen der Bild-Pixel-Matrix nur die Null als Wert steht.
Solche, sogenannten dünnbesetzten Matritzen, kann man effizient speichern, indem man alle Werte von `matrix` ungleich Null in einem 1D-Array ablegt und sich die Positionen dieses Werts in der originalen Matrix als Koordinaten `(i,j)` extra merkt. Das heißt man baut einen Vektor/1D-Array `elements`, indem die Matrixwerte gespeichert sind und zwei weitere Arrays `i` und `j`, in denen die entsprechenden Koordinaten in der Matrix liegen.

Dann gilt: `matrix[i[k]][j[k]] = elements[k]   |  k = Länge der Arrays elements, i, j`

**Beispiel**

![](https://i.imgur.com/KWQIAMG.png)

Schreiben Sie ein Programm, was die beschriebene Komprimierung realisiert und mindestens folgende Anforderungen erfüllt: 
- die Bestimmung der Anzahl der Nichtnullen einer vollbesetzten Matrix
- die Umwandlung einer vollbesetzten 2D-Matrix in eine dünnbesetzte Matrix (d.h. `elements`, `i`, `j`)
- eine Ausgabefunktion, die die dünnbesetzte Matrix als vollbesetzte Matrix ausgibt
