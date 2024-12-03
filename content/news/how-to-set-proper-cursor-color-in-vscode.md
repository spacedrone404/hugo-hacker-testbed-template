---
title: HOW TO SET PROPER COLOR FOR CURSOR AND COMMENTS IN VSCODE EDITOR
date: 2023-06-28
thumbnail: "img/vscode-color/vscode-color-header.png"
categories:	
- "Software"
- "Technology"
- "Vintage"
- "FAQ"
- "Webdev"
- "Windows 7"
- "Hacks"

tags:
- "x64"
- "EOL"
- "ESU"
- "Vscode"

weight: 1

---

<br>

> **UPDATED ON: 2023-12-02** 

The main reason i've decided to write this note is indistinct default color mappings and inability to solve issue simply using GUI of software.

<br>

In main configuration file:

```
settings.json
```
add following lines:

```
"workbench.colorCustomizations": {
        "editorCursor.foreground": "#ff0000",
        "terminalCursor.foreground": "#02ED3D",
        "editorLineNumber.activeForeground": "#ff0000",
        "editor.lineHighlightBackground": "#016119",
        "editor.lineHighlightBorder": "#02ED3D",
	"terminal.foreground": "#02ed3d"        
    },

```


To set custom color for GREY comments drop in these lines:

```
"editor.tokenColorCustomizations": {
  	"conmments": "#ff006f"
}


```

To fast access configuration file press:

```
CTRL + SHIFT + P
```

and select:

```
Preferences.Open User Settings (JSON)
```


After saving configuration you should get such look. 
<br>
Tweaking recolored active code line and changed cursors of editor and terminal console to red and green accordingly.
<br>
FYI, i'm using dark theme.

<div align="center">

<img src="/img/vscode-color/vscode-color.png" width="512px">
<hr>
<br>

</div>

<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>