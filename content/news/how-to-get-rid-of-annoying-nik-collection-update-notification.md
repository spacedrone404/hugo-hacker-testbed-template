---
title: HOW TO GET RID OF ANNOYING NIK COLLECTION UPDATE NOTIFICATION
description: Turn off update notification
date: 2021-10-28
thumbnail: "img/nik.png"
categories:
  - "FAQ"
  - "Software"
  - "Technology"
  - "Tweaks"
tags:
  - "Photoshop"

weight: 1
---

<br>

[[Nik Collection]](https://nikcollection.dxo.com/) is a great graphical effects plugin pack to work with your favorite raster editor [mine is [[Affinity Photo]](https://affinity.serif.com/en-us/photo) in case you are interested].
<br>
Everything is fine, except annoying update popup, which is opening right after every plugin initialization. 
<br>
Such stuff completely breaks workflow if you don't want to update for some reason. 
<br>
And there is no way to turn it off from GUI using normal methods.

However, you can shut update checks off from configuration file, which is located here:

```
C:\ProgramData\DxO\Nik Collection\NikCollection.cfg
```

Find the following section:

```
	<group name="Checkforupdate">
		<key name="LastCheck" type="string" value="1634475377"/>
	</group>
```
In my case number is "1634475377", which i replace with value="2634475377".
<br>
Putting **TWO** instead of **ONE** will give me update timeout right up to 2053 or smth.
Should be sufficient, i guess. 
<br>
Long number is a date in Unix format pointing to the date when last update check happened.

**So, that's it for today, hope that somebody will find post useful. See you in a while.**

<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>