# How to upgrade to latest bash version

I extracted the steps from [here](http://clubmate.fi/upgrade-to-bash-4-in-mac-os-x/)

````
brew update && brew install bash
sudo bash -c 'echo /usr/local/bin/bash >> /etc/shells'
chsh -s /usr/local/bin/bash
````
