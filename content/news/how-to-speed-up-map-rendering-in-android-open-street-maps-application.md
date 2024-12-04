---
title: HOW TO SPEED UP MAP RENDERING IN ANDROID OPEN STREET MAPS APPLICATION
date: 2022-12-11
thumbnail: "img/osm+.png"
categories:	
- "Software"
- "Technology"
- "Android 8"
- "Tweaks"

tags:
- "Performance"


weight: 1

---

> **UPDATED ON: 2023-03-31**

To speed up map rendering a bit turn on [[OpenGL]](https://en.wikipedia.org/wiki/OpenGL) acceleration in software settings.

In version 4.3 new OpenGL renderer was transferred from hidden settings to generic ones.

Now option can be found here:

```
≡ Settings ► OsmAnd settings ► Map rendering engine ► Version 2 (OpenGL)

```
It looks like that as of version 4.3.12 all compatibility and performance issues were solved.
<br>
So, i advice you to install 4.3.12 as a bare minimum to work with.

Also you'll need at least [[Snapdragon 810]](https://www.notebookcheck.net/Qualcomm-Snapdragon-810-MSM8994-SoC.116952.0.html) CPU for satisfying performance.


> Note that on Android 6 devices feature can work incorrectly or not work at all. 
<br>
On Android 7 devices it can take longer initialization, but faster rendering afterwards.
<br>
Tested on Android 8.0 and [[Sony Xperia XZ1 Compact]](https://www.gsmarena.com/sony_xperia_xz1_compact-8610.php) and setting really gives a boost. 
<br>
And take a note, that such acceleration may use more battery if you are up to such conditions.

<br>


<hr>


<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>