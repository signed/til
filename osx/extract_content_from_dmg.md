# How to extract the content of a dmg file without installing it

````
7z x jdk-8u40-macosx-x64.dmg
pkgutil --expand JDK\ 8\ Update\ 40/JDK\ 8\ Update\ 40.pkg expanded
cat expanded/jdk18040.pkg/Payload | cpio -zi
cp -r  Contents/Home/ ~/apps/java/jdk8u40
````
