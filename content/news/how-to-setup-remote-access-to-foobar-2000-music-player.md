---
title: HOW TO SETUP REMOTE ACCESS TO FOOBAR 2000 MUSIC PLAYER
date: 2024-11-30
thumbnail: "img/gallery/1958.jpg"
categories:	
- "Software"
- "Technology"
- "Internet"
- "FAQ"
tags:
- "Windows7"
- "Audio"
- "90s"

weight: 1
---

<br>


Most of you have favorite PC audio player of their own, in my case it is [[Foobar2000]](https://www.foobar2000.org).
<br>
In Android 6 times there was a wonderful software called [[Foobar 2000 Controller]](http://foobar2000controller.blogspot.com). 
<br>
It was made to control audio player remotely from your smartphone in a convenient way.
<br>
For some reason i recall it today and decided to record installing process for future use.   
<br>
Guys from [[Hydrogen Audio]](https://hydrogenaud.io/index.php/topic,62218.0.html) forum helped me out in some questions and pointed me to the right direction.


To make things rolllin' you need to:

* [[download and install Foobar2000]](https://www.foobar2000.org/download), latest version 2.24 is working fine
* download and install into Foobar by double clicking [[HttpControl]](https://github.com/regorxxx/foobar2000-assets/blob/main/foobar2000%20controller/PC_new_installation_2.0.1/foo_httpcontrol_0_97_29.fb2k-component) component <font color="#00ff62">//download via download Raw file button</font>
* download these [[configuration files]](https://github.com/regorxxx/foobar2000-assets/tree/main/foobar2000%20controller/PC_new_installation_2.0.1/foo_httpcontrol_data/foobar2000controller) <font color="#00ff62">//download via download Raw file button</font>
* place them to ```%APPDATA%\foobar2000-v2\foo_httpcontrol_data\foobar2000controller ``` 
* launch Foobar and setup appropriate settings 
```
File > Preferences > Tools > HTTP Control
```

<div align="center">

Here is my options screen

<img src="/img/foobar2000-remote.png" width="512">


</div>


<br>

Http server should be accessible by means of:


```
http://192.168.1.240:8888/

```

And if everything is correctly installed you should see on web page something like:

```
Installed templates: foobar2000controller
```

<br>

If so, we have the right to move on.

* download and install [[Android part of software]](https://github.com/regorxxx/foobar2000-assets/blob/main/foobar2000%20controller/foobar2000%20controller%20PRO_0.9.4.0a.apk) <font color="#00ff62">//download via download Raw file button</font>
* In Android greeting wizard you need to replicate your IP desktop address  of machine where Foobar is installed, 
<br>
enter the same port number and you are good to go  


If for some reason nothing happening, try to disable your firewall or router filtering capabilities just for a time of testing.

<br>


> If you don't want to download ALL files by pressing download Raw file button million of times and 
<br>
you have [[Git]](https://git-scm.com/downloads) installed you can clone whole repository like this:

```
git clone https://github.com/regorxxx/foobar2000-assets.git
```

And then select all needed files that were mentioned here previously.


> Following materials were used during creation of an article:
<br>
* [[link #1]](https://github.com/regorxxx/foobar2000-assets/tree/main/foobar2000%20controller)
* [[link #2]](https://hydrogenaud.io/index.php/topic,62218.msg1043332.html#msg1043332)



<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>