___
1. Nennen Sie vier mögliche Bildtransformationen, die zur Data Augmentation verwendet werden könne.

```
1. Rotation
2. Zoom
3. Width Shift
4. Height Shift
5. Shear
6. Vertical Flip
7. Horizontal Flip
```

2. Der Methode `models.fit_generator` kann zum Training ein Argument `class_weight` übergeben werden. Erklären Sie was dieses Argument beinhaltet und in welchen Fällen dieser hilfreich ist.

```
class_weight beinhaltet für jede Klasse den KLassenindex als key und den relativen Anteil dieser KLasse  als Value.

Fälle:
- Datensätze mit unterrepsentation bestimmter Klassen
```

3. Sie erhalten zwei Bilder von Verkehrsschildern, die nicht korrekt klassifiziert wurden. Lassen sich diese Fehlklassifikationen erklären? Und falls ja, erläutern Sie ihre Vermutung.

```
Erklärungen:
- Visuelle Ähnlichkeiten zwischen den Verkehrschildern
- Schlechte Beleucutng oder QUalität der Bilder
- Ungewöhnliche Perspektive und/oder Rotation
- Die Klassen, die schlecht erkannt wurden, sind unterrepräsentiert
- Hintergrundinformation im Bild beinflussen die Klassifizierung
```

4. Wie erhalten Sie einen Überblick über die definierte Architektur des neuronalen Netzes?

```
Mit dem Befehl model.summary()
```

5. Welche Aufgabe hat ein Dropout-Layer? Worauf ist während der Evaluationsphase/Testphase zu achten?

```
Durch den Dropout-Layer wird eine zufällige ANzahl an Weights ausgeschaltet (auf 0 setzen).
- Das hilft Overfotting zu verhindern.

Während der Testphase wird kein Dropout angewedet.
- Alle Weights sind aktiv.
- Dropout = 0.0
```

6. Welches Lernverfahren implementiert der Adam-Algorithmus?

```
Adam implemetniert ein Stochastic Gradient Descent-Lernverfahren, welches die LErnrate für die Gewichte individuell und dynamisch anpasst.
```

7. Sie haben einen Datensatz von 100 RGB-Bildern mit einer Auflösung von 32x32. Dieser wird in ein 4-dimensionale numpy-array `d` (Es wurde noch kein Train- und Testsplit durchgeführt). Was ist der output der Funktion `numpy.shape(d)` ? Was ist die Bedeutung der einzelnen Dimensionen?

```
Output: (100, 32, 32, 3)

0: Anzahl an Daten
1: Breite der Bilder
2: Höhe der Bilder
3: Anzahl der Kanäle
```

8. Was ist der Unterschied zwischen Convolution- und Pooling-Layern?

```
Convolution-Layer:
- Extrahiert Merkmale aus den Eingabedaten
- Berechnung neuer Feature-Maps
- Lernbare Gewichte

Pooling-Layer:
- Reduziert die Dimensionen der Daten und spart Ressourcen
- Berechnet einen zusammenfassenden Wert pro Region
- Keine Lernbare Gewichte
- Dient für eine kleine Invarianz
```
