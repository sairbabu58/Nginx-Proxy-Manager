## Configure Proxy host

```
- Existing URL for Pi-Hole > https://pihole.cloud-lab.j2ctechnologies.com/admin 192.168.0.117
- Existing URL for Proxmox > https://proxmox.cloud-lab.j2ctechnologies.com:8006 192.168.0.100
- Existing URL for WebServer > https://proxmox.cloud-lab.j2ctechnologies.com:8080 192.168.0.157

- Nginx proxy manager DNS name > http://proxy.cloud-lab.j2ctechnologies.com:81 192.168.0.150
```

```
- Login to proxy manager
- webUI > proxy.cloud-lab.j2ctechnologies.com:81
```
**Access: Proxmox**
```

- Dashboard > ProxyHost > Add proxy host > Details
    Domain Names: proxmox.loud-lab.j2ctechnologies.com
    Scheme: http/https [https] -> cause proxmon is running on https
    Forward HostName/IP: proxmox.cloud-lab.j2ctechnologies.com or 192.168.0.100
    Port: 8006    > cause proxmox is running on https
- Save
 
```

```
- try to access and test the connection without any port
- http://proxmox.cloud-lab.j2ctechnologies.com

```

**Access: WebServer**
```

- Dashboard > ProxyHost > Add proxy host > Details
    Domain Names: web.loud-lab.j2ctechnologies.com
    Scheme: http/https [http]
    Forward HostName/IP: web.cloud-lab.j2ctechnologies.com or 192.168.0.157
    Port: 8080    > cause proxmox is running on https
- Save
 
```

```
- try to access and test the connection without any port
- http://web.cloud-lab.j2ctechnologies.com

```

**Note:**

```
Add the DNS record and point all the url to proxy IP on PIHOLE Server
- web.cloud-lab.j2ctechnologies.com 192.168.0.150
- proxmon.cloud-lab.j2ctechnologies.com 192.168.0.150
Else, all the local entry on /etc/hosts on your machine, 
```
