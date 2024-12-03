---
title: HOW TO FLASH ROOTED ANDROID 8 ON SONY XPERIA XZ1 COMPACT IN WINDOWS 7 ENVIRONMENT
date: 2023-04-05
thumbnail: "img/xz1-a8-root/header.png"
categories:
  - "Hardware"
  - "Vintage"
  - "Technology"
  - "Software"
  - "FAQ"
  - "Windows 7"
  - "Android 8"
tags:	
  - "Sony"
  - "Xperia" 
  - "Xz1"

weight: 1
---

<br>

> **UPDATED ON: 2023-04-20** Important update, substantial refactoring, many errors fixed

## ▒ PREFACE WORDS

Following instruction is dedicated to flashing stock Android 8.0 firmware for Russian region, but almost all information can be applied to USA or any other region firmware. So, no restrictions here.

Remember that all commands and programs should be executed with admin privileges and your account must have administrator rights!
<br>
If something goes wrong for some reason be sure to check [[TROUBLESHOOTING]](#-troubleshooting) section!

[[WHY ANDROID 8.0?]](https://trackerninja.codeberg.page/post/android-8-reasons-why-i-use-it-in-2023)

<hr>

## ▒ COPYING NEEDED FILES TO SD-CARD

To make process more convenient copy in advance following files:
* Custom **TWRP recovery** to flash root access and fix camera /// **<font color="#00ec00">twrp-3.5.2_9-0-lilac.img</font>** 
<br>
[copy to **ADB** folder on your computer]
* **Magisk** application to gain root /// **<font color="#00ec00">Magisk-v20.1.zip</font>** 
<br>
[copy to sd-card, of course you can copy to internal storage too, but files will be lost after flashing firmware and you'll have to copy them over again]
* **DRM fix** to restore Camera functionality /// **<font color="#00ec00">DRM-FIX.zip</font>** 
<br>
[copy to sd-card, of course you can copy to internal storage too, but files will be lost after flashing firmware and you'll have to copy them over again]

[[ONE-PLACE & ONE FILE DOWNLOAD LINK]](https://mega.nz/file/LxQzwKQA#-eX45SsMG4UXKOUmEWd77H6NwvZJm4px-xbkBxP03NM)

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>

## ▒ INSTALLING FLASHTOOL & DRIVERS

It is a known fact that newer Sony phones should be flashed by [[Newflasher]](https://forum.xda-developers.com/t/tool-newflasher-xperia-command-line-flasher.3619426).
<br>
But today we are talking about vintage phone, so [[Flashtool]](https://github.com/Androxyde/Flashtool) is preferred.

I recommend to use version somewhere around **0.9.27 - 0.9.33**. 
<br>
Below 0.9.27 XZ1 Compact is not supported or supported badly.
<br>
Above 0.9.33 flashing is unreliably awful. Version **<font color="#00ec00">0.9.33</font>** can be downloaded [[HERE]](https://mega.nz/file/DhZ0xSzS#vJ17cj2PKmra98urp75XERSv1O0Q3aUAfpSL8h4-0Cw).

Flashtool distribution already comes with Xperia drivers. 
<br>
In **<font color="#00ec00">Drivers</font>** folder you’ll find **<font color="#00ec00">Flashtool-drivers.exe</font>**.

* Execute it with admin privileges, also make sure that Vista compatibility is turned on
* Check the following drivers:
[x] <font color="#00ec00">Flashmode Drivers</font>
[x] <font color="#00ec00">Fastboot Drivers</font>
* Agree to install **<font color="#00ec00">Sony Mobile Software Update</font>**
* Confirm google **<font color="#00ec00">Android USB driver</font>**

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>

## █ UNLOCKING BOOT LOADER

First thing you’ll need to do is to unlock boot loader of the phone.

To get the idea about can you unlock it or not you can by means of phone dialing with not-so simple combination: 

```
*#*#7378423#*#*
```
**<font color="#00ec00">Service Info ► Configuration ► Rooting Status</font>**
<br>
In **<font color="#00ec00">Bootloader unlock allowed</font>** section you should have **<font color="#00ec00">Yes</font>**.  Otherwise unlocking is not possible. 
<br>
If unlocking is possible write down **<font color="#00ec00">IMEI</font>** of your phone, which you can find right in this section too.

**<font color="#00ec00">Settings ► System ► About Phone ► Build Number ► Tap 5-6 times</font>** to enable developer settings
<br>
**<font color="#00ec00">Settings ► System ► Developer options ► OEM unlocking ► ON</font>**
<br>
**<font color="#00ec00">Settings ► System ► Developer options ► Debugging ► Debugging USB ► ON</font>**

If **<font color="#00ec00">OEM unlocking</font>** option is grayed out:

* **<font color="#00ec00">turn WiFi on</font>** to connect to internet 
<br>
* **turn off automatic date & time zone and set them manually**: 


**<font color="#00ec00">Settings ► System Date & Time ► Automatic date & time ► OFF</font>**
<br>
**<font color="#00ec00">Settings ► System Date & Time ► Automatic time zone ► OFF</font>**

Then reboot device and check again for availability of OEM unlocking option.

* Visit [[developer.sonymobile.com]](https://developer.sony.com/develop/open-devices/get-started/unlock-bootloader) 
* Select **<font color="#00ec00">Xperia XZ1 Compact</font>** in device dropdown list
* Enter previously copied device **<font color="#00ec00">IMEI number</font>**
* Press sumbit to get personal code
* [[Grab ADB tools]](https://mega.nz/file/34oFESoK#VqaU2IsMytwVQLoHH08BZzKSOtDzym5rjzK4cpYmDgg) version r31.0.3 is confirmed to work flawlessly 
* Extract tools to something like **<font color="#00ec00">C:\ADB</font>**
* Turn off smartphone
* Press **<font color="#00ec00">VOLUME UP</font>** button and **<font color="#00ec00">holding it down</font>** plug USB cable to phone
* Blue led will indicate that you are **<font color="#00ec00">fastboot mode</font>**, however screen will stay back
* Make sure that you don’t have unknown devices with question mark in the device manager. 
<br>
If **<font color="#00ec00">ADB interface</font>** is installed not correctly you should install it by force. 
<br>
First thing to try is [[Leshcat driver]](https://mega.nz/file/uhgEBKbY#Rl1Ma5eDum0ZUqJVPrwykuFXUm2_GOGJ2MeZlO_OYSo). Still not working?  Try [[stock Sony 1.01 driver]](https://mega.nz/file/LxhkCKyb#PfyG4w8Te9XYGz_OBQa580n6RjGfEgbsrjS7sVMcdh4). 
<br>
One more [[classic driver]](https://mega.nz/file/v9xHiDSD#5agYR7t6FvOLb2CqRy2z8VsAIx7fPfQ-ntieuNmCVqc). Last resort is to use [[Snappy driver pack]](https://sdi-tool.org/download).
* After you convinced that ADB interface is installed correctly open command line **<font color="#00ec00">[WIN] + [R]</font>**

```
cmd
```
Change to tools directory:
```
cd c:\adb
```

Check connected devices
```
fastboot devices
```
If everything is fine you should see something like:

```
your-device-serial-number fastboot
```

To unlock phone execute the following:
```
fastboot oem unlock 0x****************
```
where 

```
0x**************** 
```
....is a number from Sony website.

**<font color="red">Warning! Case of letters matters!</font>**


```
143n56b09
```
is not the same as:

```
143N56B09
```

After completion ADB should return:

```
OKAY!
```
Unplug USB cable, smartphone will turn off. Congrats, now you have unlocked device!

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>


## ▒ PREPARING FIRMWARE 

Latest **<font color="#00ec00">Android 8.0</font>** version is dated back to **<font color="#00ec00">2018/09/01</font>**.
Marked as: **<font color="#00ec00">47.1.A.16.20</font>**.
<br>
**<font color="red">Everything above contain unwanted Neural API to collect your personal data and sell it to third-parties.</font>**

In my case it will be firmware for Russian region [English language is fully supported].
<br>
[[Download firmware]](https://drive.google.com/drive/folders/1hOs-CCuQnEePjkakK_HZ313_OPfzCFEU) in Flashtool FTF format.
<br>
Naming should look like this: **14_G8441_47.1.A.16.20_1310-5279_R9B.ftf**

Good place to download firmwares for other regions is [[AndroidFileHost]](https://androidfilehost.com/?w=files&flid=235027).
<br>
List of XZ1 Compact develeopers can be found [[HERE]](https://androidfilehost.com/?w=developers&did=2983).


**<font color="red">Warning! If you do not follow provided instructions you probably end up with something like:</font>**

```
Unable to read TA unit 10021 error=-22 hex (00002725)
```
....during flashing process, at least if you are using **Flashtool**.

**So, obey and do the things as they should be done.**

* Rename firmware extension from **<font color="#00ec00">FTF</font>** to **<font color="#00ec00">ZIP</font>**
* Open archive in 7-Zip or WinRar
* Extract file: **<font color="#00ec00">boot_delivery.xml</font>** to your desktop
* Delete **<font color="#00ec00">boot_delivery.xml</font>** directly in arhive in your compression utility [software should do repacking]
* Navigate to **<font color="#00ec00">boot</font>**  folder in your compression utility
* Drag’n’drop previously extracted **<font color="#00ec00">boot_delivery.xml</font>** from desktop to **<font color="#00ec00">boot</font>** folder in your archiver [software will repack things]
* Rename back firmware extension from **<font color="#00ec00">ZIP</font>** to **<font color="#00ec00">FTF</font>**
* Launch **<font color="#00ec00">Flashtool</font>** at least once, then exit program
* Put newly cooked firmware to **<font color="#00ec00">C:\Users\USER_NAME\\.flashTool\firmwares</font>**

You have prepared firmware and ready for hassle-free flashing.

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>

## █ FLASHING DEVICE

* Execute Flashtool with admin privileges
* Click lightning icon and select **<font color="#00ec00">Flashmode</font>** [now you should see Sony Xperia XZ1 Compact firmware]
* Click triple times on drop-down arrows
* Select **<font color="red">47.1.A.16.20</font>** to see **<font color="#00ec00">CONTENT</font>** section filled with files
* Mark check-boxes in **<font color="#00ec00">SIN</font>** section:  [x] APPSLOG [x] USERDATA
* Hit **<font color="#00ec00">FLASH</font>** button to begin process
* Then **<font color="#00ec00">Flashtool</font>** will ask you to: 
	* turn off your phone
	* press **<font color="#00ec00">VOLUME DOWN</font>** button
	* and after that **<font color="#00ec00">plug USB cable</font>**


**<font color="#00ec00">Green LED</font>** on the device will indicate that phone is ready for flashing.
<br>
After that flasher will ask a question:

```
Those data are not in the FSC script and will be skipped:
RESET-NON-SECURE-ADB
Do you want to continue?
```
* Answer **<font color="#00ec00">YES</font>** to continue.
* Power down device after flashing to check newly installed operating system

If everything is correct application will begin flashing.

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>


## █ FLASHING TWRP CUSTOM RECOVERY

Side-loading TWRP recovery is a mandatory step to gain easy root access later on.
<br>
TWRP can be side-loaded only to unlocked smartphone!

* Extract from previously downloaded archive file with the name **<font color="#00ec00">twrp-3.5.2_9-0-lilac.img</font>** and put it into **<font color="#00ec00">ADB</font>** tools folder [for me it is **<font color="#00ec00">C:\ADB</font>**]
* Turn off smartphone
* Hold down **<font color="#00ec00">VOLUME UP</font>** button, plug **<font color="#00ec00">USB cable</font>**
* As soon as you see blue led on smartphone release **<font color="#00ec00">VOLUME UP</font>** [you are in Fastboot mode now]
* Open command line **<font color="#00ec00">[WIN] + [R]</font>**

```
cmd
```
Change to tools directory:
```
cd c:\adb
```

Check connected devices:
```
fastboot devices
```
If everything is fine you should see something like:

```
your-device-serial-number fastboot
```
Flash custom TWRP recovery:

```
fastboot flash recovery twrp-3.5.2_9-0-lilac.img
```
After that you should see **<font color="#00ec00">double OK</font>** and exclamation **<font color="#00ec00">FINISHED!</font>**
<br>
**<font color="#00ec00">Unplug USB cable</font>**, led light and smartphone will shutdown.

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>


## █ ROOTING DEVICE

Many of you understand that if you want to control your device fully it should be rooted.
We’ll do it with the help of previously installed TWRP recovery.

* Turn off smartphone
* Enter TWRP recovery: hold simultaneously **<font color="#00ec00">POWER</font>** and **<font color="#00ec00">VOLUME DOWN</font>** buttons
* After one-time vibration release **<font color="#00ec00">POWER</font>** button
* On appearance of blue Teamwin logo release **<font color="#00ec00">VOLUME DOWN</font>** button
* **<font color="#00ec00">Swipe to allow modifications</font>**
* Tap **<font color="#00ec00">INSTALL</font>** ► select previously copied: 
<br>
**<font color="#00ec00">Magisk-v20.1.zip</font>** ► **<font color="#00ec00">Swipe to confirm Flash</font>**
* Exit to starting menu
* Reboot device by selecting: **<font color="#00ec00">Reboot ► System</font>** 

One more congrats, you are a fully fledged device owner!

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>

## █ RESTORING ORIGINAL SONY CAMERA APP

If you have black screen in original Sony camera application do the following:

* Turn off smartphone
* Enter **<font color="#00ec00">TWRP recovery</font>**: hold simultaneously **<font color="#00ec00">POWER</font>** and **<font color="#00ec00">VOLUME DOWN</font>** buttons
* After one-time vibration release **<font color="#00ec00">POWER</font>** button
* On appearance of blue **<font color="#00ec00">Teamwin logo</font>** release **<font color="#00ec00">VOLUME DOWN</font>** button
* Tap **<font color="#00ec00">INSTALL</font>** ► select previously copied: 
<br>
**<font color="#00ec00">DRM-FIX.zip</font>** ► **<font color="#00ec00">Swipe to confirm Flash</font>**
* Exit to starting menu
* Reboot device by selecting: **<font color="#00ec00">Reboot ► System</font>** 

Camera should be fixed now.

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>

## █ TROUBLESHOOTING

* Before doin' things unload all unneeded software from memory, start with a **<font color="#00ec00">clean desktop</font>**
* During flashing **<font color="#00ec00">disable all antiviruses, firewalls and system protection utilities</font>**
* Always use **<font color="#00ec00">USB port on the back of your computer</font>**, in case of failure try **<font color="#00ec00">different USB ports</font>**
* Use **<font color="#00ec00">original USB cable</font>**, if something is not working try to **<font color="#00ec00">use another cable</font>**
* Still no luck? Try to use **<font color="#00ec00">generic USB 2.0 ports</font>** instead of **<font color="blue">blue USB 3.0 ports</font>**

For those of you who like to mess around with many devices at the same time, you can easily run into troubles like corrupted system files and registry branches.
In such case i recommend to do the following things:  

* **<font color="#00ec00">Uninstall all</font>** phone drivers from **<font color="#00ec00">device manager</font>**
* **<font color="#00ec00">Uninstall all</font>** mobile drivers from **<font color="#00ec00">control panel</font>**
* Do one pass of [[CCleaner]](https://mega.nz/file/OtQgzbgb#oiCKS5GsC09enDdI8scWVBrqMuceT_05-mk0Ne00Mz0)
* Do one pass of [[DISM++]](https://github.com/Chuyu-Team/Dism-Multi-language/releases)
* Reboot machine
* Use excellent [[USB DVIEW]](https://www.nirsoft.net/utils/usb_devices_view.html) to **<font color="#00ec00">remove traces of previously installed USB devices</font>**
* Right after that run [[USB OBLIVION]](https://sourceforge.net/projects/usboblivion/files) to **<font color="#00ec00">finalize cleanup of USB configuration</font>**
* Reboot machine / Try again

As a last resort **<font color="#00ec00">turn off signature protection of installed drivers</font>**: 
<br>
Hit **[F8]** during system startup and select **<font color="#00ec00">Disable driver signature enforcement</font>**. 
<br>
**<font color="red">Warning!</font>** In some motherboards **[F8]** execute boot order menu, in such case hit **[F8] again right after you select appropriate disk for booting**.
<br>
<br>
If you end up with **<font color="#00ec00">not working Sony camera</font>** you’ve messed up DRM-keys, look through the article for solution.
<br>
Nevertheless I prefer to use [[OpenCamera]](https://f-droid.org/en/packages/net.sourceforge.opencamera).

<hr>

<p style="text-align:right;"><a href="#top">▲ BACK TO TOP</a></p>


## ▒ RELEVANT STUFF

Make sure to [[install additional software]](https://trackerninja.codeberg.page/post/list-of-android-applications-which-are-telemetry-free) like firewall, proper browsers, navigational maps, or whatever you need. 
<br>
Privacy tweaks [[here]](https://trackerninja.codeberg.page/post/sony-xz1-compact-stripping-down-bloatware-plus-some-privacy-tweaks). Other Android related things [[here]](https://trackerninja.codeberg.page/tags/android).

Hope that tutorial will be useful piece of information.
<br>
If you'll notice any inconsistencies or errors please [[report me back]](https://trackerninja.codeberg.page/menu/_about/#-contacts).


<br>
<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>