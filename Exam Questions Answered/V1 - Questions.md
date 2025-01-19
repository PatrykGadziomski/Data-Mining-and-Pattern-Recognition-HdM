___
 1. Bild von Classification Report und Confusion Matrix. Sie erhalten einen Classification Report und eine Confusion Matrix eines trainierten Classifiers. Interpretieren Sie das Ergebnis.

![[Pasted image 20250110124536.png|400]]![[Pasted image 20250110124759.png|400]]

```
Classification Report
	- Ein classification Report enthält die folgenden Metriken für jede Klasse: Precision, Recall, F1-Scpre und Support

Confusion Matrix
	- Doe Confusion Matrix gibt einen Überblick über die tatsächlichen und vorhergesagten Klassifikationen_ True Positive, True Negative und False Negative, False Positive

Intepretation:
	- Precision: Niedrige Precision in einer Klasse weist auf viele False Positives hin
	    - Zu weniger Trainingdaten für eine Klasse
	    - Feature ist nicht aussagekräftig genug für diese Klasse
    - Recall: Ein niedriger Recall zeigt, dass der Klassifikation viele tatsächlichen Instanzen der Klasse nicht erkennt
	    - Zu weniger Trainingdaten für eine Klasse
	    - Feature ist nicht aussagekräftig genug für diese Klasse
    - F1-Score: Diese Metrik ist wichtig, wenn Precision und Recall für eie Klasse stark variieren
    - Confusion Matrix: Identifiziert die Klassen, die häufig verwechselt werden. 
	    - Sind die Klassen ausreichend trennbar von einander?
	    - Die Feature-Selektion oder -Extraktion verbessern
	    - Sind die Daten gleichmäßig verteilt?
```

 2. In welchen Fällen macht eine Kreuzvalidierung Sinn? Warum ist diese sinnvoll?

```
Fälle:
- Kleine Datenmengen
- Modellvergleich
- Ungleichverteilung in der Datenverteilung
- Verlässliche Evaluierung

Sinn:
- Reduzierung von Bias und Varianz in der Evaluation
- Alle Datenpunkte werden sowohl für das Training als auch für das Testen verwendet
- Robustere Schätzung der Modellierung durch Verwendung von Mittelwert und Standardabweichung
- Erkennung von Datenabhängigkeit
```

 3. Bild verschiedener Scatterplots. Sie erhalten verschiedene Scatterplots von Fahrzeugdaten. Diskutieren Sie mögliche Korrelationen. Welche Merkmale korrelieren am stärksten mit der Zielvariable? Erscheint Ihnen das plausibel?

```
- Lineare, oder nicht-lineare Zusammenhänge?
- Stärke der Korrelation? Enge oder gestreute Punktwolkte?
- Korrelation der Merkmale in Hinsicht auf die Zielvariable

- Steile oder enge Stellen == Starke Korrelation
- Korrelationseffizienten zur Hilfe holen

Beispiele:
- Lesitung X Preis: Positive Korrelation, logisch -> Mehr Leistung == Mehr Herstellungkosten == Höhere Preis
- Treibstoffverbrauch X CO2-Austoß: Positive Korrelation, logisch -> Mehr Verbrauch == Mehr Ausstoß
- Alter X Preis: Negative Korrelation: Bedingt vom Marktpreis und nicht Alter

- Sind die Korrelationen erwartbar?
- Gibt es unerwartete Zusammenhänge?
```

4. Bei vielen Anwendungen macht eine Skalierung der Daten vor dem Training Sinn. Nennen Sie eine typische Skalierungsvariante. Warum darf die Skalierung erst nach dem Split in die beiden Partitionen ausgeführt werden? Worauf ist zu achten?

```
Typische Skalisierungvariante: Min-Max-Skalierung

Skalierung erst nach dem Split:
- Wenn die Skalierung vor dem Split durchgeführt wird, werden Informatinen aus den testdaten in den Mittelwert oder die Standardabweichung der Skalisierung einfließen. Dadurch wird ein Teil der Testdaten indirekt "bekannt".

Darauf ist zu achten:
- Die Skalierung muss für Trainings- und Testdaten getrennt erfolgen
- Die Skalierung wird ausschließlich auf den Trainingsdaten berechnet
- Skalierungsverfahren können von Ausreißern stark beeinflusst werden
```

5. Beschreiben Sie kurz die in der Funktion `determineRegressionMetrics()` verwendeten Metriken:

```python
    def determineRegressionMetrics(y_test,y_pred,title=""):  
        mse = mean_squared_error(y_test, y_pred)  
        mad = mean_absolute_error(y_test, y_pred)
rmsle=np.sqrt(mean_squared_error(np.log(y_test+1),np.log(y_pred+1)))
		r2=r2_score(y_test, y_pred)  
        med=median_absolute_error(y_test, y_pred)  

        print(title)  
        print("Mean absolute error =", round(mad, 2))  
        print("Mean squared error =", round(mse, 2))  
        print("Median absolute error =", round(med, 2))  
        print("R2 score =", round(r2, 2))  
        print("Root Mean Squared Logarithmic Error =",rmsle)  
```


```
mse: Mean Squared Error
- Der Durchschnitt der quadrierten Abweichung zwischen den vorhergesagten und tatsächlichen Werten

mae: Mean Absolute Error
- Der Durchschnitt der absoluten Unterschiede zwischen den vorhergesagten und tatsächlciehn werten

rmsle: Root Mean Squared Logarithmic Error
- Die Quadratwurzel des mittleren quadrierten Fehlers zwischen den logarithmierten tatsächlichen und vorhergesagten Werten

r2: R2-Score
- Maß für den Anteil der Varianz in den tatsächlichen Werten, die durch das Modell erklärt wird.

med: Median Absoluite Error
- Der Median der absoluten Fehler zwischen den vorhergesagten und tatsächlichen Werten
```

6. Nennen Sie eine Library die den Python-Zugriff auf eine SQL Datenbank ermöglicht.

```
sqlalchemy
```

7. Was macht die `info()`\-Methode eines Pandas-DataFrames?

```
Die Methode `info()` eines Pandas-DataFrames liefert eine kompakte Übersicht über die Struktur des DataFrames, einschließlich der wichtigsten Metainformationen.
```

 8. Was macht die `describe()`\-Methode eines Pandas-DataFrames?

```
Die Methode `describe()` eines Pandas-DataFrames erzeugt eine zusammenfassende Statistik für numerische oder kategorische Daten im DataFrame.
```

9. Welche Funktion kann verwendet werden um herauszufinden ob es `None`\- oder `NaN`\-Werte in einem Pandas-DataFrame gibt? Welche Funktion wird verwendet um diese zu entfernen? Mit welcher Methode kann man fehlende Werte ersetzen?

```
Herausfinden: .isnull() oder .isna() für None oder Nan Werte, .any() für fehlende Werte

Entfernen: .dropna() entfernt Zeilen oder Spalten, die fehlende Werte enthalten.

Ersetzen: .fillna() ersetzt fehlende Werte mit einem angegebenen Wert.
```

10. Wie kann man herausfinden welche einzigartigen Werte es in einer Column in einem Pandas-DataFrame gibt?

```
.unique() gibt ein array zurück, welche alle eindeutigen Werte in der Spalte enthält.

.nunique() gibt die Anzahl der eindeutigen Werte in der Spalte zurück.
```

11. Bild eines Boxplots mit durchnummerierten Bestandteilen. Erklären Sie die Bestandteile dieses Boxplots.

```
Box: Interquartilsbereich, der die mittleren 50% der Daten umfasst

Median: Die Linie innerhalb des Kastens stellt den media dar

Whiskers:Linien, die vom Kasten nach oben und unten führen und den Bereich der "normalen" daten anzeigen

Outlier: Datenpunkte, die außerhalb des Bereichs der Whiskers liegen

Minimum und Maximum: Kleinster und größter Wert innerhalb des normalen Bereichs
```

12. Sie haben einen Pandas-DataFrame mit numerischen und kategorischen Werten. Für welchen Datentyp verwenden Sie einen Barplot und für welchen Datentyp ein Histogram?

```
Numerische Daten: Histogtram

Kategorische Daten: Barplot
```

13. Erklären Sie den Unterschied zwischen einem Histogram und einem Barplot?

```
Sie dienne unterschiedichen Zwecken.

Histogram: Wird verwendet um die Verteilung eiener kontinuierlichen Variablen darzustellen. Er zeigt, wie oft Daten innerhalb von bestimmten Intervallen auftreten.

Barplot: Wird verwendet um kategorische Daten zu visualisieren und zu vergleichen. Er zeigt die Häufigket oder den Wert jeder Kategorie.
```

14. Bild eines Histogram-Plots. Teilen Sie folgende Werte den passenden Histogram-Bins zu: `[0, 1, 1.5, 3]`

```
Um die Werte [0, 1, 1.5, 3] den passenden Histogram-Bins zuzuordnen, müssen wir zunächst die Intervalle (Bins) des Histogramms bestimmen. Ein Histogramm zeigt die Häufigkeit der Werte in bestimmten Intervallen.
```

15. One-Hot encoden Sie folgende kategorischen Merkmale in einer neuen Tabelle: `[Rot, Grün, Blau, Grün, Blau]`

|  |rot|grün|blau
|---|---|---|---|
|rot| 1 | 0 | 0 |
|grün| 0 | 1 | 0 |
|blau| 0 | 0 | 1 |
|grün| 0 | 1 | 0 |
|blau| 0 | 0 | 1 |

16. Sie haben einen numerischen Datensatz mit den Eingabedaten `X` (2d-array) und den Zielvariablen `y` (1d-array). Erklären Sie welche Schritte notwendig sind, um diesen Datensatz für Training und Evaluation eines Regressions-Modells vorzubereiten.

```
- Auf fehlende Werte und Outlier überprüfen
- Skalierung der Daten
- Aufteilung der Daten in Training- und Testsets
- Modellwahl (Linear Regression, Logistic Regression, etc.)
```

17. Nennen Sie zwei Strategien für eine Hyperparameteroptimierung und beschreiben Sie jeweils kurz das vorgehen?

```
GridSearchSV
- Bei GridSearchCV wird eine vollständige Raster-Suche über alle möglichen Kombinationen von Hyperparametern durchgeführt, die im angegebenen Gitter (Grid) enthalten sind.

RandomizedSearchCV
- Bei RandomizedSearchCV wird eine zufällige Auswahl von Hyperparameter-Kombinationen aus einem angegebenen Bereich getestet. Anstatt alle Kombinationen zu durchlaufen, werden nur eine festgelegte Anzahl zufälliger Kombinationen ausgewählt und evaluiert.
```

