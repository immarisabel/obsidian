# install
https://orcacore.com/install-configure-jenkins-almalinux-9/
first java! 11  or 17

```

sudo wget -O /etc/yum.repos.d/jenkins.repo \ https://pkg.jenkins.io/redhat/jenkins.repo

sudo dnf update -y

sudo dnf install jenkins -y

sudo systemctl enable jenkins

sudo systemctl start jenkins

sudo systemctl status jenkins

sudo cat /var/lib/jenkins/secrets/initialAdminPassword


```

open ports [[commands]]
# Jenkins Notes


### access admin first time
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

```

```
unitoken-admin
11333f3217c355f1b52553c859ce4b243e
S3hOK4nxyeZ5cwR
```
