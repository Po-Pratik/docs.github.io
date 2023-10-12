---
title: Bypass HTTPS Inspection by using Request Types.
date: 2023-10-07 16:00:00 +05:30
categories: [How To,HTTPS Inspection]
tags: [https inspection,bypass https inspection,request types]
---

# Business Challenge

The HTTPS inspection Bypass option enables you to define specific websites that are not subject to decryption as they flow through the proxy. Some websites may include personal identification information that should not be decrypted. In order to avoid liability for inspecting this type of information, you may want to specify some or all of these sites for decryption bypass. The selected sites will not be decrypted even if the category or categories that the sites belong to are selected for SSL analysis.

## To bypass HTTPS Inspection enabled SafeSquid default configuration

### Access the SafeSquid User Interface

![Slide1.PNG](Slide1.PNG)
![Slide2.PNG](Slide2.PNG)

Search policy: "BYPASS SSL INSPECTION" to Search

![Slide3.PNG](Slide3.PNG)

Edit policy to Enable as TRUE (Inspection Policies)

![Slide4.PNG](Slide4.PNG)
![Slide5.PNG](Slide5.PNG)
![Slide6.PNG](Slide6.PNG)

Edit policies and profiles to Enable as TRUE

![Slide7.PNG](Slide7.PNG)

### How to create a new policy to bypass HTTPS Inspection

![Slide8.PNG](Slide8.PNG)

Go to Request Types

![Slide9.PNG](Slide9.PNG)

![Slide10.PNG](Slide10.PNG)
![Slide11.PNG](Slide11.PNG)
![Slide12.PNG](Slide12.PNG)
![Slide13.PNG](Slide13.PNG)

Go to Access Policies

![Slide14.PNG](Slide14.PNG)
![Slide15.PNG](Slide15.PNG)
![Slide16.PNG](Slide16.PNG)

**Note**: Configure Proxy settings in the dropbox and upload/download files to validate the working
