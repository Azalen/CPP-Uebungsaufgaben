# Aufgabe 05: Arrays (Speicherallokation, tiefe und flache Kopie)

Realisieren Sie alle Aufgabenstellungen mit dynamischen eindimensionalen Arrays - d.h. mit Arrays, deren Speicher dynamisch über Zeiger erzeugt wird.

1.  Legen Sie zwei dynamische Arrays beliebiger - aber verschiedener - Länge an. Wenn das dynamische Anlegen eines der beiden Arrays scheitert, sollen Sie einen Warnhinweise ausgeben mit der Info, welches der Arrays nicht angelegt werden konnte. Nutzen Sie dazu die `try`- und `catch`-Anweisung, um das Gelingen der dynamischen Speicherallokation zu testen.
    ```c++
    // Hier dynamisches Array deklarieren
    try
    {
        // Hier Speicher für dynamisches Array erzeugen und zuweisen
        test = true;
    }
    catch(bad_alloc & exc)
    {
        test = false;
    }
    ```

2.  Legen Sie ein drittes Array an, welches mindestens soviele Komponenten enthalten kann, wie das größere der ersten Beiden. Kopieren Sie testweise das erste Array in das Dritte und geben Sie das dritte Array in voller Länge aus. **Achtung!** Hier ist eine _tiefe Kopie_ nötig! 
    
3.  Realisieren Sie eine Wertzuweisung der beiden Zeiger d.h. `dritter Zeiger/Array = erster Zeiger/Array`. Was stellen Sie fest, wenn Sie das dritte Array in der Länge des ersten Arrays ausgeben? Was, wenn Sie es in der Länge des dritten Arrays tun? Was passiert? Warum nennt man dieses Verhalten eine _flache Kopie_?

4.  Berechnen Sie die Summe der ersten beiden Arrays komponentenweise (d.h. legen sie eine neues Array für an), wobei Sie für das kürzere Array nach dessen Ende mit Nullen rechnen. Geben Sie dazu alle drei Arrays so aus, das man einfach erkennen kann, ob korrekt gerechnet wurde.

5.  Berechnen Sie die Summe der ersten beiden Arrays testweise falsch, indem Sie den dritten Zeiger auf die Summe der ersten beiden Zeiger setzen. Merkt der Compiler, dass dies eigentlich unsinnig ist? Wenn ja, geben Sie den Compilierfehler an, wenn nein, wie kann man das Ergebnis erklären?

### Hinweise:

-   Vermeiden Sie unbedingt die Entstehung von ungenutztem angelegten Speicher, der nicht mehr freigegeben werden kann
-   Vermeiden Sie unbedingt, dass Arraykomponenten in einem angelegten dynamischen Array bei der Verwendung noch uninitialisierte Werte haben
-   Auch Zeiger kann man ausgeben! Als Zeigerwert erscheint die zugehörige Speicheradresse als hexadezimale Zahl (beginnend mit dem Präfix "0x"), auf die der Zeiger zeigt
