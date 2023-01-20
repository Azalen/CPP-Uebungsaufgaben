# Aufgabe 03: Ein- und Ausgabe (fstream, get, put, stream-operatoren, EOF)  

Schreiben Sie ein C++-Programm, das eine Datei einlesen soll und den Inhalt (genauer: alle Zeichen, die Kleinbuchstaben sind) in Großbuchstaben in einer neu anzulegenden Datei abspeichern soll.

-   Lassen Sie die Namen für die einzulesende und die zu erstellende Datei einlesen
-   Prüfen Sie, ob die einzulesende Datei existiert und lesbar ist und ob die zu erstellende Datei noch nicht existiert (Trick überlegen!), aber schreibbar ist.
-   Die eingelesen Zeichen, die keine Kleinbuchstaben sind, sollen natürlich nicht verändert werden (soweit sie überhaupt beim Einlesen berücksichtigt werden).
-   Wenn man führende Whitespaces beim Zeicheneinlesen nicht automatisch überlesen will, muss man die `get`-Methode verwenden, die genau ein Zeichen (auch ein Whitespace) einlesen kann. Analog zur üblichen Ausgabe gibt es auch eine `put`-Methode (die aber genauso wie die Ausgabe eines Zeichens mit cout funktioniert).  

    **Beispiel:**
    
         char c;
         ...
         cout << "Zeichen: ";
         cin.get(c);       // statt: cin >> c;
         cout << "Kontrollausgabe des Zeichens: ";
         cout.put(c);      // statt: cout << c;
         
    
    Die `get`- und `put`-Methoden kann man auch mit  `ifstream`- bzw.  `ofstream`-Objekten (statt regulär mit `cin` und `cout`) aufrufen.

-	Fragen Sie vom Nutzer ab, ob die Ein- und Ausgabe mit den Operatoren `<<` und `>>` oder mit `put`- und `get`-Methoden erfolgen sollen.
    
    **Frage:** Wodurch unterscheiden sich beide Varianten beim Umschreiben in Großbuchstaben?
    
-	Lesen Sie solange aus der Quelldatei, bis ein Fehler auftritt oder das Dateiende (`EOF` = end of file) erreicht ist.

## Tipps: 
-   Zum einfachen Verständnis spricht nichts dagegen Filestreams analog zu `cin/cout` mit `fin/fout` zu benennen
