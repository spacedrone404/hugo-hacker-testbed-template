---
title: FENNEC F-DROID AS A REPLACEMENT FOR AGING ICECAT 68 ESR [ANDROID]
description: Choosing Android, bloat free secure browser
date: 2021-10-19
thumbnail: "img/fennec.png"
categories:
  - "Software"
  - "Technology"
  - "Rant"
  - "Reviews"
  - "Android 8"

tags:
  - "Firefox"
weight: 1
---

> **UPDATED ON: 2023-02-20**
<br> 
I recommend to replace Fennec F-Droid with [[Mull Browser]](https://f-droid.org/en/packages/us.spotco.fennec_dos) due to the fact that is **COMPLETELY** free from telemetry.
<br>
In contrast to Fennec Mull browser do not trigger any mozilla or google connections, so take a note.
<br>
**And for God's sake do not use plain Firefox, it is almost like chrome now!**


As my main web surfer IceCat begin to showing it’s age and don’t have any new versions apart from **"super-new" 68.4.2 ESR.**
<br>
[it can be found on the web, but only @ [[F-Droid Archive repository]](https://f-droid.org/archive)] So, I start to look for a viable replacement for it. 

Although, I ‘m using [[Privacy Browser]](https://www.stoutner.com/privacy-browser) as a backup option it doesn’t fully match my requirements. 
<br>
It’s even prone to crashing on [[4Gb Ram Sony XZ1 Compact phone]](https://trackerninja.codeberg.page/post/some-notes-on-sony-xz1-compact), assume memory leaks are taking place. 
<br>
**And yeah, it is chrome-based-webview thing, so take a note before using it.**

Taking into account recent Mozilla degradation changes such as:
* dropping support of mandatory FTP protocol
* starting to trace it’s users even more than ever
* absence of essential **about:config** option [we are talking about android version]
* copying chrome in every aspect

**We can safely say that Mozilla is for sure a sinking ship.**

But nevertheless these sad words some time ago I randomly stumble upon [[Fennec F-Droid browser]](https://f-droid.org/en/packages/org.mozilla.fennec_fdroid).
 
**The key points of Fennec F-Droid are:**
* pretty modern, safe version of browser based upon Firefox 81 [so a bit of future-proof is here]
* no telemetry stuff [**at least telemetry is replaced with empty stubs**, see below for explanation]
* **presence of about:config option** for under the hood fine tunings [which we all like so much]

I’ve researched the topic and find out that [[we can safely use any version which is less than 81.1.1]](https://www.apkmirror.com/apk/mozilla/fennec-f-droid/fennec-f-droid-81-1-1-release/fennec-f-droid-81-1-1-android-apk-download). 
Relan, F-Droid contributor [[reported that tracking with Firebase, Adjust, Leanplum was introduced right in 81.1.1 version]](https://forum.f-droid.org/t/welcome-a-new-fennec-f-droid/11113). However, in Fennec F-Droid [[data collecting endpoints were replaced by empty stubs]](https://www.reddit.com/r/fdroid/comments/npoakc/fennec_with_trackers). 

**I won’t trust this so much because development of repo was recently retaken by filthy mozilla.**
Nevertheless the announcement of code contributor regarding empty code stubs is a ringing bell. Stubs can be easily changed with real trackers in the upcoming future. And it will. 108%. Not less than this. 

> In conclusion I would like to underline the fact that even in today’s situation we have multiple choices for mobile web browser. 
> <br>
> **Ain’t that pretty?**
> <br>
> Make sure to check [[this post]](https://trackerninja.codeberg.page/post/selecting-your-windows-android-browser) also.

<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>