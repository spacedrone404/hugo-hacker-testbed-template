---
title: HOW TO MINIMIZE LAPTOP POWER CONSUMPTION
date: 2023-06-29
thumbnail: "img/laptop-power.png"
categories:
  - "Hardware"
  - "Software"
  - "Technology"
  - "Vintage"
  - "Lists"
  - "FAQ"
  - "Windows 7"
  - "Tweaks"

tags:
  - "Laptop"
  - "Performance"

weight: 1
---

<br>

Say you need to run on a laptop battery vintage or simply non-demanding applications for an extremely long time.
<br>
Here is a little breakdown of mandatory things to do:

* turn off in BIOS unneeded devices like camera, sd-card reader, fingerprint scanner, gsm-modem, wifi, bt or whatever you are not using
* turn on power saving features like various C-power states
* turn off hyper-threading and hi-core count [if you have such ability]
* lower screen brightness to acceptable level 
* check my [[quick]](https://trackerninja.codeberg.page/post/mandatory-steps-to-optimize-newly-installed-windows-7) and [[comprehensive]](https://trackerninja.codeberg.page/post/comprehensive-windows-7-faq-plus-catalog-of-previous-links-related-to-tweaking) optimization FAQs
* get rid of [[unneeded services and bloat applications]](https://trackerninja.codeberg.page/post/remove-telemetry-spying-updates-on-windows-7)

Also you can use core parking utility [[Park Control]](https://bitsum.com/parkcontrol), but in this mini-guide i'll show you how to set power related things up 
via internal Windows 7 tools. 
<br>
First go to:

```
* Control Panel ► Power Options ► Select Power Save plan
```
```
* Control Panel ► Power Options ► Power Saver ► Change plan settings ► Dim the display after 2 minutes
```
```
* Control Panel ► Power Options ► Power Saver ► Change plan settings ► Change advanced power settings
```

Options to tweak here:

```
* Wireless Adapter Settings ► Power Saving Mode ► Maximum Power Saving
```
```
* USB settings ► USB selective suspending ► Enabled
```
```
* PCI Express ► Link State Power Management ► Maximum power savings
```

Also consider to decrease GPU power consumption in Windows Power Options: 

```
* Intel Graphics Settings ► Intel Graphics Power Plan ► Maximum battery life
```

.... or separate driver settings, if you have newer internal GPU or discrete video card.  

<br>

And finally the most important ones:

```
* Processor power management ► System cooling policy ► Passive
```
```
* Processor power management ► Maximum processor state ► 48%
```

Choose **Max CPU state** based upon **your preference**.

As for me, i'm doin' **really looooooooong** [[Fallout 2]](https://trackerninja.codeberg.page/post/how-to-play-classic-fallout-2-to-get-the-most-out-of-it-in-2023) sessions and quite satisfied 
<br>
even with half performance of my [[i7-8550U]](https://technical.city/en/cpu/Core-i7-8550U) installed in [[Lenovo X1 Carbon Gen6]](https://trackerninja.codeberg.page/post/lenovo-x1-carbon-6th-generation-brief-review).


<div class="demo_line">

Take a note that sticking with this guide will resolve fan noise issue once and for all!

</div>


> I hope that i don't need to tell you about widely known windows 10 suckage in terms of power effectiveness 
<br>
due to loads of unneeded services and stock bloatware.


<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>