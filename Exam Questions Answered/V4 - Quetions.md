1. Wie wird ein Naive Bayes Classifier trainiert? Was muss beim Training für die spätere Klassifikation abgespeichert werden?

```
Der Naive-Bayes Classifier wird überwacht trainiert. Dabei wird ein Classifier mit den Wahrscheinlichkeiten traineirt, das ein wort w in einem Dokument der Klasse C_j vorkommt.

Die Variables cc und fc müssen abgespeichert werden
- cc(cat): Anzahlder Trainingsdokumente der Kategorie cat
- fc(w,cat): Anzahl der Traiingsdokumente der Kategorie cat in denen das Wort w vorkommt
```

2. Wie teilt ein Naiver Bayes Classifier ein neues Dokument ein?

```
Mit Hilfe der posteriori Wahrschenlichkeit.

Diese wird mit der Likelihood-Funktion, Evidenz und der a-priori Wahrscheinlichkeiten berechnet.
```

3. Welche naive Annahme liegt dem Bayes Classifier zugrunde? Ist diese Annahme im Fall der Dokumentklassifikation tatsächlich gegeben?

```
Annahme: Alle Eingabevektoren sind unabhängig voneinander.
- Nein, da Wörter in Dokumenten voneinander abhängig sind.
```

4. Betrachten Sie die Formeln für die Berechnung von 𝑃(𝐺|𝐷) und 𝑃(𝐵|𝐷). Welches Problem stellt sich ein, wenn in der Menge 𝑊(𝐷) ein Wort vorkommt, das nicht in den Trainingsdaten der Kategorie 𝐺 vorkommt und ein anderes Wort aus 𝑊(𝐷) nicht in den Trainingsdaten der Kategorie 𝐵 enthalten ist? Wie könnte dieses Problem gelöst werden?
![[Pasted image 20250114215732.png]]

```
P(w|G) bzw. P(w|B) sind 0 wenn w nich in G oder B ist, somit würde auch das Produkt in P(G|D) bzw. P(B|D) gleich 0 sein. Dadurch sind dann auch P(G|D) bzw. P(B|D) gleich 0 wodurch D mit einer Wahrscheinlichkeit von 0 in B bzw. G ist. Das Problem könnte gelöst werden wenn man eine Standard wert einführt (zb. 0.1), damit nicht durch ein einzelens Wort in einem Dokument D, das nicht in den Trainingsdaten ist, ein Dokument nicht zugewiesen werden kann.
```

5. Wie könnte die Klassifikationsgüte durch Modifikation der `getwords()`\-Methode verbessert werden?
![[Pasted image 20250114215929.png]]

```
Eine denkbare Modifikation wäre das Zähzlen: Wie oft ein Wort in eine Artikel vorkommt. Diese Zusatzinformation wird auch beim trainieren verwendet.

Somit werden die Wörte nach Häufigkeit gewichtet.
```

6. Für einen Beispielsatz erhalten Sie die bedingten sowie die a-priori Wahrscheinlichkeiten. Berechnen Sie für die gegebenen Wahrscheinlichkeiten die dazu gehörige Klasse?
![[Pasted image 20250114220243.png]]

```
Bad:  0.3 * 0.5 * 0.167 * 0.5 = 0.0125
Good: 0.7 * 0.167 * 0.5 * 0.5 = 0.029
```

7. Gegeben ist ein Bild einer Confusion Matrix. Berechnen Sie für die gegebenen Werte die Accuracy (Recall, Precision). Schreiben Sie dafür erst die Formel auf und berechnen Sie diese dann.
![[Pasted image 20250114220623.png]]

```
Accuracy = TP+TN/TP+TN+FP+FN
         = 2+5/2+5+1+2 = 7/10 = 0.7

Precision = Class 1: TP/TP+FP; Class 2: TN/TN+FN
		  = Class 1: 2/2+1 = 2/3 ; Clas 2: 5/5+2 = 5/7

Recall = Class 1: TN/TN+FN ; Class 2: TN/TN+FP
	   = Class 1: 2/2+2 = 2 ; Class 2: 5/5+1 = 5/6
```

8. Beschreiben Sie in Worten was die Accuracy-Metrik (oder Recall und Precision) aussagt bzw. wie diese zu interpretieren ist?

```
Accuracy: Gibt den Anteil der korrekt klassifizierten datenpunkten an allen Datenpunkten an
- 100% = Alle Datenpunkte wurden richtig erkannt
- Funktioniert gut, wenn die Daten gleich verteilt sind

Precision: Misst wie viele der als positiv vorhergesagten Datenpunkte, tatsächlich zur positiven Klassen gehören
- Hohe Precision: Das Modell erzeugt kaum falsche Alarme
- Wichtig bei Genauigkeit der positiven Vorhersagen

Recall: Misst wie viele der tatsächlichen positiven Datenpunkte korrelt als positiv vorhergesagt wurden
- Hoher Recall: Wenig positive Datenpunkte werden übersehen
- Wichtig wenn alle positiven Fälle erkannt werden sollen
```
