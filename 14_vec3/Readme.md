# Aufgabe 07: 3D-Vector

Schreiben Sie eine Klasse, welche einen (euklidischen) 3D-Vektor modelliert. 

**Anforderungen**
1. Einen Negationsoperator `-`, welcher einen neuen Vektor mit negativen Koordinaten zurückgibt
2. Einen Indexoperator `[]`, welcher eine Referenz auf die entsprechende Koordinate zurückgibt
3. Einen `+=`-Operator, welcher den aktuellen Vektor addiert um einen weiteren Vektor zurückgibt
4. Einen `*=`-Operator, welcher den aktuellen Vektor multipliziert mit einem weiteren Vektor zurückgibt
5. Eine Funktion `length()`, welche die Länge des Vektors errechnet

Außerdem Utility-Funktionen, welche außerhalb der eigentlichen Klassendefinition liegen:

6. Eine Operatorüberladung für `<<`, um einen 3D-Vektor mit `cout` ausgeben zu können
7. Eine Operatorüberladung für `+`, um zwei 3D-Vektoren addieren zu können

**Fragen:**
- Wieso kann bei dieser Implementation auf den `friend`-Mechanismus verzichtet werden? Bewerten Sie dies!
- Wieso wird beim `+=`-Operator eine `vec3`-Referenz zurückgegeben und nicht ein `vec3`-Instanz?
- Warum ist es bei dieser Klasse nicht nötig eigens Kopierkonstruktor, Zuweisungsoperator oder Destruktor zu definieren?

```c++
#ifndef VEC3_H
#define VEC3_H

#include <cmath>
#include <iostream>

using std::sqrt;

class vec3 {
    public:
        double e[3];

    public:
        vec3() : e{0,0,0} {}
        vec3(double e0, double e1, double e2) : e{e0, e1, e2} {}

        double x() const { return e[0]; }
        double y() const { return e[1]; }
        double z() const { return e[2]; }

        // ANFORDERUNG 1 - Negation
        vec3 operator-() const {

        }

        // ANFORDERUNG 2 - Indexzugriff
        Rueckgabetyp operator[](Paramter) { 

        }

        // ANFORDERUNG 3 - Plus-Gleich
        Rueckgabetyp operator+=(Paramter) {

            return *this;
        }

        // ANFORDERUNG 4 - Mal-Gleich

        // ANFORDERUNG 5 - Längenberechnung
        double length() const {
            
        }
};

// ANFORDERUNG 6 - Ausgabe
std::ostream & operator<<(std::ostream & out, const vec3 & v) {

}

// ANFORDERUNG 7 - Vektoraddition
Rueckgabetyp operator+(Parameter 1, Paramter 2) {
    
}

#endif
```
