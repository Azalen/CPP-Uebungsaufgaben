# Aufgabe 02: Deterministischer Zufall (rand, seed, modulo)

## Zufallsfunktion aus der C++ Standard Template Library

Schreiben Sie einen Programmteil, der das Münzwurfexperiment (Kopf oder Zahl) mit einer eingegebenen Anzahl von Versuchen simuliert. Verwenden Sie dabei die in C++ vorhandene Zufallszahlenfunktion  `rand()`, die sie so modifizieren müssen, dass das Ergebnis entweder Kopf oder Zahl bedeuten soll. Initialisieren Sie den Zufallszahlengenerator mit dem Startwert (engl. seed) `1`.

Zählen Sie, wie oft Kopf bzw. Zahl auftritt und geben Sie die Anzahlen und die diskreten Wahrscheinlichkeiten von Kopf bzw. Zahl aus, indem Sie die gezählte Häufigkeit des Ereignisses durch die Anzahl der Versuche dividieren.

## Eigene Zufallsfunktion

Führen Sie analog 1.000.000 Versuche durch, ersetzen Sie aber den Aufruf der `rand()`-Funktion durch eine Iteration aus dem Buch von *Kernighan/Ritchie*, die Pseudozufallszahlen erzeugt:
    
> // Start der Iteration <br />
> x<sub>0</sub>  = 1
>
> // Aktuelle Iteration <br />
> // r<sub>i</sub>  ist aktuelle Zufallszahl <br />
> x<sub>i+1</sub>  = x<sub>i</sub> * 1103515245 + 12345 &nbsp; &nbsp; &nbsp; für  i = 0, 1, ...  <br />
> r<sub>i</sub>  = (x<sub>i+1</sub>  / 65536) % 32768
> 

Dabei wird die ganzzahlige Division angewandt und nicht die Fließkommadivision.  
Verwenden Sie statt  `int`  den Datentyp  `unsigned int`  (vorzeichenlose ganze Zahl) für die Variablen _x<sub>i</sub>_  und  _r<sub>i</sub>_ .  
Vermeiden Sie die Verwendung von Arrays sondern errechnen Sie nur die jeweils aktuelle Zufallszahl in Iteration `i`.
