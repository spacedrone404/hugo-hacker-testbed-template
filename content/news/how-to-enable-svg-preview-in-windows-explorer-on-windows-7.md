---
title: HOW TO ENABLE SVG PREVIEW IN WINDOWS EXPLORER ON WINDOWS 7
date: 2023-11-03
thumbnail: "img/svg.png"
categories:	
- "Technology"
- "Vintage"
- "Software"
- "Windows 7"
- "FAQ"

tags:
- "SVG"
- "Graphics"
- "Gems"

weight: 1

---

<br>

So, you <u style="text-decoration:underline dotted; text-decoration-thickness: 4px; text-decoration-color: red">want to be a hip</u> and would like to have the feature of SVG preview in file explorer like in fancy windows 11 of friend of yours?
<br>
It is surely possible, even on <u style="text-decoration:underline dotted; text-decoration-thickness: 4px; text-decoration-color: red">such old crone like Windows 7!</u>

[[SVG See]](https://github.com/tibold/svg-explorer-extension/releases) is an excellent application, which bring such functionality to our crony operating system.
 
If you are for some reason don't observe SVG previews in explorer there are a couple of things that you could try to fix things up:

* make sure that file explorer is set to View ► Medium Icons 
* check that Tools ► Folder Options ► View ► Always show icons, never thumbnails [ ] is unticked
* hard reset system icon cache by following commands:

```
ie4uinit.exe -ClearIconCache
taskkill /IM explorer.exe /F
DEL "%localappdata%\IconCache.db" /A
DEL "%localappdata%\Microsoft\Windows\Explorer\iconcache*" /A
shutdown /r /f /t 00
```

> Command prompt should be executed with admin privileges.
<br>
Last line will reboot machine to apply complete reset.
 

<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>