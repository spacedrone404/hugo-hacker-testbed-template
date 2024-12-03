---
title: HOW TO RUN OBS STUDIO V29 IN WINDOWS 7
date: 2023-02-17
thumbnail: "img/obs29w7.png"
categories:	
- "Software"
- "Technology"
- "Vintage"
- "FAQ"
- "Lists"
- "Windows 7"
- "Hacks"

tags:
- "Obs"
- "EOL"
- "ESU"

weight: 1

---

> I'll keep post updated if any changes happen.

Recently last officially supported version was [[27.4.2]](https://trackerninja.codeberg.page/post/obs-studio-still-support-windows-7-and-this-fact-is-not-advertised).
<br>
But from now on we can use actual version of software. 

Here is small instruction list on how to make things rollin' under mighty Windows 7:

* Obtain hacked [[QT 6.3.1 DLLs for Windows 7]](https://web.tresorit.com/l/iWnTl#yGMg45iqZObF8miEZt7FaA) ||| [[Mirror]](https://cloud.disroot.org/s/ZecNemxBN26T2xn) [QT6 is not officially supported]
* Download [[CFF Explorer]](https://ntcore.com/files/CFF_Explorer.zip)[direct link] for basic resource hackery
* Obviously grab latest zipped archive [[OBS Studio 29.0.2]](https://github.com/obsproject/obs-studio/releases/download/29.0.2/OBS-Studio-29.0.2-Full-x64.zip) [direct link]
<br>
Beware that crappy exe-installer will spit out error that you have "obsolete OS", just ignore false statement and use zipped version instead.
* From extracted QT6 archive take files: 
<br>
**Qt6Core.dll**, **Qt6Gui.dll** and place them into **\OBS\bin\64bit** folder,
then take **QWindows.dll** and put it to **\OBS\bin\64bit\platforms** folder
* Run CFF Explorer, open **obs.dll**. Find "Import Directory", locate **KERNEL32.dll** file
* Find **IsWow64Process2** parameter and rename it to **IsWow64Process** [simple as that]
* Save changes to changed **obs.dll**
* **Start OBS Studio 29 and you are in the game again!**

<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>