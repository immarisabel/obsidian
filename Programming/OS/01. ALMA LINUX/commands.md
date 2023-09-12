## networks
```
ip a

sudo systemctl restart network

```

## open ports to the world:

```
netstat -na | grep XXXX # check status

lsof -i -P |grep http

firewall-cmd --get-active-zones

firewall-cmd --zone=public --add-port=XXXX/tcp --permanent

firewall-cmd --reload

```




UUIDs : 
```
nmcli connection show
```

## copy web files

```
sudo mkdir /var/www/html/....

sudo scp <local_file_path> <username>@<server_ip_or_hostname>:<remote_directory>

scp C:\Users\Administrator\Documents\Programming\WEBSITE\vm-site\index.html root@vm.marisabel.nl:/var/www/html/index.html
```


### Find 

apps
```
rpm -qa | grep '^a'
```

anything anywhere
```
find /path  -type f -exec grep -l 'string' {} +
```

https://dade2.net/kb/how-install-phpmyadmin-on-almalinux-8/
---
## tags

#commands #linux 
