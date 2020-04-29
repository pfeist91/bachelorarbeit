# Quellcode Bachelorarbeit
Dieses Repository enthält den Quellcode für meine Bachelorarbeit "Automatische Zusammenfassung von (Unter-)Kapiteln in englischsprachigen Lernskripten der IUBH". Er basiert auf dem "Pointer generator + coverage"-Modell von [@abisee](https://github.com/abisee) und wurde entsprechend angepasst, sodass er als Jupyter Notebook auf der Google Colab Umgebung ausgeführt werden kann.

## Ursprünglicher Quellcode
Das ursprüngliche Modell und der dazugehörige Quellcode können im [Github-Repository](https://github.com/abisee/pointer-generator) von [@abisee](https://github.com/abisee) abgerufen werden. Dort finden sich auch weitere nützliche Informationen, wie z. B. ein vortrainiertes Modell.

## HowTo
Die train-Datei dient zum Trainieren des neuronalen Netzes. Die eval-Datei dagegen zur parallelen Überprüfung der von der -train-Datei erstellten Checkpoints. Jenes Modell, das den geringsten "running avg loss"-Wert aufweist, wird vom Eval-Prozess gespeichert.

### Vorbereitungen
Bevor mit dem Training des Modells gestartet werden kann, müssen die Datensätze entweder selbst vorverarbeitet oder aber die bereits vorverarbeiteten Daten heruntergeladen und entpackt werden. Siehe dazu folgendes [Github-Repository](https://github.com/abisee/cnn-dailymail). Die Dateien können direkt im Google Drive entpackt werden, siehe dazu die ersten beiden Abschnitte im train-Notebook.

### Neuronales Netz trainieren
Nachdem die Daten entpackt und die Pfade im train-Notebook entsprechend angepasst wurden, kann mit dem Training des Modells begonnen werden. Dazu sollten für die Parameter *FLAGS.max_enc_steps* und *FLAGS.max_dec_steps* zunächst kleine Werte gewählt werden, z. B. 50 und 15.
Nachdem das Training gestartet wurde, sollte parallel das eval-Notebook mit den gleichen Parametern gestartet werden. Für Details siehe [hier](https://github.com/abisee/pointer-generator#how-to-run).

### Text zusammenfassen
Mithilfe des decode-Notebooks können entweder Zusammenfassungen aus dem CNN/Dailymail - Datensatz angefertigt werden oder aber auch eigene Texte eingebunden werden. Das Modell erwartet diese jedoch als .bin-Datei. Für die Konvertierung siehe [@dondon2475848](https://github.com/dondon2475848/make_datafiles_for_pgn).
