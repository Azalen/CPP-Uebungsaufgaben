# Aufgabe 11: Kreis

![](https://t3.ftcdn.net/jpg/01/27/67/06/360_F_127670641_O3hzqpED3RHtsswdeBmDVUndKbWiv1WA.jpg)

Schreiben Sie eine Klasse `Kreis`. Ein Kreis besitzt einen Mittelpunkt im zweidimensionalen Raum und einen Radius. Weisen Sie dem `Kreis` außerdem eine `Farbe` zu. Um welche Art von Klassenbeziehung handelt es sich bei `Kreis` und `Farbe` (Fachbegriff!) und wie wird diese in C++ umgesetzt? Welche Arten von Klassenbeziehungen kennen Sie außerdem?

Schreiben sie **objektabhängige** Methoden um den Umfang und den Flächeninhalt eines Kreises zu berechnen! Schreiben Sie eine eine **objektunabhängige** Methode um den Abstand zwischen zwei Punkten im zweidimensionalen Raum zu berechnen (Hinweis: Pytagoras)! 

Überladen Sie den Operator `/` für zwei Kreise. Dieser soll angeben, ob sich die zwei Kreise schneiden (`true`) - oder eben nicht (`false`). Implementieren Sie dies in den aus der Vorlesung bekannten Varianten d.h. einmal als objektabhängige Methode innerhalb der Klasse und einmal als globale Funktion mit Hilfe des `friend`-Mechanismus/Deklaration (eventuell müssen Sie zum Testen immer eine der beiden Varianten auskommentieren).


## Anregungen / Tipps

- Klassenbeziehungen wurden speziell in OOAD besprochen
- Zu Testzwecken ist eine Ausgabefunktion für Kreise sicher sinnig
- bei der Operatorüberladung ist die `const`-Correctness von besonderer Bedeutung
