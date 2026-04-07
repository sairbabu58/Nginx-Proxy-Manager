## Redirection Host from OLD-URL to New-URl

Note:
- My appplication is lets say running on old-j2ctechnologies.com
- Old url got changed and new URL is new-j2ctechnologies.com
- If some will hit still to the old URL it will redirect to new URL 

  ```
-> old domain docker app running on http://old.j2ctechnologies.com:8082 (same host or diff host)
-> new domain docker app running on http://new.j2ctechnologies.com:8083 (same host or diff host)
  ```

```
-> add the pihole dns name and ip (proxy IP)
-> proxy-Manager
-> you can add old to old and new to new for testing.
-> access old URL and validate the output [i am from old domain]
-> Access new url and validate the output  [i am from new domain]
```

```
-> Configure redirection Host

-> ProxyManager webUI
-> Hosts > New Redirection Host
  Domainname: old.j2ctechnologies.com
  Sceme: http
  Forward Domain: new.j2ctechnologies.com
Http Code: 301 Moved permanently 
```
