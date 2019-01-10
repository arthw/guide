# You will see a gray window in VNC viewer and there is no terminal and window-manager.

# Method
Install gnome GUI tools:
```
sudo apt-get install gnome-panel gnome-settings-daemon metacity nautilus gnome-terminal
```

Edit the configure file under your home folder:
```
vi .vnc/xstartup
```

Copy following content to the file above:
```
#!/bin/sh

#Uncomment the following two lines for normal desktop:
#unset SESSION_MANAGER
#exec /etc/X11/xinit/xinitrc

[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
xsetroot -solid grey
vncconfig -iconic &
x-terminal-emulator -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop" &
x-window-manager &
gnome-panel &
gnome-settings-daemon &
metacity &
nautilus &
```
