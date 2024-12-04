---
title: HOW TO IMPORT CUSTOM CERTIFICATE TO CERTIFICATE STORAGE IN DEBIAN LINUX
date: 2024-08-19
thumbnail: "img/gallery/1975.jpg"
categories:	
- "Software"
- "Technology"
- "FAQ"
- "Security"
tags:
- "Debian"
- "Linux"

weight: 1
---

<br>


Say you are trying to install software and receive message from the operating system about untrusted certificate in certificate chain.
<br>
In such case you need to import certificate of the middle-man organization into the Linux certificate storage to make things happen.   


If for some reason your third-party certificate comes in DER binary format, you should convert it to CRT format:

```
openssl x509 -inform DER -in certificate.der -out certificate.crt
```

Copy to storage:

```
sudo cp certificate.crt /usr/local/share/ca-certificates/my-custom-ca/
```

> Do not forget to install [[Midnight Commander]](https://midnight-commander.org) to make file management operations a bit easier:

```
sudo apt-get install mc
```

Update cert storage:

```
sudo update-ca-certificates
```

To check installed cert [exact name without extension]:

``` 
ls /etc/ssl/certs | grep certificate 
```

<br>

If everything is OK utility should display full name of certificate with extension.

If you removed any certificates from the storage and would like to refresh the storage:
```
sudo update-ca-certificates --fresh
```

> That's it for today, catch me around!


<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>