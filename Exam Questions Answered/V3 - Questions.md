___
1. Nennen Sie zwei Verfahren mit denen sich Recommender Systeme umsetzen lassen.

```
UCF - User-based Collaborative Filtering
ICF - Item-based Collaborative Filtering
```

 2. Nennen Sie zwei Einsatzgebiete von Recommender Systemen und beschreiben Sie was dort empfohlen wird.

```
E-Commerce:
- Produkte, die ein utzer kaufen könnte, basierende auf seinem bisherigen Käufen, seinem Surfverhalten pder dem Verhalten ähnlicher Nutzer.

Streaming-Dienste:
- Filme, Serien oder Musik, die einem Nutzer basierend af seienn Vorlieben, Bewertungen oder dem Verhalten ähnlicher Nutzer gefallen könnten.
```

 3. Handelt es sich bei der dargestellten User-Item Matrix um ein User-based oder Item-based Verfahren?
![[Pasted image 20250113193035.png]]

```
Links: User-based Ansatz:
- Die Ähnlichkeit zwischen Nutzer wird ermittelt. Es wird überprüft welche Nutzer (U1, U2, etc.) ähnliche Werte in den Items haben.
- Vergleich von Zeilen

Rechts: Item-based Ansatz:
- Die Ähnlichkeit zwischen den Items wird ermittelt. Es wird geschaut welche Items eine ähnliche Bewertung vom Beutzer erhalten haben.
- Vergleich von Spalten
```

4. Beschreiben Sie das Prinzip des userbasierten Collaborativen Filtering (UCF). Welche Nachteile hat das UCF?

```
UCF ist ein verfahren, welches Empfehlungen anhand der Ählichkeit zwischen Nutzern ermittelt. Um für User1 eine Empfehlung zu erzeugen, wird zunächst der ähnlichste Kunde, oder Menge an Kuinden, ermittelt. Dann werden U1 die Items empfohlen, die dem ähnlichsten Kunde gekaut hat, U1 jeodch noch nicht.

Nachteile:
- Skaliert schznecht im Falle sehr großer User/Item-Matrizen
- Unzuverlössig für User, welche noch nicht viel gekauft haben
```

 5. Beschreiben Sie das Prinzip des itembasierten Collaborativen Filtering (ICF). Welche Vorteile hat das ICF?

```
ICF ist ein Verfahren, welches Empfehlungen anhand der Ähnlichkeit zwischen Items ermittelt. rodukte sind umso ähnlicher, je mehr Kunden diese Produkte gemeinsam gekauft haben. Für ein Item1 werden die ähnlichsten Items ermittelt und dem User vorgeschgklagen, falls er sie nich nicht gekauft hat.

Vorteile:
- Skaliert gut im Falle sehr großer User/Item-Matrizen
- Die Empfehlungen sind stabilder, im Falle, dass das Nutzerverhalten sich ändert
```

6. Nennen Sie zwei bekannte Ähnlichkeitsmaße.

```
1. Euklidische Distanz
2. Pearson Korrelation
3. Cosinus Ähnlichkeitsmaß
```

7. In welchen Fällen sind Cosinus- und Pearsonähnlichkeit der euklidischen Ähnlichkeit vorzuziehen?

```
- Wenn nur die Richtung oder das Muster der Bewertung wichtig ist
- Wenn Normiereung der Daten erforderlich ist

- Wenn die lineare Beziehung zwischen Variablen wichtig ist
- Wenn Skalierungsunterschiede zwischen den Vektoren vorhanden sind
```

8. Zeichnen Sie die zwei Vektoren a=[1,2] und b=[2,1] in ein Koordinatensystem ein und markieren Sie die euklidische Distanz, sowie die geometrische Interpretation der Cosinus- Distanz.

![[Pasted image 20250113195258.png|500]]

```
- Die euklidische Distanz zwischen den Vektoren wird als grüne gestrichelte Linie dargestellt
- Die cosinus Distanze ist der Cosinus des Winkels 0 zwischen den beiden Vektoren
```

9. In welchen Fällen ist der Einsatz des Russel Rao- oder des Jaccard-Ähnlichkeitsmaßes sinnvoll?

```
- Bei binären Vektoren
- Wenn man nur die Anzahl er Merkmale berücksichtigen soll
```

10. Gegeben ist eine User-Item-Matrix mit Filmbewertungen und der berechneten euklidischen und Pearson Ähnlichkeit zwischen zwei Personen. Diskutieren Sie die unterschiedlichen Ähnlichkeitswerte. Worauf sind diese zurückzuführen?
![[Pasted image 20250113200419.png|500]]

```
- Die Eukloidische Distanz misst dem Abstand zwischen den Vektoren im Vektorraum
- Die Pearson Korraltion misst die lineare Korrealtion zwischen den Bewertungen zweier Benutzer
- Die PK konzntriert sich auf den Trens der Bewertungen, und die ED aud ei absoluten Unterscihede zwischen den Bewertungen
```