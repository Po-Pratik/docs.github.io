---
title: Block specific website through SafeSquid.
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [manage category]
---

# Client Scenario

Stark tech has 200 employees. Stark tech has distributed all 200 employees into different 'User Groups.' Now, Stark tech wants to block specific websites for the defined 'User Group,' say 'MANAGERS.'

Stark tech's challenges are:

1. All Managers should not be allowed to access specific websites, e.g., Facebook.com. When managers access those websites, they should get a blocked template.

2. Suppose websites like 'google' (search engine) are blocked for defined User groups. The users of that user group should not be able to access google.com, google.co.in, google.co.uk.

# Solution

The SafeSquid Custom Category feature is a solution proposed for Stark tech. The solution is to 'blacklist' mentioned websites from the Custom Category and apply the 'Do not bypass' action to them. Suppose you want to block 'facebook.com.'

Create Custom Category: blacklist and apply Action: Do not bypass so that you should get a block template.

**Note**:

- If you blacklist 'google,' it will match google.com, google.co.in, google.co.uk. But if you blacklist 'google.com,' then google.co.in will not match.

## Prerequisites

HTTPS Inspection should be enabled in SafeSquid. If not enabled, you can check our document - [How to enable HTTPS Inspection](link-to-enable-https-inspection).

**Note**: Even though HTTPS inspection is disabled, it will work. But it will not show the block template.

- Enable SScore as TRUE, which is under application setup (By default, SScore should be enabled as TRUE)

Access SafeSquid interface

Go to the configure page

![BlacklistSlide1 (1).PNG](BlacklistSlide1%20(1).PNG)

Go to Categorize Web-Sites under Custom Settings

![BlacklistSlide1 (2).PNG](BlacklistSlide1%20(2).PNG)

![BlacklistSlide1 (3).PNG](BlacklistSlide1%20(3).PNG)
![BlacklistSlide1 (4).PNG](BlacklistSlide1%20(4).PNG)

Add your website to the custom category

![BlacklistSlide1 (5).PNG](BlacklistSlide1%20(5).PNG)

![BlacklistSlide1 (7).PNG](BlacklistSlide1%20(7).PNG)

Go to Access Profiles in Restriction Policies

![BlacklistSlide1 (8).PNG](BlacklistSlide1%20(8).PNG)
![BlacklistSlide1 (9).PNG](BlacklistSlide1%20(9).PNG)
![BlacklistSlide1 (10).PNG](BlacklistSlide1%20(10).PNG)
![BlacklistSlide1 (11).PNG](BlacklistSlide1%20(11).PNG)
![BlacklistSlide1 (12).PNG](BlacklistSlide1%20(12).PNG)
![BlacklistSlide1 (13).PNG](BlacklistSlide1%20(13).PNG)
![BlacklistSlide1 (14).PNG](BlacklistSlide1%20(14).PNG)
![BlacklistSlide1 (15).PNG](BlacklistSlide1%20(15).PNG)
![BlacklistSlide1 (16).PNG](BlacklistSlide1%20(16).PNG)
![BlacklistSlide1 (17).PNG](BlacklistSlide1%20(17).PNG)
![BlacklistSlide1 (18).PNG](BlacklistSlide1%20(18).PNG)
![BlacklistSlide1 (19).PNG](BlacklistSlide1%20(19).PNG)
