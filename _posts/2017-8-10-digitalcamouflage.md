---
layout: post
title: Pico CTF 2017 Digital Camouflage
category: ctf
---
<b>Digital Camouflage</b>

Category: Forensics

We need to gain access to some routers. Let's try and see if we can find the password in the captured network data: data.pcap.
HINTS
It looks like someone logged in with their password earlier. Where would log in data be located in a network capture?
If you think you found the flag, but it doesn't work, consider that the data may be encrypted.

After downloading the .pcap file, I opened the file with wireshark. I sorted the packets by protocol to and began searching for any HTML protocol packets that had POST data. Packet number 122 had the criteria I was looking for and inside the HTML form data I saw a username and password in clear text. The password had padding on the the end indicating it was base64 encoded. 

![Image description](/images/digitalcamouflag.png)

I copied the encoded password and then decoded the password with base64

![Image description](/images/digitalcamoulfag2.png)
