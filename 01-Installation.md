## How to install Nginx Proxy Manager

```
$ yum -y install eple-release
$ yum -y install podman
$ yum -y install podman-compose

```

```
https://nginxproxymanager.com/guide/

https://nginxproxymanager.com/setup/

```
$ mkdir compose ; cd compose
$ vi container-compose.yml
$ podman-compose up  -d

```
-> Login to proxy manager
-> https://<ip-hostname>:81

```
