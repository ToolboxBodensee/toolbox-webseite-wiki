Lektor ist als Python-Modul verfügbar und kann mit 
```bash
make install
```
installiert werden. Auch die Installation *in einem [virtuellen Enviroment](https://docs.python.org/3/tutorial/venv.html)* ist möglich mit:
```bash
make install-virtual-env
```

Zum Starten von Lektor muss man mit der Kommandozeile in das root-Verzeichnis der Webseite wechseln
und kann dort mit
```bash
make server
```
den Lektor Server starten. Im Browser lässt sich die Webseite dann mit 127.0.0.1:5000 aufgerufen und auch bearbeitet werden.

Soll während der Server läuft die Assets (css und javascript) neu gebaut werden, weil diese sich geändert haben, so lässt sich dies mit
```bash
make build
```
erreichen