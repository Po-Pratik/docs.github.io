---
title: How to block virus uploads and downloads
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [block virus,virus protection]
---

## Client Scenario

You might download a file containing a virus during an e-commerce session. To protect your network from these threats, SvScan is the inbuilt module in SafeSquid that protects users against malware. ClamAV and ICAP are secondary servers provided along with SvScan. You can integrate your clamAV and ICAP servers also for virus scanning.

> **Note**: Make sure that SSL Inspection is enabled before using SvScan for scanning for malware. It enables the HTTPS sites also for scanning the malicious content.

## Prerequisites

  * HTTPS Inspection should be enabled in SafeSquid. If not enabled, you can check our document - [How to enable HTTPS Inspection](#).

## Access the SafeSquid User Interface

![SvScan (1).png](SvScan%20(1).png)

## Two Options to reach SvScan Section

### Go via Search Option or Go from side bar

![SvScan (2).PNG](SvScan%20(2).PNG)
![SvScan (3).png](SvScan%20(3).png)
![SvScan (4).png](SvScan%20(4).png)

## Ensure Section with Enabled TRUE

![SvScan (5).PNG](SvScan%20(5).PNG)

Follow the given link for more details [SvScan Documentation](http://docs.safesquid.com/index.php/SvScan)

## Download and Upload virus file to test

Go to [EICAR Test Site](http://www.eicar.org/) and download any virus file. You should get a blocked template.

![Download-virus.jpg](Download-virus.jpg)
