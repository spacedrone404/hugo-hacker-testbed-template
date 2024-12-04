---
title: HOW TO EXPORT FIREFOX BOOKMARKS AND OPEN LOCALLY PLACED HTML FILES ON ANDROID 
date: 2024-08-08
thumbnail: "img/gallery/2021.jpg"
categories:	
- "Software"
- "Technology"
- "Software"
- "Rant"
- "FAQ"

tags:
- "Browser"
- "Firefox"

weight: 1
---

<br>

You might think that it is kinda ridiculous title, but read on to find out.

First of all you have to understand that i'm not going to share my personal bookmarks with some ugly copro 
<br>
that cloaks itself under the umbrella of free software ideas and use their lame anti-private sync. 
<br>
And i'm certainly not going to use any web service provided by these companies in any case. 
 
Of course we won't skip that generic rant part about how dumb project managers are for not implementing 
<br>
essential features like bookmark export or the ability to open local HTML files in 2024. 
<br>
But luckily we are not so dumb that we can't do the necessary things ourselves.


The first thing to mention is that we need a rooted device to do this rather funky trick.
<br>
<font color="red">Everything for the convenience of the housewife!</font> 

Locate: 

```
browser.db
```

```
/data/data/org.mozilla.firefox/files/mozilla/YOUR-PROFILE-ID.default/browser.db
```

In some cases you can run into the situation when there is no such file. Then look for:

```
places.sqlite
```

<font color="red">I love the accuracy and certainty of the program's structure!</font>
<br>
In case for Mull [Firefox fork which i'm using] file is located here:

```
/data/data/us.spotco.fennec_dos/files/mozilla/places.sqlite
```

Copy file to a PC and extract data via [[SQLite]](https://www.sqlite.org/download.html).
<br>
I used a [[recent binary]](https://www.sqlite.org/2024/sqlite-tools-win-x64-3460000.zip) for windows.
<br>
Database file and SQLite software should be in the same folder.

We have to make some selections from the various tables. 
<br>
**Moz_bookmarks** for titles and **Moz_places** for urls. 
<br>
Oh God, what a horrible logic!

To make things happen type the following magic:

```
sqlite3 places.sqlite "select '<a href=''' || url || '''>' || moz_bookmarks.title || '</a><br/>' as ahref from moz_bookmarks left join moz_places on fk=moz_places.id where url<>'' and moz_bookmarks.title<>''" > bookmarks.html
```

This exports a plain list of bookmark links from a compressed database to a separate HTML file. 
<br>
Of course it's not even close to heaven, but at least it's something.

It might look like that we're at the finish line, but that is definitely not the case.
<br>
<font color="red">More banger news! Firefox can't open locally placed HTML files in 2024!</font> ["Security" they say]. 

To bypass this moronic dumbsh#t install an old version of Firefox, i chose [[Fenix 84]](https://github.com/mozilla-mobile/fenix/releases/tag/v84.1.4) for this purpose.

Remember to turn off telemetry:

```
SETTINGS -> PRIVACY & SECURITY -> DATA COLLECTION
```


To open the bookmark file type the following in the address bar of the legacy browser: 

```
file:///storage/emulated/0/Download/bookmarks.html
```

> <font color="red">Note that</font> there are three [!] slashes instead of the usual two! 

<font color="red">The inability to export accumulated bookmarks coupled with the inability to open local HTML files can be considered as horrendously strange especially in 2024.</font> 
<br>
Maaaan, i just can't believe my eyes, what i can is to imagine how many similar restrictions there will be in Android 28.

As you can see, it wasn't for nothing that I decided to stock up on the Oppo X6 which runs Android 13 by default.
<br>
And i'm definitely is not going to upgrade to subsequent versions, because <font color="red">the further google goes the more artificial limitations are added.</font> 
<br>
It looks like they will end up like Windows.

<font color="red">More importantly, open source communities like Mozilla are going the same way, not listening to the community at all 
<br>
and implementing dubious and vague features instead of the ones that are really expected.</font>


The rant is over, but at least some useful things have been done.
<br>
I hope i'm not woefully boring and promise to do more entertaining posts in the future.
  
<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>