---
title: HOW TO RUN NODE.JS 18.18 LTS ON OBSOLETE WINDOWS 7
date: 2023-06-14
thumbnail: "img/node7/node7header.png"
categories:	
- "Software"
- "Technology"
- "Vintage"
- "Webdev"
- "Windows 7"
tags:
- "EOL"
- "ESU"
- "Nodejs"

weight: 1

---

<br>

> **UPDATED ON: 2024-08-29**

Node.js dropped Windows 7 "support" rigth after [[version number 13]](https://nodejs.org/download/release/latest-v13.x).What a load of sh#t.
<br>
Today i'll tell you how to overcome this nonsense and run latest LTS version [[Node.JS 18.x]](https://nodejs.org/download/release/latest-v18.x) without any problems.
<br>
More newer versions may work also. I'll leave you some room for experiments.
<br>
Recently i found excellent already [[patched installer of NodeJS 18]](https://github.com/Alex313031/node18-win7) 

First of all you need to download zipped version of software, not msi one.

```
node-v18.18.2-win-x64.7z   
```
or

```                        
node-v18.18.2-win-x64.zip  
``` 


Unpack archive in any folder on drive C.
I'll use this path:

```
C:\Program Files\nodejs
```


Then <u>three system</u> variables must be declared in Windows environment.


* Add to system **<font color="red">Path</font>** following string:

```
C:\Program Files\nodejs

```


* Add to system variables **<font color="red">NODE_PATH</font>** parameter with the same value:

```
C:\Program Files\nodejs
```

* And finally add to system variables **<font color="red">NODE_SKIP_PLATFORM_CHECK</font>** parameter with value:

```
1
```


<div align="center">


**Things should look like this:**
<br>
<img src="/img/node7/node-vars.png" width="370">
<hr>
<br>

**Run command line and check that Node.js is installed correctly:**
<br>
<img src="/img/node7/node-ver.png" width="800">
<hr>
<br>

**You can also check it from Visual Studio Code Power shell terminal:**
<br>
<img src="/img/node7/node-vscode.png" width="512">
<hr>
<br>

</div>

> Usually things should work without reboot, but if you for some reason run into unexpected things please reboot just to make sure that everything is applied correctly.

<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>