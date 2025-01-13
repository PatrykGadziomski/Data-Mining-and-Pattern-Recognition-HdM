## Versuch 6 - Neural Networks

1. Nennen Sie vier mögliche Bildtransformationen, die zur Data Augmentation verwendet werden könne.
2. Der Methode `models.fit_generator` kann zum Training ein Argument `class_weight` übergeben werden. Erklären Sie was dieses Argument beinhaltet und in welchen Fällen dieser hilfreich ist.
3. Sie erhalten zwei Bilder von Verkehrsschildern, die nicht korrekt klassifiziert wurden. Lassen sich diese Fehlklassifikationen erklären? Und falls ja, erläutern Sie ihre Vermutung.
4. Wie erhalten Sie einen Überblick über die definierte Architektur des neuronalen Netzes?
5. Welche Aufgabe hat ein Dropout-Layer? Worauf ist während der Evaluationsphase/Testphase zu achten?
6. Welches Lernverfahren implementiert der Adam-Algorithmus?
7. Sie haben einen Datensatz von 100 RGB-Bildern mit einer Auflösung von 32x32. Dieser wird in ein 4-dimensionale numpy-array `d` (Es wurde noch kein Train- und Testsplit durchgeführt). Was ist der output der Funktion `numpy.shape(d)` ? Was ist die Bedeutung der einzelnen Dimensionen?
8. Was ist der Unterschied zwischen Convolution- und Pooling-Layern?