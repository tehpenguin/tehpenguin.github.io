---
layout: post
title: Pico CTF 2017 Speacial Agent User
category: ctf
---



<b>Category: FOrensics</b>

Special Agent User

We can get into the Administrator's computer with a browser exploit. But first, we need to figure out what browser they're using. Perhaps this information is located in a network packet capture we took: data.pcap. Enter the browser and version as "BrowserName BrowserVersion". NOTE: We're just looking for up to 3 levels of subversions for the browser version (ie. Version 1.2.3 for Version 1.2.3.4) and ignore any 0th subversions (ie. 1.2 for 1.2.0)
HINTS
Where can we find information on the browser in networking data? Maybe try reading up on user-agent strings.
