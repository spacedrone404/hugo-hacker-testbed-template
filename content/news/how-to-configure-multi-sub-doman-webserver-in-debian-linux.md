---
title: HOW TO CONFIGURE MULTI SUB-DOMAN WEBSERVER IN DEBIAN LINUX
date: 2024-08-21
thumbnail: "img/gallery/1994.jpg"
categories:	
- "Software"
- "Technology"
- "FAQ"
tags:
- "Debian"
- "Linux"

weight: 1
---

<br>

Firsts things first, for better file handling install [[Midnight Commander]](https://midnight-commander.org):

```
sudo apt-get install mc
```

Download fresh version of webserver software:

```
sudo apt-get install apache2
```

Locate and edit configuration file: 

```
/etc/apache2/apache2.conf
```

Note that in some distributions it can named as httpd.conf.

No file at all? You can create it by:


```
touch apache2.conf
```

For relatively easy editing i recommend Nano editor.

```
sudo apt-get install nano
```

* CTRL+O ► to save file
* CTRL+X ► exit file

Here is an example for locally placed development webserver, containing two sub-domains.
<br>
Site and it's sub-domains are set to use 8484 port.     


```
Listen 8484
NameVirtualHost localhost:8484

<VirtualHost localhost:8484>
        ServerName localhost
        ServerAlias localhost
        DocumentRoot /var/www/website.com
</VirtualHost>

<VirtualHost dev.localhost:8484>
        ServerName localhost
        ServerAlias localhost
        DocumentRoot /var/www/website.com/_dev
</VirtualHost>

<VirtualHost subdomain.localhost:8484>
        ServerName localhost
        ServerAlias localhost
        DocumentRoot /var/www/website.com/_subdomain
</VirtualHost>

```


So, in the end of the day we have three folders:

```
website.com [1]
  └  _dev [2]
  └  _subdomain [3]
```

> Take a note that underscore in folder naming is not mandatory thing and i'm using it because i like to see the most important folders above all others.


And three websites to be developed:

```
http://localhost:8484
http://dev.localhost:8484
http://subdomain.localhost:8484

```

<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>