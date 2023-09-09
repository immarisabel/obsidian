https://dade2.net/kb/how-to-install-apache-mysql-and-php-on-almalinux-8/

https://www.redhat.com/sysadmin/install-apache-web-server

```shell
$ sudo dnf install httpd
```

Using your text editor of choice (mine is [Vim](https://www.redhat.com/sysadmin/four-things-vim), but [Nano](https://www.redhat.com/sysadmin/four-things-nano) or others work just as well), open `/etc/httpd/conf/httpd.conf`

These two values may already be set in that file, but confirm them to be sure:

```plaintext
DocumentRoot /var/www/html
Listen 80
```

```shell
$ sudo systemctl start httpd 
$ sudo systemctl status httpd

$ sudo systemctl enable --now httpd

```

## Open port 80

```shell
$ sudo firewall-cmd --permanent --zone=public --add-service=http 
$ sudo firewall-cmd --reload 
$ sudo firewall-cmd --list-all --zone=public
```

### Later to look for:

```shell
[mari@vm ~]$ sudo firewall-cmd --list-all --zone=public
public (active)
  target: default
  icmp-block-inversion: no
  interfaces: enp0s3
  sources:
  services: dhcpv6-client http ssh
  ports:
  protocols:
  masquerade: no
  forward-ports:
  source-ports:
  icmp-blocks:
  rich rules:
```
#TODO

# LOGS

`$ sudo cat /var/log/httpd/access_log | grep -I download-this.txt`

---
## tags

#linux  #server #config #commands 
