Hat man auf seiner Host kein python oder will man *keine* zusätzliche Software installieren, so steht ein Docker Image `toolboxbodensee/lektor:latest` zur Verfügung.

Damit lässt sich das Projekt innerhalb eines *Containers* bauen und sogar der Lektor-Server ausführen.

Der Einfachheit halber stehen mehrere *make* **docker-** Befehle zur Verfügung. Der Projektordner sowie die Lektor-cache `.cache/lektor` werden als Volume zu der Container angehängt.

```bash
# lädt die Lektor Docker Image vom Docker Hub herunter
make docker-pull

# baut die Assets und die lektor cache (lektor build)
make docker-build

# führt den Lektor Server auf localhost:5000 aus
make docker-server

# führt eine Shell aus innerhalb des Containers. Diese kann man zum Debuggen nutzen.
make docker-shell
```

**Tipp:** Zum Verwenden von Docker muss ``docker`` installiert sein und als Service gestartet sein.<br/>
Außerdem muss dein User zur Gruppe docker gehören und sollte nicht als root ausgeführt werden!<br/>
Weitere Hinweise dazu u.a. auf [wiki.archlinux.org](https://wiki.archlinux.org/index.php/docker#Installation).
