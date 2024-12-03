---
title: HOW TO ENABLE HTML CODE IN MARKDOWN FILES
description: Changing configuration file of Hugo engine
date: 2021-08-23
thumbnail: "img/html-mark.png"
categories:
  - "Software"
  - "Webdev"
  - "FAQ"
tags:
  - "Markdown"
  - "Hugo"
  - "Html"
weight: 1
---

<br>


Trick is very simple, if you know where to dig.
Just find **config.toml** file of your Hugo theme and add following section.

<!--more-->

```
[markup]
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true  # Enable html code inside markdown files

```

This code will enable "unsafe HTML" code inside markdown *.md files.


<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>