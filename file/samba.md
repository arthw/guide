sudo apt update
sudo apt install samba
whereis samba

mkdir /home/<username>/sambashare/

sudo nano /etc/samba/smb.conf

[sambashare]
    comment = Samba on Ubuntu
    path = /home/username/sambashare
    read only = no
    browsable = yes
    
    
sudo service smbd restart

sudo ufw allow samba

sudo smbpasswd -a username


sudo adduser neo
sudo smbpasswd -a neo 
