# X keyboard bindings

XKB versus xmodset

## Terms
1. scancode lowest identification umber for a key, it is the value that a keyboard sends to a computer
1. keycode 2nd level of identification corresponding to a function
1. keysym 3rd level of identification corresponding to a symbol. May depend on whether a modifier key was also pressed


## Tools
* showkey   has to be run in a tty, shows scancodes, keycode and keysm if a key gets pressed
* evtest    Seems to be required in some cases if working with USB keyboards
* xev       keycodes are different in x; use xev to get them
* xmodmap   commandline tool to list/manipulate the current keybindings
* xkeycaps  graphical frontent to xmodmap

## xmodmap
xmodmap -pke print the current keymap table fromatted into expressions


## Links
* https://wiki.archlinux.org/index.php/Extra_keyboard_keys#In_Xorg
* http://www.in-ulm.de/~mascheck/X11/xmodmap.html
* https://blacketernal.wordpress.com/set-up-key-mappings-with-xmodmap/
* https://offend.me.uk/blog/14/
***** https://superuser.com/questions/819414/order-of-keysym-in-xmodmap-config-file/823923
***** https://forum.xfce.org/viewtopic.php?id=10094
***** https://unix.stackexchange.com/a/326263
***** https://unix.stackexchange.com/questions/249122/why-do-my-xmodmap-binds-involving-altgr-only-work-on-some-keys/313711#313711
***** https://wiki.ubuntuusers.de/Xmodmap/
***** https://askubuntu.com/questions/5095/typing-using-key-combinations

Mode_switch= pre XKB name fo AltGr (https://unix.stackexchange.com/questions/55076/what-is-the-mode-switch-modifier-for)
