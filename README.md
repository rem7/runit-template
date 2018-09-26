# runit-template
runit template

#### Create a user
```
sudo groupadd webapp
sudo useradd -g webapp -d /var/go -s /bin/bash go
sudo mkdir /var/go
sudo chown go:webapp /var/go
```

#### Log
Make sure to create the directory for logs and set the owner right
Next copy the log/config file to that dir ie. /var/log/myapp/config

#### Increasing system limits for open files

update to have `/etc/security/limits.conf`
```conf
* soft nofile 65000
* hard nofile 65000
```

documentation at:
http://smarden.org/runit/index.html
