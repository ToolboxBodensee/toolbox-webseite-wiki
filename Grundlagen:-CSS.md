Das CSS-Design wird mit [sass](https://github.com/sass/node-sass) generiert.
Das vereinfacht die Verständlichkeit der einzelnen Designelemente
und ermöglicht auch das Anpassen des Designs durch das simple Verändern weniger Variablen.
Für die 
Example use and installation:
```bash
# Install sass:
gem install sass
# generate css from sass
make sass
```

**Nützliche Tipps:**
Nahezu das gesamte Design der Webseite wird über die main.min.css datei geregelt. Diese befindet sich jedoch nicht mehr im git sondern muss lokal gebaut werden.
Das Lektor Template prüft, ob die Datei ``assets/css/main.min.css`` vorhanden ist. 
Sollte keine der genannten Dateien verfügbar sein, so wird diese von der offiziellen toolbox-bodensee.de Webseite eingebunden. Wenn sie lokal verfügbar ist, wird die lokale Datei eingebunden.
Der lokale Lektor Server cached einige Dateien. So kann es sein, dass das nachträgliche hinzufügen der css Datei keine Beachtung findet und nicht zum neu Einbinden seitens lektor führt.
Der lokale cache kann mit den folgenden Befehl geleert werden und anschließend der lokale Server wieder gestartet werden. Hierbei werden assets wie css und js mithilfe von webpack neu compiliert und komprimiert:
```bash
# clean lektor cache
lektor clean

# generate assets and run lektor server
lektor server -f webpack
```