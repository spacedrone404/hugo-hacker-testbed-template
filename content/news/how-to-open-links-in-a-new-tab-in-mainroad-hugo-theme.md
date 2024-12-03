---
title: HOW TO OPEN LINKS IN A NEW TAB IN MAINROAD HUGO THEME 
description: 
date: 2021-09-12
thumbnail: "img/external-links.png"
categories:
  - "Software"
  - "FAQ"
  - "Webdev"
tags:
  - "HTML"
  - "Markdown"
weight: 1
---

<br>

I bet that many of you would like to open site links not in the same window, but in a background tab.
<br>
Such behavior is restricted by default settings of most Hugo themes. Mainroad is restricting it also. 
<br>
Here is a solution on how to overcome weird limitation.

Create file **render-link.html** in **_default** folder of the theme.
<br>
```
Name_of_your_site\themes\mainroad\layouts\_default\_markup\render-link.html 
```
Contents of **render-link.html** should be like this:

```
<a href="{{ .Destination | safeURL }}"{{ with .Title}} title="{{ . }}"{{ end }}{{ if strings.HasPrefix .Destination "http" }} target="_blank" rel="noopener"{{ end }}>{{ .Text | safeHTML }}</a>
```

<br>


<hr>


<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>