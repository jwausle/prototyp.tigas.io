# Prototyp.tigas.io

Docker-compose prototyp for tigas.io. 

## Getting started

* clone repo
* start ubuntu vm with vagrant 
* start tigas.io within ubuntu vm

> require vagrant >=2.2.2

> require virtualbox >=6.0

```
git clone https://github.com/jwausle/prototyp.tigas.io.git
cd prototyp.tigas.io/vagrant
vagrant up 
# must success

vagrant ssh 
vagrant@ubuntu-bionic:~$ cd /usr/share/tigas.io
vagrant@ubuntu-bionic:/usr/share/tigas.io $ docker-compose up
# must succes
```

* update `/etc/hosts` on host 

```
echo "[LOCAL_VM_IP] tigas.io" >> /etc/hosts
echo "[LOCAL_VM_IP] sstit.tigas.io" >> /etc/hosts
```

* open [grafana](http://sstit.tigas.io/g) 
* open [traefik](http://tigas.io:8080) 

## Deploy

> require docker>=18.06

> require docker-compose>=1.17 

```
git clone https://github.com/jwausle/prototyp.tigas.io.git
scp -r prototyp.tigas.io user@prod
ssh user@prod
user@prod:~$ cd prototyp.tigas.io
user@prod:prototyp.tigas.io$ docker-compose up
```