# Versuch 1 - Supervised Learning, Datenexploration und -visualisierung

 1. [Bild von Classification Report und Confusion Matrix]. Sie erhalten einen Classification Report und eine Confusion Matrix eines trainierten Classifiers. Interpretieren Sie das Ergebnis.
 2. In welchen Fällen macht eine Kreuzvalidierung Sinn? Warum ist diese sinnvoll?
 3. [Bild verschiedener Scatterplots] Sie erhalten verschiedene Scatterplots von Fahrzeugdaten. Diskutieren Sie mögliche Korrelationen. Welche Merkmale korrelieren am stärksten mit der Zielvariable? Erscheint Ihnen das plausibel?
 4. Bei vielen Anwendungen macht eine Skalierung der Daten vor dem Training Sinn. Nennen Sie eine typische Skalierungsvariante. Warum darf die Skalierung erst nach dem Split in die beiden Partitionen ausgeführt werden? Worauf ist zu achten?
 5. Beschreiben Sie kurz die in der Funktion `determineRegressionMetrics()` verwendeten Metriken:

    ```Python
    def determineRegressionMetrics(y_test,y_pred,title=""):  
        mse = mean_squared_error(y_test, y_pred)  
        mad = mean_absolute_error(y_test, y_pred)  
        rmsle=np.sqrt(mean_squared_error(np.log(y_test+1),np.log(y_pred+1)))# +1 for avoiding log(0)   
        r2=r2_score(y_test, y_pred)  
        med=median_absolute_error(y_test, y_pred)  
        print(title)  
        print("Mean absolute error =", round(mad, 2))  
        print("Mean squared error =", round(mse, 2))  
        print("Median absolute error =", round(med, 2))  
        print("R2 score =", round(r2, 2))  
        print("Root Mean Squared Logarithmic Error =",rmsle)  
    ```
 6. Nennen Sie eine Library die den Python-Zugriff auf eine SQL Datenbank ermöglicht.
 7. Was macht die `info()`\-Methode eines Pandas-DataFrames?
 8. Was macht die `describe()`\-Methode eines Pandas-DataFrames?
 9. Welche Funktion kann verwendet werden um herauszufinden ob es `None`\- oder `NaN`\-Werte in einem Pandas-DataFrame gibt? Welche Funktion wird verwendet um diese zu entfernen? Mit welcher Methode kann man fehlende Werte ersetzen?
10. Wie kann man herausfinden welche einzigartigen Werte es in einer Column in einem Pandas-DataFrame gibt?
11. [Bild eines Boxplots mit durchnummerierten Bestandteilen] Erklären Sie die Bestandteile dieses Boxplots.
12. Sie haben einen Pandas-DataFrame mit numerischen und kategorischen Werten. Für welchen Datentyp verwenden Sie einen Barplot und für welchen Datentyp ein Histogram?
13. Erklären Sie den Unterschied zwischen einem Histogram und einem Barplot?
14. [Bild eines Histogram-Plots] Teilen Sie folgende Werte den passenden Histogram-Bins zu: `[0, 1, 1.5, 3]`
15. One-Hot encoden Sie folgende kategorischen Merkmale in einer neuen Tabelle: `[Rot, Grün, Blau, Grün, Blau]`
16. Sie haben einen numerischen Datensatz mit den Eingabedaten `X` (2d-array) und den Zielvariablen `y` (1d-array). Erklären Sie welche Schritte notwendig sind, um diesen Datensatz für Training und Evaluation eines Regressions-Modells vorzubereiten.
17. Nennen Sie zwei Strategien für eine Hyperparameteroptimierung und beschreiben Sie jeweils kurz das vorgehen?