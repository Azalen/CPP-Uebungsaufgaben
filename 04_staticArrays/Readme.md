# Aufgabe 04: Arrays (Index-Rotation/Permutation)  

**Arbeiten Sie mit statischen C-Arrays!**

1.  Legen Sie ein `double`-Array **y** an, das an Index  _i=0,1,...,N_, die Werte  _sin(x<sub>i</sub>)_  hat, wobei  _x<sub>i</sub>  = i*(pi/2 - 1/10)/N_  ist.  
    Erzeugen Sie ein weiteres `double`-Array  **kopie**, das zunächst dieselben Werte wie das Array  **y**  besitzen soll.
    
2.  Sortieren Sie das `double`-Array **kopie** um, indem Sie die Arraykomponenten um zwei Positionen nach vorne/links rutschen und als neuen vorletzten Wert den alten ersten Wert sowie als neuen letzten Wert den alten zweiten Wert verwenden.  
    Geben Sie die so veränderten Arraykomponenten zur Kontrolle aus.
    
3.  Legen Sie alternativ ein `int`-Array **rotation** an, dessen Arraykomponenten umgeordnete Indizes zum Zugriff auf das Array **y** enthalten sollen. Besetzen Sie das Array also so, dass es die Werte 2, 3, ..., N, 0 ,1 enthält.  
    Geben Sie die Komponenten des Array **y**  nun rotiert um zwei nach vorne/links aus, indem Sie statt dem Index `i` den Index `rotation[i]` verwenden.
    
4.  Erzeugen Sie eine zufällige Indexpermutation (d.h. ein `int`-Array **perm** mit einer zufälligen Anordnung der Zahlen 0, 1, ..., N), indem Sie wie folgt vorgehen:  
    - Bestimmen Sie eine zufällige ganze Zahl zwischen 0 und N und setzen Sie diese als den Wert `perm[0]`
    -  Für einen Index `i` von 1 bis N bestimmen Sie eine neue zufällige ganze Zahl zwischen 0 und N und prüfen Sie solange, ob diese Zufallszahl schon im bisher besetzten Arrayteil von **perm** vorhanden ist, bis Sie eine noch nicht vorkommende Zahl bestimmt haben
    -  Speichern Sie dann diese Zufallszahl in `perm[i]`
  
5.  Geben Sie die so permutierten Komponenten des Arrays **y** sowie die Anzahl der Indizes `i`, die durch die Indexpermutation nicht verändert werden, aus.
