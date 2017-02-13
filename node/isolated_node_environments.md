# isolated node environments

# nvm
## install
1.
```bash
export NVM_DIR="$HOME/.nvm" && (
  git clone https://github.com/creationix/nvm.git "$NVM_DIR"
  cd "$NVM_DIR"
  git checkout -b current `git describe --abbrev=0 --tags --match "v[0-9]*" origin`
) && . "$NVM_DIR/nvm.sh"
```
1. Initialize nvm when the shell is started `~/.profile`
```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
[[ -r $NVM_DIR/bash_completion ]] && . $NVM_DIR/bash_completion
```
1. `nvm list-remote` shows the available node versions
1. `nvm install node 7.5.0` installs node in version 7.5.0, latest is installed if no version is provided
## use in a project
1. In project directory run `echo 7.5.0 > .nvmrc`
1. Run `nvm use` to switch from the default version to the project specific node version.

# nodeenv
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
