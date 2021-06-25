### Set automatic startup VNC sessoin :1
```
sudo vi /etc/init.d/vnc


#!/bin/sh
### BEGIN INIT INFO
# Provides: tightvncserver
# Required-Start: $syslog $remote_fs $network
# Required-Stop: $syslog $remote_fs $network
# Default-Start: 2 3 4 5
# Default-Stop: 0 1 6
# Short-Description: Starts VNC Server on system start.
# Description: Starts tight VNC Server. Script written by James Swineson.
### END INIT INFO

export USER='xxx'  
 
eval cd ~$USER
 
case "$1" in
  start)
    su $USER -c '/usr/bin/vncserver -geometry 1680x900 :1'
    
    echo "Starting TightVNC server for $USER "
    ;;
  stop)
    su $USER -c '/usr/bin/vncserver -kill :1'
    echo "Tightvncserver stopped"
    ;;
  *)
    echo "Usage: /etc/init.d/vnc {start|stop}"
    exit 1
    ;;
esac
exit 0
```

Or, replace the cmd by:
`/usr/bin/vncserver -localhost no -geometry 1680x900 :1`

### Enable auto startup
```
sudo chmod 755 /etc/init.d/vnc
sudo update-rc.d vnc defaults
```

### Reboot to test

`sudo reboot`
