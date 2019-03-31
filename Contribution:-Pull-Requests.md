Es gibt zwei Möglichkeiten Pull Requests zu reviewen:

### Änderungen lokal Downloaden und Bewerten

1.  Die im Pull Request eingereichte Version clonen

```bash
# ID des Pull Request eintragen
PULLREQUEST=42
# Git-Repository clonen
git clone --depth=30 https://github.com/ToolboxBodensee/toolbox-webseite.git toolbox-pull-request
# In das Repo navigieren
cd toolbox-pull-request
# zum Pull Request wechseln
git fetch origin +refs/pull/$PULLREQUEST/merge:
git checkout -qf FETCH_HEAD
```

2.  Den geklonten Pull Request anschauen ``lektor server -f webpack``
3.  Änderungen requesten oder Pull Request approven

### Änderungen online reviewen

Die eingereichten Pull Requests werden automatisiert durch ein [Go-Skript](https://github.com/ottojo/pullRequestHost) und Travis auf ein Testsystem deployed. Nachdem die Travis-Checks durchgelaufen sind, kann man diesen Pull Request unter dem von einem bot geposteten Link anschauen. Auf GitHub sieht man, welche Dateien hier betroffen sind. Auf dem Testsystem sieht man, wie das fertige Ergebnis aussieht.
