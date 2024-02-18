# whonix-script
Simple script to build whonix on a mac with apple silicon

## how to install and use this

First install a debian 12 wm on your system, make sure you make a user with sudo privileges with no password needed. Then add the gpg keys from whonix manually as described in their websites. No need to install any dependencies or anything else. But i do recommend to download and use tmux or screen in while running the script. Specially if you run this on ssh as then you do not loose all your build progress.

You can either add this script by running it manually, add it to your bashrc or even just put it in /usr/bin. Whatever fits you best. Do please read the script before running it.

## how to run the script

Call on the script with the tag you want to build as a argument. Example like this:

```
$ whonix 17.1.1.8-developers-only
```

## questions?
if you got any do please contact me or make a issue if you find any bugs or want something special out of this.
