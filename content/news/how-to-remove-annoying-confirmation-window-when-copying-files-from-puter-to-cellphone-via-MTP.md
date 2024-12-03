---
title: HOW TO REMOVE ANNOYING CONFIRMATION WINDOW WHEN COPYING FILES FROM PUTER TO CELLPHONE OVER DUMB MTP PROTOCOL
description: Remove annoying confirmation window when copying “non-standard” files from ‘puter to cellphone over dumb MTP protocol
date: 2021-09-23
thumbnail: "img/mtp/mtp.png"
categories:
  - "FAQ"
  - "Software"
  - "Windows 7"
  - "Android 8"
  - "Hacks"

tags:
  - "MTP"
  - "Storage"

weight: 1
---


<br>


<div align="center">

Of course you run into situations when you would like to copy "non-standard" files to your 
<br>
Android smartphone and dumb MTP protocol showed up window like this one:

<img src="/img/mtp/mtp1.png" width="500">
<br>
<br>

And this torture repeated after every new file type copied.
Such imbecility can be removed by following command in admin console:


</div>

```
regsvr32 /u wpdshext.dll
```

<div align="center">
<img src="/img/mtp/mtp2.png" width="500">
</div>

<br>
<br>

That's all, limitation is gone.

**Another hint**, which potentially can help to overcome weird design of MTP protocol.
<br>
You can’t create [by means of generic drag’n’drop] shortcut pointing to folder, which is located on MTP device.
Yeah, another MTP shite. 
<br>
However, there is not so obvious way to make this happen.

 * Connect your cellphone through MTP to the computer.
 * Just right click on cellphone folder, and select copy.
 * On windows desktop right click and select **paste as a shortcut** [this is not typo].
<br>

► **BLOG UPDATE:** 

<div class="demo_line">

<p style="text-align:right;">Added some glitch animations and scanline VHS effects. 
<br>
Are we in 90s after all or what? 
<br>
<a href="https://creativemarket.com/spacedrone808" target="_blank">Imagery by spacedrone808 </a></p>

</div>

<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>