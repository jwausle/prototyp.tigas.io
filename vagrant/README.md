# Boot ubuntu docker host from scratch

* require vagrant >=2.2.2
* require virtualbox >=6.0

## Run vagrant first time

```
vagrant up

... take while donwload + provision ubuntu+docker/docker-compose
# - with 4GB RAM
# - get a 172.x.y.z external local IP address
# - mount /vagrant/ and /vagrant_data folder from host
# dockerd is up and running with privelleges for vagrant user.
```

## Use vagrant

```
vagant ssh
vagrant@ubuntu-bionic:~$ docker ps
... must success

vagrant@ubuntu-bionic:~$ cd /usr/share/tigas.io
vagrant@ubuntu-bionic:/usr/share/tigas.io $ docker-compose up
... must success
```
