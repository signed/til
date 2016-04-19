# Execute module scripts

Some npm modules (e.g. typscript) install scripts (e.g. tsc) that can be used in the scripts part of `package.json`.
You can invoke them on the command line like this:

```
PATH=$(npm bin):$PATH tsc --help
``` 

Bundle this in an alias like `npm-exec` and any script can be ececuted like `npm-exec tsc --help`:
```
alias npm-exec='PATH=$(npm bin):$PATH'
```

[stackoverflow](http://stackoverflow.com/a/15157360)
