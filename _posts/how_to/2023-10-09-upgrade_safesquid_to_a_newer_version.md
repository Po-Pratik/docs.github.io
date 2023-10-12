---
title: How To Upgrade SafeSquid To A Newer Version using SafeSquid's web console
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [HowTo]
---

# Overview

SafeSquid SWG upgrade is a newer version of the SafeSquid that offers a significant change or major improvement over your current version. Upgrade your SafeSquid to the latest version which may consists of bugfixes and enhancements. When you upload latest tarball of SafeSquid SWG from WebGUI monit service will automatically restart the SafeSquid service.

# Prerequisites

* Monit service should be running and started on your SafeSquid server, you can check it by using below command from your SafeSquid server

```bash
pidof monit
```

* If you did not find pid of monit, run below command to Start the Monit service

```bash
/etc/init.d/monit start
``` 

* The partition size of /tmp/safesquid used must be less than 4%, you can check it by using below command

```bash
df -kh
```

After executing the command last line of the output will be similar as shown below
```
/dev/ram1        62M  1.3M   58M   3% /tmp/safesquid
```

Check the highlighted number which shows the actual usage, if it is greater than 4%, then remove the files from the folder /tmp/safesquid

You can remove files from /tmp/safesquid by going to that folder location using the command :   
```
cd /tmp/safesquid
```

Further delete all the files from the folder by using the command :    rm -rf * 

 
# Access the SafeSquid User Interface
UpgSlide1.png
# Go to Support Page
UpgSlide2.png
	 
# Go to Upgradation

**Note:** Download the latest SafeSquid SWG tarball from here and save into your machine. 
UpgSlide3.png
#  Select New tarball

Select the latest SafeSquid tarball downloaded and saved in your machine before.
UpgSlide4.png

 
UpgSlide5.png
 
UpgSlide6.png
  	 
UpgSlide6.png
   
  Click on upload button to upload new tar file.
UpgSlide7.png
# Testing Upgradation

You can see upgraded version number of SafeSquid SWG at the bottom right corner of interface.
UpgradationtarballSlide9.png