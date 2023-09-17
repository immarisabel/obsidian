https://www.server-world.info/en/note?os=AlmaLinux_9&p=httpd2&f=1

1 port:
```
sudo nano /etc/httpd/conf.d/revers_proxy.conf


<IfModule mod_proxy.c>
    ProxyRequests Off
    <Proxy *>
        Require all granted
    </Proxy>
    # backend server and forwarded path
    ProxyPass / http://vm.marisabel.nl:8091/
    ProxyPassReverse / http://vm.marisabel.nl:8091/
</IfModule> 

reload httpd
```
