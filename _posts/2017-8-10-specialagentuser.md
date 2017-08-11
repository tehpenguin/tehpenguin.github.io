---
layout: post
title: Pico CTF 2017 Special Agent User
category: ctf
---



<b>Category: Forensics</b>

Special Agent User

<i>We can get into the Administrator's computer with a browser exploit. But first, we need to figure out what browser they're using. Perhaps this information is located in a network packet capture we took: data.pcap. Enter the browser and version as "BrowserName BrowserVersion". NOTE: We're just looking for up to 3 levels of subversions for the browser version (ie. Version 1.2.3 for Version 1.2.3.4) and ignore any 0th subversions (ie. 1.2 for 1.2.0)
HINTS
Where can we find information on the browser in networking data? Maybe try reading up on user-agent strings.</i>

I downloaded the .pcap file and began to look for HTTP packets with GET or POST request within the HTTP packets. The first few packets I came accross did not have any User-Agents listed. Once I read through the contents of packet 80, I found the information I looking for: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.6; rv:25.0) Gecko/20100101 Firefox/25.0. This challenge is looking specifically for the browser with 3 levels of subversion for the browser version, which is Firefox/25.0.


![Image description](/images/specialuseragent.png)
