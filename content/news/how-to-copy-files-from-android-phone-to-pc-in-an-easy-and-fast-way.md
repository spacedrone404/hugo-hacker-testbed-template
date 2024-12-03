---
title: HOW TO COPY FILES FROM ANDROID PHONE TO PC IN AN EASY AND FAST WAY
date: 2024-07-21
thumbnail: "img/gallery/1958.jpg"
categories:	
- "Software"
- "Technology"
- "Vintage"
- "FAQ"
- "Windows 7"
- "Android 8"

tags:
- "MTP"
- "Console"

weight: 1
---

<br>
         
First things first. 
<br>
I often need to copy substantial amount of photos from my phone.
<br>
It can't be done via Windows GUI without millions of mouse clicks or keystrokes. 
<br>
Here you will find a solution on how to do this in a proper way.
<br>
The key tool for this will be [[ADB]](https://en.wikipedia.org/wiki/Android_Debug_Bridge), developer tools for Android.

<font color="red">Wishes: command line, batch, no file explorer, no mouse, no clickety-clack.</font>

Sicking tired of all of these not-so-precise-instructions i've decided to make my own.
<br>
Why on Earth such thing as copying plain files become so complicated? 
<br>
Answer is pretty straightforward: Microsoft and Apple are top-notch dorks that is why.

[[MTP]](https://en.wikipedia.org/wiki/Media_Transfer_Protocol) is a horrible protocol, which was created by Microsoft to transfer files between multimedia devices. 
<br>
The implementation of it's functionality is quite terrible. I am not going to rant about it's quirks and bugs today. 
<br>
I just wanted to mention that Apple's idea of copying certain files through a proxy-program called iTunes is worse
<br>
than the MTP protocol. So, at least MTP is not the worst solution in the world. 

Enough of this endless intro, back to the main topic.

First of all you need to enable USB debugging on your Android device.
<br>
This can be done from Developers settings, which are usually hidden and 
<br>
have to be enabled by gazillions of taps on the build number of your Android version. 
<br>
In most cases it is located somewhere around "About device" section.

If you want to get ADB software up and running on your Windows 7 machine, 
<br>
you'll need to make sure you have the right tools for the job.
<br>
The official ADB site provides only Windows 10 compatible crap 
<br>
and we definitely don't want this, don't we?

<font color="red">And hey, kiddo, remember that you are on Windows 7 website? 
<br>
There's nothing else in this reality.</font>

* Grab tested and working version from [[ClockworkMod]](https://adb.clockworkmod.com).

* Connect your device to PC and confirm <font color="red">File transfer</font> on the device.

* Install MSI, find ADB folder and access it from the command line.

* Type @ command line to show connected devices:

```
adb devices
```

<div align="center">

You should see something like this:

<img src="/img/adb.png" width="512">

<br>
<br>

That means the device is already connected.

</div>


These days most smartphones come with no sd-card at all. Everything for your convenience.
<br>
<font color="red">Give your generous high fives and props to dumb-heads from Apple.</font> 
<br>
That is why to access the internal flash of the device we need such not-so obvious path:

```
/storage/emulated/0/
```

Finally, to copy files from Android phone to PC type something like this:

```
adb pull /storage/emulated/0/DCIM/Camera c:\my-photos\
```

This line will copy folder <font color="red">Camera</font> with all it's contents to your PC on drive C to folder <font color="red">my-photos</font>.
<br>
Of course i copy from multiple folders, that is why combininig multiple command lines into one convenient batch file is a thing to do.
<br>
And yeah, if you want to copy files from PC to Phone just replace <font color="red">pull</font> with <font color="red">push</font> and you are good to go.

Here is an example of my batch file:

```
c:
cd "C:\Program Files (x86)\ClockworkMod\Universal Adb Driver" 
adb pull /storage/emulated/0/DCIM/Camera C:\Users\#p8#8\Desktop\4STOCK
adb pull /storage/emulated/0/Pictures/Raw C:\Users\#p8#8\Desktop\4STOCK

```
In this example I copy <font color="red">JPG</font> files from <font color="red">Camera</font> folder and <font color="red">RAW</font> files from <font color="red">Raw</font> folder.
<br>
Damned android file system and their unobvious mishmash standards for developers.
<br>
Poor devs!


That is it for today. 
<br>
<font color="red">Enjoy the `puters.</font>



<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>