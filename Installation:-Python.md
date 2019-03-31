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