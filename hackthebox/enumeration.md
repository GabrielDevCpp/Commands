# Gobuster
```
gobuster dir -u http://10.10.10.121/ -w /usr/share/dirb/wordlists/common.txt
gobuster dns -d inlanefreight.com -w /usr/share/SecLists/Discovery/DNS/namelist.txt
```
Status Code
* https://en.wikipedia.org/wiki/List_of_HTTP_status_codes
SecList
* https://github.com/danielmiessler/SecLists
Install SecList
```
git clone https://github.com/danielmiessler/SecLists
sudo apt install seclists -y
gobuster dns -d inlanefreight.com -w /usr/share/SecLists/Discovery/DNS/namelist.txt
```
Banner Grabbing/Web Server Headers
```
curl -IL https://www.inlanefreight.com
```
WyeWitness
* https://github.com/FortyNorthSecurity/EyeWitness
Whatweb
```
whatweb 10.10.10.121
```

## Certificates


Robots.txt

* Ctrl+U

Generate Wordlist
https://github.com/digininja/CeWL
