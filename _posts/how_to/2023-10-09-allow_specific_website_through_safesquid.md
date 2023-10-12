---
title: Allow specific website through SafeSquid.
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [manage category]
---

# Client Scenario

Stark tech has 200 employees. Stark tech distributes all 200 employees into different 'User Groups.' Now, Stark tech has blocked all websites for the defined 'User Group,' say 'General Users.'

Stark tech's challenges are:

1. General users should be allowed to access specific websites, namely, www.safesquid.com, etc. When users access those websites, they get a block template. General users should not be able to access anything else apart from the mentioned websites.

2. Suppose websites like 'google' are blocked for defined User groups. The users of that user group should be able to access google.com, google.co.in, google.co.uk.

# Solution

The SafeSquid Custom Category feature is a solution proposed for Stark tech. The solution is to 'white list' mentioned websites (safesquid.com) from the Custom Category and apply the 'allow' action to them. Suppose websites like 'google' need to be allowed for defined User groups; white list the 'google' website from the Custom Category feature of SafeSquid and apply the 'allow' action to it so that you will get access to both google.com, google.co.in, and google.co.uk.

**Note**: If you white list 'google,' it will match google.com, google.co.in, google.co.uk, but if you white list 'google.com,' then google.co.in will not match.

## Prerequisites

HTTPS Inspection should be enabled in SafeSquid. If not enabled, you can check our document - [How to enable HTTPS Inspection](link-to-enable-https-inspection).

![AllowcustomcategorySlide1 (1).PNG](AllowcustomcategorySlide1%20(1).PNG)

Access SafeSquid interface

Go to the configure page

![AllowsitescategorySlide1 (2).PNG](AllowsitescategorySlide1%20(2).PNG)

Go to Custom Settings: Categorize Web-sites

![AllowcustomcategorySlide1 (3).PNG](AllowcustomcategorySlide1%20(3).PNG)

Add your website to the custom category

![AllowcustomcategorySlide1 (4).PNG](AllowcustomcategorySlide1%20(4).PNG)
![AllowsitescategorySlide1 (5).PNG](AllowsitescategorySlide1%20(5).PNG)
![AllowcustomcategorySlide1 (6).PNG](AllowcustomcategorySlide1%20(6).PNG)
![AllowcustomcategorySlide1 (7).PNG](AllowcustomcategorySlide1%20(7).PNG)
![AllowcustomcategorySlide1 (8).PNG](AllowcustomcategorySlide1%20(8).PNG)

Go to Search

![AllowcustomcategorySlide1 (9).PNG](AllowcustomcategorySlide1%20(9).PNG)

Search policy: "WHITELIST"

![AllowcustomcategorySlide1 (10).PNG](AllowcustomcategorySlide1%20(10).PNG)
![AllowcustomcategorySlide1 (11).PNG](AllowcustomcategorySlide1%20(11).PNG)
![AllowcustomcategorySlide1 (12).PNG](AllowcustomcategorySlide1%20(12).PNG)
![AllowcustomcategorySlide1 (13).PNG](AllowcustomcategorySlide1%20(13).PNG)
![AllowcustomcategorySlide1 (14).PNG](AllowcustomcategorySlide1%20(14).PNG)
![AllowcustomcategorySlide1 (15).PNG](AllowcustomcategorySlide1%20(15).PNG)
