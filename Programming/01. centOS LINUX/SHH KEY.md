## SHH Installation:

`ssh {REMOTE_HOST}`

Create the .ssh directory:
`mkdir ~/.ssh`

Set the right permissions:
`chmod 700 ~/.ssh`

Create the authorized_keys file:
`touch ~/.ssh/authorized_keys`

Set the right permissions:
`chmod 600 ~/.ssh/authorized_keys`

### WINDOWS:
`ssh-keygen -t rsa`
`type $env:USERPROFILE\.ssh\id_rsa.pub | ssh {REMOTE_HOST} "cat >> .ssh/authorized_keys"`

### Password disable:
`sudo nano /etc/ssh/sshd_config`
`sudo service sshd restart`