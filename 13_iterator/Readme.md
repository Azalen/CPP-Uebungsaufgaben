# Aufgabe 13: Iteratoren (vector, set, map)  

Viele Datenstrukturen in der STL (Standard Template Library) besitzen keinen Index-Zugriff und können daher nicht mit einer regulären for-Schleife durchlaufen werden, um bspw. alle Elemente auszugeben.
```c++
// STL VECTOR -> funktioniert, da für den Vector der Indexoperator [] implementiert/überladen ist 
vector<int> vec = {1, 2, 3, 4, 5};
for(int i = 0; i < vec.size(); i++)
    cout << vec[i] << endl;

// STL SET -> funktioniert nicht, da für das Set der Indexoperator [] nicht (!) implementiert/überladen ist 
set<int> set = {1, 2, 3, 4, 5};
for(int i = 0; i < set.size(); i++)
    cout << set[i] << endl;  
```

Damit es trotzdem möglich ist, durch solche Datenstrukturen zu laufen existieren Iteratoren. Diese können von vorwärts und rückwärts implementiert sein und/oder auch als `const_interator` d.h. nur mit Lesezugriff auf die Elemente der Datenstruktur. Die Nutzung von Iteratoren in Schleifen läuft über zwei spezielle Funktionen: `begin()` und `end()` welche Zugriff auf das erste Element der Datenstruktur und auf das Element nach dem letzten Element (also ein Pseudo-Letztes-Element) liefern. Um das Element der Datenstruktur zu erhalten muss der Iterator dann derefenziert werden (streng genommen ist der *-Operator für die Iterator-Klasse überladen).

```c++
set<int> s = {1, 2, 3, 4, 5};
for(set<int>::iterator it = s.begin(); it != s.end(); ++it)
    cout << *it << endl;
```

### Anforderungen

Nutzen Sie Iteratoren um in der angegebenen Zahlenmenge (engl. set) den Wert mit der größten Quersumme zu finden.

```c++
set<int> nums = {23, 42, 61, 84, 91, 92, 87, 9, 101, 105};
```

Nutzen Sie Iteratoren um in der angegebenen Abbildung (engl. map) den Namen mit der größten zugeordneten Zahl zu finden.
```c++
map<string, int> m;
m["Celine"] = 1;
m["Domme"] = 5;
m["Basti"] = 7;
```

### Hinweise:

- Das keyword `auto` ist hilfreich, um den Datentyp der Iteratoren nicht jedesmal ausschreiben zu müssen
- die STL-map ist über Paare (z.B. `pair<string, int>`)implementiert, deren Elemente mit `.first` und `.second` zugreifbar sind
