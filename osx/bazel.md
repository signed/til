# Installing bazel on mac

Commands are from [here](https://kythe.io/getting-started-macos/)

```shell
xcode-select -p
```

If this prints `/Library/Developer/CommandLineTools` you have to install xcode and run

```shell
sudo xcode-select -s /Applications/Xcode.app/Contents/Developer
```

```shell
brew tap bazelbuild/tap
brew install bazelbuild/tap/bazel
```


sudo xcode-select -s /Users/wischan/Applications/Xcode.app/Contents/Developer
