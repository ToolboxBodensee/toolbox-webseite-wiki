Lektor ist alsPython-Modul verfügbar und kann mit ``python2 -m lektor`` verwendet werden.
Auch die Installation über pip *(in einem [virtuellen Enviroment](https://docs.python.org/3/tutorial/venv.html)* ist möglich:
```bash
# create virtual enviroment
virtualenv venv
# activate virtual enviroment
. venv/bin/activate
# install lektor to virtual enviroment
pip install lektor

# install ruby-sass (for css styles)
gem install sass
```

Zum Starten von Lektor muss man mit der Komandozeile in das root-Verzeichnis der Webseite gehen
und dort mit dem Befehl ``lektor server`` Lektor starten. Im Browser kann dann 127.0.0.1:5000 aufgerufen werden, um die Webseite zu bearbeiten. Die Versionskontrolle der Webseite findet über Git statt. Daher wenn möglich Bilder erst
bearbeiten, bevor diese veröffentlicht werden!

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