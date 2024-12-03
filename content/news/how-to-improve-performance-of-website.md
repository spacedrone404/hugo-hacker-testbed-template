---
title: HOW TO IMPROVE PERFORMANCE OF WEBSITE
date: 2023-11-04
thumbnail: "img/imporveperf.png"
categories:	
- "Software"
- "Technology"
- "FAQ"
- "Webdev"

tags:
- "Internet"
- "Website"

weight: 1

---

<br>

> **UPDATED ON: 2023-11-04**

Nothing complex here, at least at this time.
<br>
Here i'll accumulate performance related information. 

## ░▒▓ LAZY LOADING OF IMAGES ▓▒░

Just implemented lazy loading at my main index page.
<br>
Concept is pretty simple you are loading images only when they appearing in the viewport of the browser.
<br>
All you need to do is just to apply <font color="red">loading="lazy"</font> to the classes of loaded images.


```
<img loading="lazy" src="/img/demo./png" alt="Picture">

```
In my case it was like this:

```
<img loading="lazy" src="{{ .Params.thumbnail | relURL }}" alt="{{ .Title }}">

```

<hr>

## ░▒▓ PRELOADING FONTS ▓▒░


If you are using custom fonts, they should be loaded at first place, to maintain consistency of page.

Can be done by adding <font color="red">rel="preload"</font> line to loaded CSS file.


```
<link rel="stylesheet" rel="preload" href="styles.css">

```

In my case it was like this:

```
<link rel="stylesheet" rel="preload" href="{{ $style.RelPermalink }}">

```

And don't forget to use WOFF2 fonts, because of a really small size. 

<hr>

## ░▒▓ MINIFYING CSS STYLES ▓▒░

When uploading site to the hosting always minify [optimize] CSS and Js code to improve loadind times of website. 


<font color="red">GENERIC CSS CODE</font>
<br>
```
@font-face {
    font-family: 'amiga_topaz_unicode_rusRg';
    src: url('/fonts/amiga-webfont.woff2') format('woff2'),
 	 url('/fonts/amiga-webfont.woff') format('woff');
    font-size: 18px;
    font-weight: normal;
    font-style: normal;

}


@font-face {
    font-family: 'MisterGiacco-Bold';
    src: url('/fonts/MisterGiacco-Bold.woff2') format('woff2'),
         url('/fonts/MisterGiacco-Bold.woff') format('woff');
    font-size: 18px;

}

```

<font color="red">OPTIMIZED/MINIFIED CSS CODE</font>
<br>
```
@font-face {font-family: 'amiga_topaz_unicode_rusRg';src: url('/fonts/amiga-webfont.woff2') format('woff2'), url('/fonts/amiga-webfont.woff') format('woff');font-size: 18px;font-weight: normal;font-style: normal;}@font-face {font-family: 'MisterGiacco-Bold';src: url('/fonts/MisterGiacco-Bold.woff2') format('woff2'), url('/fonts/MisterGiacco-Bold.woff') format('woff');font-size: 18px;}@font-face .... 

```

Neat tool to use: [[CSS BEAUTIFIER]](https://beautifytools.com/css-beautifier.php).
<br>
Utility formats your CSS code, makes it minified or more readable if you want to. 

<hr>

## ░▒▓ OPTIMIZE YOUR IMAGES ▓▒░

Always optimize images in graphical editor by internal tools or if your are passionate enough do external optimization also.

[[Excellent utils]](https://trackerninja.codeberg.page/post/pinga-and-gif-optimizer-compression-tools) to optimize PNGs and animated GIFs.
<br>
Also check the GRAPHICS & SVG sections of my [[collection of links]](https://trackerninja.codeberg.page/post/essential-links-for-frontend-web-developer).
 
<hr>

## ░▒▓ ANOTHER TRICK ▓▒░


...
<br>
...
<br>
...
<br>
...
<br>


<hr>


## ░▒▓ PROPER LINKS ▓▒░

[[CSS-Tricks]](https://css-tricks.com) ► nice site to acquire optimization knowledge. 

[[ESSENTIAL FRONTEND DEVELOPER LINKS]](https://trackerninja.codeberg.page/post/essential-links-for-frontend-web-developer) may come in handy too.
 
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>