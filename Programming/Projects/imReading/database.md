
**Version**: **mysql  Ver 15.1** Distrib **10.11.3-MariaDB**, for debian-linux-gnu (x86_64) 

## Configuration

### app properties

```properties
  
#persist the data  
spring.datasource.url=jdbc:h2:file:./data/books  
  
spring.datasource.driverClassName=org.h2.Driver  
spring.datasource.username=mari  
spring.datasource.password=unicorn  
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect  
spring.jpa.hibernate.ddl-auto=update  
spring.h2.console.enabled=true  
spring.jpa.show-sql=true  
spring.main.allow-bean-definition-overriding=true  
hibernate.enable_lazy_load_no_trans = true  
  
```

## COMMANDS
```shell
To use:

mysql db_name

mysql --user=user_name --password=your_password db_name


Columns:

 --column-names

    Write column names in results.

--column-type-info, -m

    Display result set metadata.

Database:

--connect-timeout=seconds

     Set the number of seconds before connection
           timeout. (Default value is 0.)

--database=db_name, -D db_name

     The database to use.

 --debug-info, -T

     Prints debugging information and memory and CPU usage statistics when the program exits.

--default-auth=name

    Default authentication client-side plugin to use.

--init-command=str

    
    SQL Command to execute when connecting to the MariaDB server. Will automatically be re-executed when reconnecting.

•   --password[=password], -p[password]

           The password to use when connecting to the server. If you use the short option form
           (-p), you cannot have a space between the option and the password. If you omit the password value following the --password or -p option on the command line, mysql prompts for one.
		Specifying a password on the command line should be considered insecure. You can use an option file to avoid giving the password  on the command line.

--port=port_num, -P port_num

           The TCP/IP port number to use for the
           connection or 0 for default to, in order of
           preference, my.cnf, $MYSQL_TCP_PORT,
           /etc/services, built-in default (3306).
           Forces --protocol=tcp when specified on the
           command line without other connection
           properties.


 --table, -t

    
    
    Display output in table format. This is the default for interactive use, but can be used to produce table output in batch mod

  --user=user_name, -u user_name

     The MariaDB user name to use when connecting to the server.

 --version, -V



```
MYSQL COMMANDS
       mysql sends each SQL statement that you issue to
       the server to be executed. There is also a set
       of commands that mysql itself interprets. For a
       list of these commands, type help or \h at the
       mysql> prompt:
```shell
           mysql> help
           List of all MySQL commands:
           Note that all text commands must be first on line and end with ´;´
           ?         (\?) Synonym for `help´.
           clear     (\c) Clear command.
           connect   (\r) Reconnect to the server. Optional arguments are db and host.
           delimiter (\d) Set statement delimiter.
           edit      (\e) Edit command with $EDITOR.
           ego       (\G) Send command to mysql server, display result vertically.
           exit      (\q) Exit mysql. Same as quit.
           go        (\g) Send command to mysql server.
           help      (\h) Display this help.
           nopager   (\n) Disable pager, print to stdout.
           notee     (\t) Don´t write into outfile.
           pager     (\P) Set PAGER [to_pager]. Print the query results via PAGER.
           print     (\p) Print current command.
           prompt    (\R) Change your mysql prompt.
           quit      (\q) Quit mysql.
           rehash    (\#) Rebuild completion hash.
           source    (\.) Execute an SQL script file. Takes a file name as an argument.
           status    (\s) Get status information from the server.
           system    (\!) Execute a system shell command.
           tee       (\T) Set outfile [to_outfile]. Append everything into given
                          outfile.
           use       (\u) Use another database. Takes database name as argument.
           charset   (\C) Switch to another charset. Might be needed for processing
                          binlog with multi-byte charsets.
           warnings  (\W) Show warnings after every statement.
           nowarning (\w) Don´t show warnings after every statement.
           For server side help, type ´help contents´

```
