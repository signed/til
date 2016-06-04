# Setup  docker toolbox on osx

```
# Install Homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
# Install Cask
brew install caskroom/cask/brew-cask
# Install docker toolbox
brew cask install dockertoolbox

# create the docker machine
docker-machine create --driver "virtualbox" docker-vm

# start the docker machine
docker-machine start docker-vm

# this command allows the docker commands to be used in the terminal
eval "$(docker-machine env docker-vm)"

# at this point can run any "docker" or "docker-compose" commands you want
docker run hello-world
```
