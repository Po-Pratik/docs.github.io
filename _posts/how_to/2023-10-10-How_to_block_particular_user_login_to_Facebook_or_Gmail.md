---
title: How to block particular user login to Facebook or Gmail
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [user control,access,control login,restrict access]
---

# Overview

In a corporation, you may need to restrict login usernames from Facebook and Gmail. Except for selected users, all others can log in to Facebook or Gmail.

# Prerequisites

  * HTTPS Inspection should be enabled in SafeSquid. If not enabled, you can check our document - [How to enable HTTPS Inspection](#).

# Access the SafeSquid User Interface

![LoginbSlide1 (1).png](LoginbSlide1%20(1).png)

# Go to Search

![LoginbSlide1 (2).png](LoginbSlide1%20(2).png)

# Search policy: "BLOCK PARTICULAR USER LOGIN"

![LoginbSlide1 (3).png](LoginbSlide1%20(3).png)

# Go to Content Modifier: Rewrite Policies

![LoginbSlide1 (4).png](LoginbSlide1%20(4).png)
![LoginbSlide1 (6).png](LoginbSlide1%20(6).png)

## Ensure Global Section with Enabled TRUE

![LoginbSlide1 (7).png](LoginbSlide1%20(7).png)
![LoginbSlide1 (8).png](LoginbSlide1%20(8).png)
![LoginbSlide1 (9).png](LoginbSlide1%20(9).png)

## Go to Rewrite Policies and make it Enable

![LoginbSlide1 (10).png](LoginbSlide1%20(10).png)
![LoginbSlide1 (11).png](LoginbSlide1%20(11).png)
![LoginbSlide1 (12).png](LoginbSlide1%20(12).png)

## Enter Username inside Pattern

![LoginbSlide1 (13).png](LoginbSlide1%20(13).png)
![LoginbSlide1 (14).png](LoginbSlide1%20(14).png)

# Search policy: "BLOCK PARTICULAR USER LOGIN" again

![LoginbSlide1 (5).png](LoginbSlide1%20(5).png)

# Go to Access Profiles to Enable

![LoginbSlide1 (15).png](LoginbSlide1%20(15).png)
![LoginbSlide1 (16).png](LoginbSlide1%20(16).png)
![LoginbSlide1 (17).png](LoginbSlide1%20(17).png)
![LoginbSlide1 (18).png](LoginbSlide1%20(18).png)

# To test

## Go to Facebook and Login

Try logging in to your Facebook account. It will show you the below page:

![Blocklogin particularuser testing1.jpg](Blocklogin%20particularuser%20testing1.jpg)

## Go to Gmail and Login

Try logging in to your Gmail account. It will show you the below page:

![Blocklogin particularuser testing2.jpg](Blocklogin%20particularuser%20testing2.jpg)
