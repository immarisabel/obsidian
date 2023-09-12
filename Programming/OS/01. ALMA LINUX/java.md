
https://www.howtoforge.com/how-to-install-java-openjdk-oraclejdk-on-almalinux-9/
https://orcacore.com/install-openjdk-17-almalinux-9/

```
sudo dnf install java-17-openjdk java-17-openjdk-devel
```

### Installing Java Oracle JDK 17

Run the curl command below to download the RPM package of Java Oracle JDK 17.
```
curl -qO https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.rpm
```

Once the download process is finished, install the RPM file of Java Oracle JDK 17 using the following command.

```
sudo rpm -ivh jdk-17_linux-x64_bin.rpm
```
## Configuring JAVA_HOME Environment Variable

When you expect to use third applications such as Apache Tomcat and Gradle, then you must configure the default JAVA_HOME environment variable on your AlmaLinux server.

You can set up the JAVA_HOME environment variable as a system-wide or per-user configuration.

### Setup JAVA_HOME System-wide

To use JAVA_HOME system-wide, you can utilize the bash profile configuration on the /etc/profile.d/ directory, which will be loaded automatically at login.

Create a new script /etc/profile.d/java.sh using the nano editor command below.
```
sudo nano /etc/profile.d/java.sh
```


Insert the following configuration. In this example, we'll set up JAVA_HOME with Java OpenJDK 17.

```
JAVA_HOME="/usr/lib/jvm/java-17-openjdk"

```


Save and exit the editor when you're finished.

Now run the following command to make the script /etc/profile.d/java.sh executable and load it to your current session.
```
sudo chmod +x /etc/profile.d/java.sh  
source /etc/profile.d/java.sh
```


Verify the JAVA_HOME environment variable using the following command. If the operation was successful, you should see the JAVA_HOME environment variables pointed to your default OpenJDK directory.
```
echo $JAVA_HOME
```
### Setup JAVA_HOME Per-user

If you want to set up JAVA_HOME as per-user, you can utilize the ~/.bashrc script that will be loaded automatically upon login.

Log in to your user using the following command.

su - username

Edit the ~/.bashrc file using the nano editor command below.

nano ~/.bashrc

Add the following configuration to the bottom of the line.

JAVA_HOME="/usr/lib/jvm/java-17-openjdk"

Save the changes and exit the editor when finished.

Now reload the ~/.bashrc to apply the changes, then verify the JAVA_HOME environment variable using the command below.

source ~/.bashrc  
echo $JAVA_HOME

# java
https://www.howtoforge.com/how-to-install-java-openjdk-oraclejdk-on-almalinux-9/
https://orcacore.com/install-openjdk-17-almalinux-9/

```
sudo dnf install java-17-openjdk java-17-openjdk-devel
```

### Installing Java Oracle JDK 17

Run the curl command below to download the RPM package of Java Oracle JDK 17.
```
curl -qO https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.rpm
```

Once the download process is finished, install the RPM file of Java Oracle JDK 17 using the following command.

```
sudo rpm -ivh jdk-17_linux-x64_bin.rpm
```
## Configuring JAVA_HOME Environment Variable

When you expect to use third applications such as Apache Tomcat and Gradle, then you must configure the default JAVA_HOME environment variable on your AlmaLinux server.

You can set up the JAVA_HOME environment variable as a system-wide or per-user configuration.

### Setup JAVA_HOME System-wide

To use JAVA_HOME system-wide, you can utilize the bash profile configuration on the /etc/profile.d/ directory, which will be loaded automatically at login.

Create a new script /etc/profile.d/java.sh using the nano editor command below.
```
sudo nano /etc/profile.d/java.sh
```


Insert the following configuration. In this example, we'll set up JAVA_HOME with Java OpenJDK 17.

```
JAVA_HOME="/usr/lib/jvm/java-17-openjdk"

```


Save and exit the editor when you're finished.

Now run the following command to make the script /etc/profile.d/java.sh executable and load it to your current session.
```
sudo chmod +x /etc/profile.d/java.sh  
source /etc/profile.d/java.sh
```


Verify the JAVA_HOME environment variable using the following command. If the operation was successful, you should see the JAVA_HOME environment variables pointed to your default OpenJDK directory.
```
echo $JAVA_HOME
```
### Setup JAVA_HOME Per-user

If you want to set up JAVA_HOME as per-user, you can utilize the ~/.bashrc script that will be loaded automatically upon login.

Log in to your user using the following command.

su - username

Edit the ~/.bashrc file using the nano editor command below.

nano ~/.bashrc

Add the following configuration to the bottom of the line.

JAVA_HOME="/usr/lib/jvm/java-17-openjdk"

Save the changes and exit the editor when finished.

Now reload the ~/.bashrc to apply the changes, then verify the JAVA_HOME environment variable using the command below.

source ~/.bashrc  
echo $JAVA_HOME