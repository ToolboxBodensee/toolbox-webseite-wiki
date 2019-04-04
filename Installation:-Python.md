Für die Installation mit Python muss der Source Code von git geladen werden. Hierzu werden folgende Programme benötigt:
- git
- git-lfs

Die geschieht auf den gängigeren Linux Platformen zB. mit:
```bash
sudo apt install git git-lfs
```
oder
```bash
sudo pacman -S git git-lfs
```
Eine Installation ist entsprechend auch auf Windows und Mac möglich (eine entsprechende Installationsanleitung findet sich nach kurzer Such mit der Suchmaschine deiner Wahl)

Für die Installation von Lektor und weiteren benötigten Programmen muss in der Kommandozeile in das root-Verzeichnis der Webseite gewechselt werden. Die Installation erfolgt mit
```bash
make install
```
Auch die Installation *in einem [virtuellen Enviroment](https://docs.python.org/3/tutorial/venv.html)* ist möglich mit:
```bash
make install-virtual-env
```

Auch zum Starten des Servers muss in das root-Verzeichnis der Webseite gewechselt werden. Der Server lässt sich mit
```bash
make server
```
starten. Im Browser lässt sich die Webseite dann mit http://localhost:5000/ aufrufen und auch bearbeitet werden.

Sollen während der Server läuft die Assets (css und javascript) neu gebaut werden, weil diese sich geändert haben, so lässt sich dies mit
```bash
make build
```
erreichen