source /etc/network/interfaces.d/*
sudo nano source /etc/network/interfaces

static : enp0s8  XXX.XXX.XX.XXX/24
local inet: enp0s3




/etc/network/interfaces.d/CONFIGFILE
# DHCP
sudo nano enp0s3.conf
```shell
iface enp0s3 inet dhcp

```
# STATIC IP
sudo nano enp0s8.conf
```shell

iface enp0s8 inet static
     address 192.168.56.103/24
     gateway 192.168.2.254
     
```
 secondary?  192.168.56.104
 sudo systemctl restart networking

? 10.0.02.15

 sudo nano /etc/network/interfaces
```shell

  GNU nano 7.2     /etc/network/interfaces               # This file describes the network interfaces available o># and how to activate them. For more information, see in>

source /etc/network/interfaces.d/*

# The loopback network interface
auto lo
iface lo inet loopback


# The primary network interface
allow-hotplug enp0s8
iface enp0s8 inet dhcp

# The secondary network interface
allow-hotplug enp0s3
iface enp0s3 inet dhcp




```

