Install lxde:

```sudo apt-get install xorg lxde-core```

Install vncserver:

```sudo apt-get install tightvncserver```

Set password:

```vncpasswd```

Start up to create config file:

```vncserver```

Edit config file

```vi ~/.vnc/xstartup```

Add:

```
lxterminal &
/usr/bin/lxsession -s LXDE &
```

Reboot:

```sudo reboot```

Start up:

```vncserver```
