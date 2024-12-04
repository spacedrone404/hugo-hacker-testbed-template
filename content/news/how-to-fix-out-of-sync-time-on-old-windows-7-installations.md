---
title: HOW TO FIX OUT OF SYNC TIME ON OLD WINDOWS 7 INSTALLATIONS
date: 2023-10-08
thumbnail: "img/out-of-sync.png"
categories:	
- "Technology"
- "Vintage"
- "Software"
- "Windows 7"
- "FAQ"

tags:
- "Services"

weight: 1

---

A couple of weeks ago i run into problem related to out-of sync time clock.
<br>
Tried almost all imaginable solutions, like time service restarting, checking that internet time-sync option is turned on and so on 
<br>
and so forth. Of course to no avail at all. How typical! My Windows 7 installation dates back to early 2019 and i've plethora 
<br>
of software installed, and more over system is heavily customized so plain reinstall of operating system is not an option in my case. 
<br>
Too much work to be done, so i come up with a solution in a slacker's way, as usual.  

To fix things up i put a simple batch file with admin privileges into startup folder.


```
win32tm /resync
```

**<font color="red">And tada! Everything returned back on track.</font>** 

I understand that it is a workaround, but what the heck if it works!
<br>
I'm planning windows reinstall somewhere around autumn of 2024, when POS updates will reach their end of life. 
<br>
Just to start from scratch with fully updated distribution.


<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>