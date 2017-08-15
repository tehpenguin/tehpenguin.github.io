---
layout: post
title: Pico CTF 2017 Meta Find Me
category: ctf
---
<b> Category: Forensics </b>

Meta Find Me

<i>Find the location of the flag in the image: image.jpg. Note: Latitude and longitude values are in degrees with no degree symbols,/direction letters, minutes, seconds, or periods. They should only be digits. The flag is not just a set of coordinates - if you think that, keep looking!
HINTS
How can images store location data? Perhaps search for GPS info on photos</i>

In this challenge we are given an image and we need to find the flag within the image. The first thing we look at is the meta data or EXIF data in the image. We can do that with the command exif image.jpg

![Image description](/images/metafindme3.jpg)

Exif shows some gps information that will need for our flag. 

![Image description](/images/metafindme1.png)

We are still missing some metadata so I opened up the file with a hexeditor and was able to find the other portion of the flag. 

![Image description](/images/metafindme2.png)

Combining our two parts of the flag together we get:
flag_2_meta_4_me_88_4_06c3
