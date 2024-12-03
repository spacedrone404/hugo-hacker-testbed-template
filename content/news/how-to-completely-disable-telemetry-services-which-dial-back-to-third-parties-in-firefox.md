---
title: HOW TO COMPLETELY DISABLE TELEMETRY SERVICES WHICH DIAL BACK TO THIRD-PARTIES IN FIREFOX
date: 2023-08-04
thumbnail: "img/ff-telemetry-off.png"
categories:	
- "Technology"
- "Internet"
- "FAQ"
- "Lists"
- "Windows 7"
- "Tweaks"
- "Hacks"
- "Security"
- "Privacy"

tags:
- "Firefox"
- "Browser"


weight: 1

---

> **UPDATED ON: 2023-09-06**
<br>
Some new parameters were added.

Note that by default all [[Nightly versions]](https://trackerninja.codeberg.page/post/windows-7-x64-executes-firefox-117-nightly-version-without-any-issues) of Firefox are sending back telemetry to third-parties in extensive manner.
<br>
So, to disable such malicious actions besides turning off telemetry settings via standard GUI options:


```
about:preferences#privacy 
```

You'll need to use good old: 


```
about:config 
```

To change to:

```
FALSE
```

...or create following parameters in software registry:

```
toolkit.telemetry.archive.enabled
toolkit.telemetry.enabled
toolkit.telemetry.unified
toolkit.telemetry.unifiedIsOptIn
toolkit.telemetry.bhrPing.enabled
toolkit.telemetry.firstShutdownPing.enabled
toolkit.telemetry.hybridContent.enabled
toolkit.telemetry.newProfilePing.enabled
toolkit.telemetry.reportingpolicy.firstRun 
toolkit.telemetry.shutdownPingSender.enabled
toolkit.telemetry.updatePing.enabled
browser.newtabpage.activity-stream.feeds.telemetry
browser.newtabpage.activity-stream.telemetry
browser.ping-centre.telemetry
devtools.onboarding.telemetry.logged
datareporting.healthreport.uploadEnabled 
datareporting.policy.dataSubmissionEnabled 
experiments.activeExperiment
experiments.enabled
experiments.supported
network.allow-experiments

```

**<font color="red">!Note</font>** **toolkit.telemetry.enabled** can't be tweaked in Nightly versions of browser.

Then set to:

```
TRUE
```
these ones:

```
toolkit.telemetry.rejected
toolkit.telemetry.coverage.opt-out
datareporting.sessions.current.clean  
```
and finally tweak last two ones:

```
toolkit.telemetry.server = CLEAR VALUE
browser.newtabpage.activity-stream.telemetry.structuredIngestion.endpoint = CLEAR VALUE
toolkit.telemetry.prompted = 2
```

Reboot browser to apply changes.

<br>

**<font color="red">!BONUS:</font>** Do you know that [[SeaMonkey]](https://www.seamonkey-project.org/releases) browser doesn't have any of those nasty parameters?
<br>
For android systems i can recommend [[Mull]](https://f-droid.org/packages/us.spotco.fennec_dos) & [[IceRaven]](https://github.com/fork-maintainers/iceraven-browser/releases) browsers. 
<br>
They are shipped with settings that almost do not require any tweaking,

<br>

<hr>

<br>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>