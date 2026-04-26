# [apt vs apt-get](https://linuxize.com/post/apt-vs-apt-get/)

The table below maps the most common `apt` commands to their `apt-get` or `apt-cache` equivalents:

|Task|apt|apt-get / apt-cache|
|---|---|---|
|Update package index|`apt update`|`apt-get update`|
|Upgrade all packages|`apt upgrade`|`apt-get upgrade`|
|Full upgrade (may remove packages)|`apt full-upgrade`|`apt-get dist-upgrade`|
|Install a package|`apt install pkg`|`apt-get install pkg`|
|Remove a package|`apt remove pkg`|`apt-get remove pkg`|
|Remove with config files|`apt purge pkg`|`apt-get purge pkg`|
|Remove unused dependencies|`apt autoremove`|`apt-get autoremove`|
|Search for a package|`apt search keyword`|`apt-cache search keyword`|
|Show package details|`apt show pkg`|`apt-cache show pkg`|
|List installed packages|`apt list --installed`|`dpkg --list`|
|List upgradable packages|`apt list --upgradable`|(no direct equivalent)|
|Edit sources list|`apt edit-sources`|(manual file editing)|

As you can see, `apt` merges `apt-get` and `apt-cache` into one tool and adds a few convenience commands like `apt list` and `apt edit-sources` that have no direct `apt-get` equivalent.