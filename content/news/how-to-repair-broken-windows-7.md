---
title: HOW TO REPAIR BROKEN WINDOWS 7
description: Sfc, Dism tools
date: 2021-08-20
thumbnail: "img/fix-files.png"
categories:
  - "Software"
  - "Vintage"
  - "Lists"
  - "FAQ"
  - "Windows 7"
tags:
  - "Tools"

weight: 1
---

<br>


> To check system hard drive and fix errors:

```
chkdsk c: /f 
```
To check system hard drive, fix errors, locate and mark bad sectors:

```
chkdsk c: /r
```

Very basic command to check integrity of system files:

```
sfc /scannow
```


**If sfc can't help you try DISM.**


Check system health for any corruption presence:

```
Dism /Online /Cleanup-Image /CheckHealth
```


Check system health for store corruption presence:

```
Dism /Online /Cleanup-Image /ScanHealth
```

Finally, repair command:

```
Dism /Online /Cleanup-Image /RestoreHealth
```

**PS If i recall something that i've missed, will post it as an update later on.**  

<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>