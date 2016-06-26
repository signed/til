# isolated python environments

1. install [setuptools](https://pypi.python.org/pypi/setuptools)
1. install [pip](https://pip.pypa.io)
1. install [virtualenv](https://virtualenv.pypa.io/)
1. install [virtualenvwrapper](https://virtualenvwrapper.readthedocs.org/)

```bash
sudo apt-get install python-setuptools
sudo easy_install pip
sudo pip install --upgrade pip
sudo pip install virtualenv
sudo pip install virtualenvwrapper
```

in $HOME/.profile add
```
export WORKON_HOME=$HOME/.virtualenvs
. /usr/local/bin/virtualenvwrapper.sh
```

logout / login

```bash
mkvirtualenv my_cool_project
deactivate
workon my_cool_project
```
