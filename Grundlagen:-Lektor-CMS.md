Das CMS für diese Webseite ist [Lektor](https://www.getlektor.com/).<br/>
Die Installationsanleitung gibt es [hier](https://www.getlektor.com/downloads/).<br/>
Für Bilder im git verwenden wir [git-lfs](https://git-lfs.github.com/). Weitere Informationen dazu gibt es [weiter unten](https://github.com/ToolboxBodensee/toolbox-webseite/wiki/Grundlagen%3A-git-LFS).<br/>
Lektor ist auch als Python-Modul verfügbar und kann mit ``python2 -m lektor`` verwendet werden.
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