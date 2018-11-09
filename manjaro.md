# Updating
``` bash
pacman -Syu
```

# Macify
```bash 
setxkbmap -option 'altwin:ctrl_win'
```

In Keyboard settings preferences remove anything point to SUPER

```bash
sudo vim /etc/X11/xorg.conf.d/00-keyboard.conf
```


```
Section "InputClass"
Identifier "system-keyboard"
MatchIsKeyboard "on"
Option "XkbLayout" "us"
Option "XKbOptions" "altwin:ctrl_win"
EndSection
```
