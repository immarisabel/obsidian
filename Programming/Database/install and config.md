



57YOALHVB5HYP22K3D7E6U9MOR5SDEM2

```shell

sudo apt update

sudo apt install php-mbstring php-zip php-gd

wget https://files.phpmyadmin.net/phpMyAdmin/4.9.7/phpMyAdmin-4.9.7-all-languages.tar.gz

tar xvf phpMyAdmin-4.9.7-all-languages.tar.gz

sudo mv phpMyAdmin-4.9.7-all-languages/ /usr/share/phpmyadmin

sudo mkdir -p /var/lib/phpmyadmin/tmp

sudo chown -R www-data:www-data /var/lib/phpmyadmin

sudo nano /usr/share/phpmyadmin/config.inc.php

	$cfg['blowfish_secret'] = '57YOALHVB5HYP22K3D7E6U9MOR5SDEM2'; /* YOU MUST FILL IN THIS FOR COOKIE AUTH! */






```


https://www.digitalocean.com/community/tutorials/how-to-install-phpmyadmin-from-source-debian-10