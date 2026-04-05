## Configure Proxy host

```
-> Existing URL for Pi-Hole > https://pihole.cloud-lab.j2ctechnologies.inter/admin 192.168.0.117
-> Nginx proxy manager DNS name > http://proxy.cloud-lab.j2ctechnologies.inter:81 192.168.0.150
```

```
-> Login to proxy manager
-> webUI > proxy.cloud-lab.j2ctechnologies.inte:81
-> Dashboard > ProxyHost > Add proxy host > Details
    Domain Names: <proxy-host DNS> proxy.cloud-lab.j2ctechnologies.inter
    Scheme: http/https [https] -> cause pihole is running on https
    Forward HostName/IP: pihole.cloud-lab.j2ctechnologies.inter/192.168.0.117
    Port: 443    > cause pihole is running on https
-> Save
 
```

```
-> try to access and test the connection
-> http://proxy.cloud-lab.j2ctechnologies.inter/admin

```
