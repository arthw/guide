### Set NFS Host
#### Install Tool
```
sudo apt update
sudo apt install nfs-kernel-server
```

#### Create Share Folder
```
mkdir /home/jianyuzh/share
```
#### Add Clients IP in Config

x.x.0.0 is clients IP mask

```
sudo vi /etc/exports
/home/jianyuzh/share x.x.0.0/16(rw,sync,fsid=0,crossmnt,no_subtree_check)
```

#### Restart NFS Server
```
sudo service nfs-server restart
```

### Set NFS Client

#### Install Tool

```
sudo apt update
sudo apt install nfs-common
```

#### Create Mount Point

```
mkdir /home/jianyuzh/share
```

#### Edit for Auto Mount

nfs-host.com is domain name or IP of NFS Host.

```
sudo vi /etc/fstab
nfs-host.com:/home/jianyuzh/share /home/jianyuzh/share    nfs     defaults        0       0
```
#### Enable Mount without Reboot
```
sudo mount -a
```
