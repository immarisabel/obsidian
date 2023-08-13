# network config
` sudo vi /etc/sysconfig/network-scripts/ifcfg-enp0s3`

### Original:

```shell
TYPE=Ethernet 
PROXY_METHOD=none 
BROWSER_ONLY=no 
BOOTPROTO=dhcp 
DEFROUTE=yes 
IPV4_FAILURE_FATAL=no 
IPV6INIT=yes 
IPV6_AUTOCONF=yes 
IPV6_DEFROUTE=yes 
IPV6_FAILURE_FATAL=no 
IPV6_ADDR_GEN_MODE=stable-privacy 
NAME=enp0s3 
UUID=cc0d52b4-a991-4d1e-86e3-565058c35357 
DEVICE=enp0s3 
ONBOOT=yes HWADDR=08:00:27:3C:2F:66 
IPV6_PRIVACY=no
```

### WORKING MODIFIED
```shell

TYPE=Ethernet
PROXY_METHOD=none
BROWSER_ONLY=no
BOOTPROTO=none
DEFROUTE=yes
IPV4_FAILURE_FATAL=no
IPV6INIT=yes
IPV6_AUTOCONF=yes
IPV6_DEFROUTE=yes
IPV6_FAILURE_FATAL=no
IPV6_ADDR_GEN_MODE=stable-privacy
NAME=enp0s3
UUID=cc0d52b4-a991-4d1e-86e3-565058c35357
DEVICE=enp0s3
ONBOOT=yes
HWADDR=08:00:27:3C:2F:66
IPV6_PRIVACY=no


IPADDR=192.168.2.8
NETMASK=255.255.255.0
GATTEWAY=192.168.2.254
DNS1=8.8.8.8
DNS2=8.8.4.4

```

# troubleshooting
LINUX `ip a`
WINDOWS `ip config`

-----
## tags

#network #linux #ip #config

