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
