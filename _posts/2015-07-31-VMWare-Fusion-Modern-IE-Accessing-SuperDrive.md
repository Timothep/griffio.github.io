---
layout: post
title: How to allow VMWare Fusion 6 with a Modern.IE XP image access to the SuperDrive in OSX
category: tip
tags: vmware
published: true
summary: Fixing VMWare Fusion 6 with Modern IE XP image accessing SuperDrive
---

After downloading the "IE8 - WinXP" VmWare image from [modern.ie](http://dev.modern.ie/tools/vms/mac/)
the SuperDrive CD-ROM on the Apple host is not accessible. 

The notification message is:

![legacy emulation](https://raw.githubusercontent.com/griffio/griffio.github.io/master/public/legacy-emulation.png)

"Your VM is configured to use legacy emulation but this host does not support it.
Try configuring this virtual machine's CDROM to not use legacy emulation."

**Steps to fix.**

Ideally this should be done immediately after extracting the image from the download.

To avoid a corrupted vmx file read the tips here. [http://kb.vmware.com](http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1014782).

Make sure the VMWare Fusion application is closed in the OSX dock.

Make a backup of the current vmx file located in "IE8 - WinXP.vmwarevm" ("Show Package Contents") 

Preferably using Vim or other commandline editor that won't change any whitespaces or quotes.

edit "IE8 - WinXP.vmx"

Locate the cd-rom ide device section

Change from "atapi-cdrom"

~~~
ide1:0.deviceType = "atapi-cdrom"
~~~

Change to "cdrom-raw"

~~~
ide1:0.deviceType = "cdrom-raw"
~~~

Save the changes and exit.

Double click the image "IE8 - WinXP" as normal from Finder.

It is not necessary to update the vm image when prompted or update vmware tools.

Once this Windows image has booted the CD-ROM can be accessed by using the normal connect to CD/DVD (IDE) option in the menu.

It may take a few seconds to initialize and see the CD-ROM is accessible in MyComputer.

The next time the image is started the CD-ROM will connect automatically to the SuperDrive.
