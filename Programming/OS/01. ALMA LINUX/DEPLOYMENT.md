## jenkins
https://orcacore.com/install-configure-jenkins-almalinux-9/
https://www.digitalocean.com/community/tutorials/opening-a-port-on-linux
## references

https://www.linode.com/docs/guides/how-to-deploy-spring-boot-applications-nginx-ubuntu-22-04/
https://www.baeldung.com/executable-jar-with-maven
https://www.learnbestcoding.com/post/37/deploy-springboot-app-linux
https://docs.spring.io/spring-boot/docs/current/reference/html/deployment.html#deployment.installing.nix-services
https://youtu.be/6okiy2Upx_k?si=72KRfiH1Ukpiix9u
## maven

```

<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-dependency-plugin</artifactId>
    <executions>
        <execution>
            <id>copy-dependencies</id>
            <phase>prepare-package</phase>
            <goals>
                <goal>copy-dependencies</goal>
            </goals>
            <configuration>
                <outputDirectory>
                    ${project.build.directory}/libs
                </outputDirectory>
            </configuration>
        </execution>
    </executions>
</plugin>

```

## linux

path for jar : /usr/share/java/


![[springboot.service]]

```
sudo ln -s  /usr/share/javasystemctl daemon-reload/springboot.jar /etc/init.d/springboot
```

make sub-server in webmin
upload jar to home

then

configure:
https://www.baeldung.com/spring-boot-app-as-a-service

` /etc/systemd/system/myapp.service 
```

[Unit] 
Description=A Spring Boot application 
After=syslog.target 

[Service] 
User=OWNER 
ExecStart=/path/to/your-app.jar SuccessExitStatus=143 

[Install] WantedBy=multi-user.target

```

```
sudo chown root:root /home/vm/public_html/demo/0/demo.jar
sudo chmod 500 /home/vm/public_html/demo/0/demo.jar
sudo chown root:root /home/vm/public_html/demo/1/demo.jar
sudo chmod 500 /home/vm/public_html/demo/1/demo.jar
sudo chown root:root /home/vm/public_html/demo/2/demo.jar
sudo chmod 500 /home/vm/public_html/demo/2/demo.jar
sudo chown root:root /home/vm/public_html/demo/3/demo.jar
sudo chmod 500 /home/vm/public_html/demo/3/demo.jar



 sudo ln -s /home/vm/public_html/demo/0/demo.jar /etc/init.d/demo1
 sudo ln -s /home/vm/public_html/demo/1/demo.jar /etc/init.d/demo2
 sudo ln -s /home/vm/public_html/demo/2/demo.jar /etc/init.d/demo3
 sudo ln -s /home/vm/public_html/demo/3/demo.jar /etc/init.d/demo4


sudo service demo1 start
sudo service demo2 start
sudo service demo3 start
sudo service demo4 start

```
redirect:
```shell
iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-ports 8080
```

to auto start

```

sudo systemctl enable demo1
sudo systemctl start demo1
sudo systemctl status demo1

sudo systemctl enable demo2
sudo systemctl start demo2
sudo systemctl status demo2
sudo systemctl enable demo3
sudo systemctl start demo3
sudo systemctl status demo3
sudo systemctl enable demo4
sudo systemctl start demo4
sudo systemctl status demo4

sudo service demo1

# Fail?

ls -l /path/to/myapp.jar 

# red?
chmod +x /path/to/myapp.jar 
ls -l /path/to/myapp.jar 

#green?

sudo systemctl daemon-reload

sudo systemctl enable myapp
sudo systemctl start myapp
sudo systemctl status myapp

```



# external config file
https://www.baeldung.com/spring-properties-file-outside-jar
## 2. Using the Default Location[](https://www.baeldung.com/spring-properties-file-outside-jar#app-properties)

By convention, Spring Boot looks for an externalized configuration file — _application.properties_ or _application.yml_ — in four predetermined locations in the following order of precedence:

- A _/config_ subdirectory of the current directory
- The current directory
- A classpath _/config_ package
- The classpath root

Therefore, **a property defined in _application.properties_ and placed in the _/config_ subdirectory of the current directory will be loaded.** This will also override properties in other locations in case of a collision.


