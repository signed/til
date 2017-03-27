# Low-Level keybinding modifications

There are two separate keybindings.
The one active in an X-session and the on active in a tty.
This only covers changes in the X session.

## List the current keybindings

````shell
xmodmap -pke  # list the current keybindings
````

## Interactivly discover keysym use xev
````shell
xev 
````

## Override mappings

Use the lines from the output from `xmodmap -pke` and make the canges needed.
Create ~/.Xmodmap file to hold the keybinding changes needed.

Add the following to ~/.profile to ensure the changes are loaded.
You could use .xsession for this, but sddm does not source it in the version currently used in Kubuntu 16.04 [1][1]

````
. xmodmap ~/.Xmodmap

````


[1]: https://github.com/sddm/sddm/issues/647
