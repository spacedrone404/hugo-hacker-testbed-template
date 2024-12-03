---
title: EXIFTOOL ▀ HOW TO FAST TAG GRAPHICS FILES WITH PERSONAL METADATA
date: 2022-02-20
thumbnail: "/img/exif.png"
categories:	
- "Software"
- "FAQ"

tags:
- "Exif"

weight: 1

---


<br>

[[Exiftool]](https://www.exiftool.org) is a convenient command line tool, which allows to change meta data of media files, like photos and pictures.
<br>
You can download it [[here]](https://www.exiftool.org/exiftool-12.40.zip).


**CLEARING IPTC/EXIF METADATA IN ALL EXISTING FILES**

```
c:\exiftool.exe -overwrite_original -all= C:\PATH-TO-YOUR_FOLDER
exit
```

**CHANGING/OVERWRITING TAG METADATA IN APPOINTED FOLDER**

```
c:\exiftool.exe -overwrite_original -XMP-iptcCore:CreatorWorkEmail="YOUR EMAIL ADDRESS" -XMP-iptcCore:CreatorWorkURL="YOUR WEBSITE" -artist="YOUR NAME" -copyright="YOUR COPYRIGHT" -Credit="YOUR NAME" -Source="YOUR NAME" -sep ", " -keywords="background, backdrop, postcard, design, element, wallpaper, dramatic, concept, decoration, scene, vivid, vibrant, travel, trip" C:\FOLDER-TO-PROCESS
exit
```

<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>