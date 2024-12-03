---
title: HOW TO RUN LATEST VS CODE IN WINDOWS 7 X64
date: 2023-06-24
thumbnail: "img/vscode/vscode.png"
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

> UPDATED ON: 2024-07-05
<br>
> <b><font color="blue">v1.81.1 is a more recent version, which can be executed without any efforts</font></b> 
<br>
> <b><font color="red">v1.89 is a hacked <a href="https://github.com/Alex313031/codium/releases" target="_blank">[FINAL version]</a> for Windows 7 x64</font></b> 
<br>
So, Windows 7 users <u style="text-decoration:underline dotted; text-decoration-thickness: 4px; text-decoration-color: green">are pretty safe at this point</u> despite <u style="text-decoration:underline dotted; text-decoration-thickness: 4px; text-decoration-color: red">artificial restrictions of big corps</u>.

<br>

Usually i'm not feeling so delightful regarding microsoft modern programs, but this one is pretty good.
<br>
And of course they tried to artificially cripple it under "obsolete" Windows 7. 

Officially latest VS Code version to support Windows 7 is [[v1.70]](https://code.visualstudio.com/updates/v1_70) and it's dated back to July 2022.
<br>
Notwithstanding this statement you can easily run the most recent version of software [[v1.81.1]](https://update.code.visualstudio.com/1.81.1/win32-x64-archive/stable) [direct link], just by downloading **ZIP archive**, 
<br>
**MSI installer** has artificial stub to display dumb message that you are using not supported OS and blocking installation.

After you'll launch unpacked VS Code software will display one-time warning about Windows 7 EOL.
<br>
It can be totally ignored and muted by pressing cog gear and selecting **"DON'T SHOW AGAIN"**.
<br>

<div align="center">
<img src="/img/vscode/vscode-win7.png" width="384">
<hr>
<br>
</div>

However, there is one more closable EOL notification in the top bar of the program. 
<br>






Quick and dirty hack is to remove EOL banner code related to Windows 7 obsolescence.
<br>
[[Notepad++]](https://notepad-plus-plus.org/downloads) is recommended. Location of configuration file: 

```
C:\Users\USERNAME\AppData\Local\Programs\Microsoft VS Code\resources\app\out\vs\workbench\workbench.desktop.main.js 
```

Before any manipulations please make a backup copy:

```
workbench.desktop.main.js
``` 

Code to remove [triple click to select whole line]:

<font color="red">For v1.79.2:</font>

```
if(c.isWindows){const be=this.G.os.release.split("."),ke=be[0],me=be[1],Ie=new Map([["6",new Map([["1","Windows 7 / Windows Server 2008 R2"],["2","Windows 8 / Windows Server 2012"],["3","Windows 8.1 / Windows Server 2012 R2"]])]]);if(Ie.get(ke)?.has(me)){const Ee=(0,t.localize)(35,null,this.Q.nameLong,Ie.get(ke)?.get(me)),Re=[{label:(0,t.localize)(36,null),href:"https://aka.ms/vscode-faq-old-windows"}];this.bb.show({id:"windowseol.banner",message:Ee,ariaLabel:(0,t.localize)(37,null,Ee),actions:Re,icon:le.Codicon.warning}),this.t.prompt(w.Severity.Warning,Ee,[{label:(0,t.localize)(38,null),run:()=>this.J.open(I.URI.parse("https://aka.ms/vscode-faq-old-windows"))}],{neverShowAgain:{id:"windowseol",isSecondary:!0,scope:w.NeverShowAgainScope.APPLICATION},priority:w.NotificationPriority.URGENT,sticky:!0})}}if(c.isMacintosh){const be=this.G.os.release.split(".")[0],ke=new Map([["15","OS X El Capitan"],["16","macOS Sierra"]]);if(ke.has(be)){const me=(0,t.localize)(39,null,this.Q.nameLong,ke.get(be)),Ie=[{label:(0,t.localize)(40,null),href:"https://aka.ms/vscode-faq-old-macOS"}];this.bb.show({id:"macoseol.banner",message:me,ariaLabel:(0,t.localize)(41,null,me),actions:Ie,icon:le.Codicon.warning}),this.t.prompt(w.Severity.Warning,me,[{label:(0,t.localize)(42,null),run:()=>this.J.open(I.URI.parse("https://aka.ms/vscode-faq-old-macOS"))}],{neverShowAgain:{id:"macoseol",isSecondary:!0,scope:w.NeverShowAgainScope.APPLICATION},priority:w.NotificationPriority.URGENT,sticky:!0})}}
```

<font color="red">For v1.81.1:</font>

```
if(h.$i){const be=this.F.os.release.split("."),ve=be[0],ge=be[1],Se=new Map([["6",new Map([["1","Windows 7 / Windows Server 2008 R2"],["2","Windows 8 / Windows Server 2012"],["3","Windows 8.1 / Windows Server 2012 R2"]])]]);if(Se.get(ve)?.has(ge)){const Ee=(0,t.localize)(37,null,this.P.nameLong,Se.get(ve)?.get(ge)),De=[{label:(0,t.localize)(38,null),href:"https://aka.ms/vscode-faq-old-windows"}];this.$.show({id:"windowseol.banner",message:Ee,ariaLabel:(0,t.localize)(39,null,Ee),actions:De,icon:ce.$Aj.warning}),this.s.prompt(C.Severity.Warning,Ee,[{label:(0,t.localize)(40,null),run:()=>this.I.open(S.URI.parse("https://aka.ms/vscode-faq-old-windows"))}],{neverShowAgain:{id:"windowseol",isSecondary:!0,scope:C.NeverShowAgainScope.APPLICATION},priority:C.NotificationPriority.URGENT,sticky:!0})}}
```

After removal VS Code will complain about integrity of installation:
<br>

```
"Your Code installation appears to be corrupt. Please reinstall."
```
<br>

Just ignore it and reply with: 
```
Don't show again!
```
<br>

<div align="center">

Here is about screen confirming software version.

<img src="/img/vscode/181.png" width="384">
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