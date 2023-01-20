# Aufgabe 12: Bibliothek (Vererbung, Assotiation) 

Eine `Bibliothek` hat `Verleihobjekte` mit einer eindeutigen `Identifikationsnummer` und `Mitarbeiter`. `Verleihobjekte` können `Bücher` oder `Hörspiele` sein. `Bücher` haben einen `Titel`, einen `Autor`, ein `Genre` und eine `Seitenanzahl`. `Hörspiele` haben einen `Titel`, einen `Vorleser`, ein `Genre` und eine `Dauer`. Die `Genres` sind _Krimi_, _Fantasy_ und _Science-Fiction_. Ein `Autor` sowie auch ein `Mitarbeiter` hat einen `Vor`- und einen `Nachnamen` sowie ein `Geburtsdatum`. Ein `Mitarbeiter` hat außerdem ein `Jahresgehalt`. Ein `Datum` hat einen `Tag`, einen `Monat` und ein `Jahr`. 

Realisieren Sie die `Bibliothek` als **vollständigen** Klassenentwurf.

Überladen Sie desweiteren den Output-Stream-Operator für `Bücher`, sodass diese leicht mit `cout <<` verwendet werden können. Sie können hierbei - aber müssen nicht - den `friend`-Mechanismus verwenden.
```c++
ostream & operator<<(ostream & os, const Buch & b);
```
Hinweis: Beim Aufruf `cout << b` ist der Stream - also `cout` - der erste Parameter und das Buch `b` der zweite Parameter. D.h. man könnte selbige Funktionalität auch durch den Funktionsaufruf `operator<<(cout, b)` erreichen.

**Bonus:** Ein Buch hat nicht nur einen Autor, sondern der Autor eigentlich auch Bücher, die er verfasst hat. Bilden Sie dies ab! Hinweis: Vorwärts-Deklaration.

### Hinweise:

- Es kann - aber muss nicht - mehrmals Vererbung verwendet werden
- Enums können Arbeit abnehmen
- Kommentieren Sie in den Headerfiles an welcher Stelle Vererbung und an welcher Stelle Assotiationen Anwendung finden
