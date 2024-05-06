## Nmap
```
nmap 10.129.42.253
nmap -sV -sC -p- 10.129.42.253
```

###    Scripts
* locate scripts/citrix
* /usr/share/nmap/scripts/citrix-brute-xml.nse

###    Banner Grabbing
```
nc -nv 10.129.42.253 21
```

###    FTP
```
nmap -sC -sV -p21 10.129.42.253
```

###    SMB
```
nmap --script smb-os-discovery.nse -p445 10.10.10.40
nmap -A -p445 10.129.42.25
```

```
nmap -p- --min-rate 1000 -sV 10.129.128.223
nmap -sV -sC -A 10.129.42.253
```

### PORTS
```
nmap --min-rate 1000 10.10.10.40 | grep 'open' | awk '{ print $1 }' | awk '{print ($0+0)}' | sed -z 's/\n/,/g;s/,$/\n/'
```

### FTP
```
ftp -p 10.129.42.253
```

###SMB
```
    List
smbclient -N -L \\\\10.129.42.253
    Connect
smbclient \\\\10.129.42.253\\users
smbclient -U bob \\\\10.129.42.253\\users
```

https://www.samba.org/samba/docs/current/man-html/smbclient.1.html

### SNMP
```
snmpwalk -v 2c -c public 10.129.42.253 1.3.6.1.2.1.1.5.0
```
https://github.com/trailofbits/onesixtyone
```
onesixtyone -c dict.txt 10.129.42.254
```

### Readable Files
```
find . -perm -o=r -type d 2>/dev/null
```