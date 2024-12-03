---
title: HOW TO SETUP CUSTOM FONTS IN WINDOWS 7 CONSOLE 
date: 2024-01-10
thumbnail: "img/gallery/2021.jpg"
categories:	
- "Software"
- "FAQ"
- "Vintage"
- "Windows 7"
tags:

- "Console"
- "Fonts"
- "Far"

weight: 1
---

<br>

As a hardcore user of [[dual-panel orthodox file manager]](https://farmanger.com) i always suffered because of sucky look of default console fonts.
<br>
Native preloaded font list has quite scarce selection, if you ask me.
<br>

<div align="center">

<img src="/img/console-fonts/far-fonts.png" width="325">  

</div>

<br>

To fix such disappointment you'll need:

* install desired fonts by means of windows control panel
<br>  
* copy EXACT FONT NAME fonts section in control panel
<br>

<div align="center">

<img src="/img/console-fonts/fonts-cp.png" width="284">  

</div>

<br>

* paste it into registry key into following branch

``` 
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Console\TrueTypeFont
```
* note that every new subsequent font should be added by a key with added one zero to registry key name
<br>

<div align="center">

<img src="/img/console-fonts/fonts-registry.png" width="604">

</div>

<br>
<br>

* reboot computer to apply & enjoy!

<div align="center">

**DEFAULT FONT**
<br>
<img src="/img/console-fonts/far-default.png" width="500">  

**CUSTOM FONT**
<br>
<img src="/img/console-fonts/far-custom.png" width="500">  



Vintage [[BigBlue Terminal]](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/BigBlueTerminal.zip) [direct link] font downloaded from [[NerdFonts]](https://www.nerdfonts.com/font-downloads).

</div>


<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>