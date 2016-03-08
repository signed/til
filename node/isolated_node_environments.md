# isolated node environments

1. setup a [python virtualenv](../python/isolated_python_environments.md)
1. install [nodeenv](http://ekalinin.github.io/nodeenv/) within this environment

```bash
mkvirtualenv node_js
pip install nodeenv
sudo apt-get install libssl-dev
nodeenv --list
nodeenv --prebuilt -p --node=latest --npm=latest
```

This way the node installation is part of the python virtualenv and no separate activation of nodeenv is needed.
Just use `workon node_js` and `node` and `npm` are available