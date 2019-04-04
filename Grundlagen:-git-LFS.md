Für große Dateien haben wir angefangen auf [git-lfs](https://git-lfs.github.com/) zu setzen. Hierbei werden große Dateien nicht mehr ganz so schlimm in die History des git eingebaut.
Das war mit mehreren MB großen Bildern schon schlimm, aber noch verkraftbar. Insbesondere große Videos sollten allerdings nicht direkt im git abgelegt werden.

Zur Verwendung von git-lfs muss die git-lfs command line extention installiert sein!
Die geschieht auf den gängigsten Platformen zB. mit:


```bash
sudo apt install git-lfs
```
oder
```bash
sudo pacman -S git-lfs
```
