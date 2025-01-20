___
1. Beschreiben Sie kurz das Clustering-Verfahren KMeans. Was sind die jeweiligen Vor- und Nachteile dieser Methode?

```
Die Schritte hinschreiben!

Bei dem KMeans Clustering Verfahren werden anfangs zufällige Cluster Mitten ausgewählt.
Die Trainingsdaten werden dem Cluster zugewiesen, wessen Mitte am nächsten ist. Für jedes Cluster wird die Mitte neu ermittelt in dem der Schwerpunkt von allen Trainigsdaten berechnet wird, welche zu einem Cluster zugeteilt wurden. Wenn sich die Mitten der Cluster nicht mehr verschieben ist das Clustering fertig.

Vorteile:
- Rechneffizient, besonders für große Datenmengen
- Kann dzrch Vorverarbeitung (z.b. PCA) an viele Datenarten angepasst werden

Nachteile:
- Anzahl der k CLuster muss im Voraus definiert werden
- Zufällige Startwerte für den Zentriod, führen zu unterschiedlichen Ergebnissen
- Empfindlich gegenüber Outliern
```

2. Beschreiben Sie kurz das Clustering-Verfahren DBSCAN. Was sind die jeweiligen Vor- und Nachteile dieser Methode?

```
Die Schritte hinschreiben!

Der DBSCAN ermöglicht es, Cluster in einem Datensatz zu identifizieren der nicht nur auf räumlicher Nähe, sondern auch auf Dichte basiert. Anders als bei K-Means benötigt DBSCAN keine im voraus festgelegten Cluster. Somit ist dieser Algorithmus flexibler als andere.
Ein zufällig nicht besuchter Kernpunkt wird ausgewählt und alle erreichbaren Punkte in seiner Nachbarshaft werden identifiziert. Diese Punkt bilden ein Cluster. Dieser Vorgang wird nun wiederholt, indem er neue Kernpunkte findet, die nicht Teil eines Clusters sind, und die Nachbarschaft jedes Kernpunkts durchsucht, bis alle Kernpunkte besucht wurden.

Vorteile:
- Markiert isolierte Punkte als Rauschen
- Anzahl der Cluster muzss nicht festgelegt werden
- Funktioniert gut bei großen Datensätzen

Nachteile:
- Es kann schwirig sein Ausreißer zu behandeln
- Hängt stark von den gewählten Parametern ab
- Anfällig für Datenskalierung und Distanzmetriken
```

3. Mit welcher Python-Bibliothek können Sie unkompliziert HTTP-requests durchführen?

```
Requests
```

 4. Angenommen Sie sammeln Daten von einem API-Endpoint aus dem Internet mit einer Python-Bibliothek. Wie können Sie sicherstellen, dass ihr Program bei Fehlern nicht abbricht? Nennen Sie drei Fehler oder die konkreten Exceptions die auftreten können.

```
Try-Except Block einbauen.

1. HTTPError: Wenn der Server eine HTTp-Antwort mit einem Fehlercode zurückgibt
2. Timeout: Wemm die maximale Zeit der Serveranfrage überschritten wird
3. TooManyRedirects: Falls in einer Schleife zu viele Weiterleitungen stattfinden
```

5. [Bild eines Pairplots] Beschreiben Sie was in den unterschiedlichen Quadranten dargestellt ist. Was wird in der Hauptdiagonalen dargestellt? Was können Sie aus den Nebendiagonalen ablesen?

```
Paitplot: Sammlung von Scatter Plots und Histogrammen
-> Beziehungen zwischen mehgeren Variablen im Datensatz

- Quadranten: Jeder Scatterplot stellt jeweils die Beziehnugnzwische zwei Variablen dar (X-, Y-Achse)
	- Zusammenhände: Positive, Negative, oder keine Korrelation
	- Verteilung: Clustern, die auf bestimmte Struktuzren im Datensatz hinweisen

- Hauptdiagonale: Jees Histogramm, steht für die jweilige Variable. Verteilung der Werte
	- Verteilungsform: Gleichmäßig oder nicht, verteilt
	- Ausreißer: Auffälige Werte

- Nebendiagonalen: Identisch zu dem oberen Quadranten, X-, Y-Achse gespiegelt.
	- Beobachtung: Für Bestätigung der Beziheungen zwischen den Variablen
```

 6. Wofür wird der PCA-Algrithmus verwendet?

```
- Dimensionsreduktion
```

 7. [Bild eines Beispiel-Clusterings wie im Notebook (Scatterplot, Barplots/Boxplots, Bilder)] Sie erhalten das Ergebnis eines Clusterings von Pokemon-Daten. Welche Merkmale (numerische oder kategorische) haben Ihrer Meinung nach den größten Einfluss auf das Ergebnis? Begründen Sie ihre Antwort anhand der verfügbaren Plots.

```
Sehr großen einfluss auf adas ergebnisse haben die Typen der Pokemon (kategrischen Merkmale).
Die Kategorischen Merkmale werden One Hot Encodiert, dadurch werden aus einem merkmale, 15 neue geneirert, welche einfluss auf das Clusteriung haben.

Das Merkt man deutlich an den unteren Clustern, den die Pokemn sind größtenteils nach Typ geclustert, was die Balkendauigramme verdeutlichen.

Die Numerischen Merkmale haben nicht viel Einfluss auf das Clustering, den wie auf den Boxplots zu erkennen, unterscheiden sich die Werte der 4 Cluster fast nicht. Diese könnten dann Einfluss haben, wenn es mehre Typen gibt und somit ein einheitliches Clusteruing nach Typ nicht mehr möglich ist.
```

8. Was berechnet der Silhoutte-Score?

```
Der Silhoutte-Score gibt an, wie gut die Datenpunkte innerhalb eines Clusters gruppiert sind und wie deutlich sie von anderen Clustern getrennt sind.
```

 9. Was kann man mithilfe der Elbow-Methode herausfinden?

```
Die Elbow-Methode dient zur Bestimmung der optiumalen Anzahl von Clustern in einem Datensatz.
```

10. Bonusfrage: Wie viele Pokemon gab es in der ersten Edition?

```
151
```

