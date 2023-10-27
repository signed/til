# convert mov to animated gif

```shell
brew install imagemagick ffmpeg
mkdir frames
ffmpeg -i cast.mov -r 1 frames/image.%05d.png
convert frames/image.*.png cast.gif
```
