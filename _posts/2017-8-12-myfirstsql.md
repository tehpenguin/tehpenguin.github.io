---
layout: post
title: Pico CTF 2017 My First SQL
category: ctf
---
<b>Category: Web Exploitation</b>

  
My First SQL

<i>I really need access to website, but I forgot my password and there is no reset. Can you help?
HINTS
Have you heard about SQL injection?</i>

This is an obvious SQL injection challenge. The goal on this challange is to pass the following string to the SQL database in order to retrieve any credentials. 

SELECT * FROM Users WHERE Username='$username' AND Password='$password'

The query here returns a value (or a set of values) because the condition is always true (OR 1=1). In this way the system has authenticated the user without knowing the username and password. There is a problem that arises in which we have to close the parantheses in order to close the comment and get a correct query. This consists of adding a number of closing parentheses until we obtain a corrected query

$username = 1' or '1' = '1

$password = 1' or '1' = '1

![Image description](/images/myfirstsql.png)


![Image description](/images/myfirstsql2.png)
