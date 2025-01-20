1. Was sind Eigenvektoren und Eigenwerte?

```
Eigenvektoren:
- Eigenvektoren sind die Vektoren innerhlab der transformierten Matrix und ändern ihre Richtung nicht bei einer linearen Abbildung und werden nur skaliert.

Eigenwerte:
- Eigenwerte gteben an, wie viel Information von jedem Eigenvektor beschrieben wird. Höhrere Eigenwerte = Eigenvektor erklärt einen größeren Anteil der Unterschiede in den Bildern
```

2. Was versteht man unter Eigenfaces?

```
Eigenfaces sind Eigenvektoren und werden so genannt wenn diese für Gesichtserkennung verwendet werden.
```

3. Wie kann mit der PCA eine Dimensionsreduktion durchgeführt werden?

```
1. Normierung
2. Berechnung der COvarianzmatrix
3. Eigenvektoren und Eigenwerte der Kovaruanzmatrix bestimmen
4. Ordnen der Eigenvektoren und Festlegung der Anzahl der Dimensionen im transformierten Raum
5. Daten transformieren
```

4. Wie werden mit dem Python Modul `image`von matplotlib Bilder in ein Python-Programm geladen?

```
Mit der image.imread()-Methode
```

5. Die Gesichtserkennung mit der Eigenface-Methode besteht aus einer Trainings- und Erkennungsphase. Erklären Sie jeweils kurz die notwendigen Schritte in der jeweiligen Phase.

```
Trainingsphase:
- Ein Model wird erstellt, welches die Hauptmerkmale der Trainingsgesichter beschreibt
- Die 5 Schritte der PCA Dimensionalitätsreduktion werden angewendet

Erkennungsphase:
- Eneuen Gesicht wird mit dem Modell verglichen
- Das Bild muss auf die gleiche Weiße vorverarbeitet werden wie in der Trainingsphase
- Projektion in den Eigenface Raum
- Vergleich mit den Trainingsdaten
- Klassifikation
```

6. Unter welcher Annahme ist eine Dimensionalitätsreduktion eines N^2 großen Raums (NxN großes Bild) in einen K-dimensionalen Unterraum zulässig?

```
Annahme: Die Daten liegen in einer niedrigdimensionalen Teilmenge der hochdimensionalen Raums
```

7. Sie bekommen einen Scatter-Plot für ein 2D-Koordinatensystem. Zeichnen Sie die Hauptachsen ein (Lage des ersten Eigenvektors sowie die Lage des zweiten Eigenvekors). Zeichnen Sie zusätzlich die proportionalen Längen der Eigenwerte ein (Länge muss nicht exakt sein).
![[Screenshot 2025-01-15 103420.png|400]]
![[Pasted image 20250115103426.png|400]]

