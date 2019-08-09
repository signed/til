# How to split a large binary files into multiple parts
````shell
split --bytes=2000m --numeric-suffixes --numeric-suffix-length=3 file.xip
cat file.xip.000 file.xip.001 file.xip.003 > file.xip
pkgutil --check-signature file.xip
xip -x file.xip
````
