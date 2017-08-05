---
layout: post
title: Testing Open Ports with Python
category: tutorials
---

This is a simple python script that is designed to test whether or not a port is open based upon a ping. I will be adding more functionality to the script in the near future. 

#!/usr/bin/python 
import socket 
ip = raw_input("Enter the IP address: ")
port = input("Enter the  Port Number: ")
sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
if sock.connect_ex((ip,port)):
print "Port", port, "is closed"
else: 
print "Port", port, "is open"

