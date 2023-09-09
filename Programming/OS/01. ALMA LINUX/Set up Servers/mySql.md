```shell

# login
mysql -u root -p

#create database
create database NAME;

#see databases
show database;
status


#remote access
 GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'password' WITH GRANT OPTION;



/etc/logrotate.d/mysqld
```