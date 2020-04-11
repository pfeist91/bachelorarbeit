# Quellcode Bachelorarbeit
Dieses Repository enthält den Quellcode für meine Bachelorarbeit "Automatische Zusammenfassung von (Unter-)Kapiteln in englischsprachigen Lernskripten der IUBH". Er basiert auf dem "Pointer generator + coverage"-Modell von @abisee und wurde entsprechend angepasst, sodass er als Jupyter Notebook auf der Google Colab Umgebung ausgeführt werden kann.

## Ursprünglicher Quellcode
Das ursprüngliche Modell und der dazugehörige Quellcode können im [Github-Repository](https://github.com/abisee/pointer-generator) von @abisee abgerufen werden. Dort finden sich auch weitere nützliche Informationen, wie z. B. ein vortrainiertes Modell.

## HowTo
Die train-Datei dient zum Trainieren des neuronalen Netzes. Die eval-Datei dagegen zur parallelen Überprüfung der von der -train-Datei erstellten Checkpoints. Jenes Modell, das den geringsten "running avg loss"-Wert aufweist, wird vom Eval-Prozess gespeichert.

### Vorbereitungen

### Neuronales Netz trainieren

### Text zusammenfassen
