 Anleitung für Linux:
===========

1. Installiere git-lfs, was du für downloaden der Webseite benötigst.
([Siehe](https://github.com/ToolboxBodensee/toolbox-webseite/wiki/Installation))
*Dies muss man nur einmal machen, dann ist es installiert!*
```bash
# Kurzfassung:
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
```
2. Dieses Repository forken oder einen neuen Branch erstellen (übers [GitHub Interface](https://github.com/toolboxbodensee/tollbox-webseite.git))
3. Geforktes Repository auf deinen Computer clonen
```bash 
git lfs clone https://github.com/<dein_github_benutzer>/toolbox-webseite.git
```
*Wenn das schief geht, dann hast du vermutlich git-lfs nicht korrekt installiert.*

3. Öffne deine Kommandozeile im geklonten Repository-Fork 
```bash
cd toolbox-webseite
```
5. Installiere dir lektor, um die Webseite zu bearbeiten. ([Siehe](https://github.com/ToolboxBodensee/toolbox-webseite/wiki/Installation))
```
# Kurzfassung
make install
```

6. Webseite updaten... (unter [http://localhost:5000/](http://localhost:5000/))
```
make server
```
7. Lektor Beenden (``Strg. + C``)
8. Änderungen commiten 
```
git add --all
git commit -m "An der Webseite habe ich ____ geändert"

```
8. Änderungen hochladen
```
git push
```
9. Pull Request Stellen (übers GitHub Interface)


**Hinweise**
-  Die Versionskontrolle der Webseite findet über Git statt. Daher wenn möglich Bilder erst
bearbeiten und dann veröffentlichen. Denn sonst sind alle Versionen der Bilder für immer in der History der Webseite gespeichert. 
