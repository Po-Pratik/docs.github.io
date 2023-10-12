---
title: GSuite App Sync Setup With SafeSquid
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [gsuite]
---

# Problem Statement

When using the G Suite Sync App to configure a G Suite account on Microsoft Outlook (available for Windows 7 and Windows 10) with SafeSquid (SAB) installed and Proxy-Authentication enabled, there's an authentication issue preventing the syncing of the G Suite account.

# Solution

The G Suite application doesn't have its own proxy settings. Instead, it fetches proxy settings and proxy authentication credentials from the IE (Internet Explorer) browser, which are system-wide settings. The core problem is that when setting up MS Outlook using the G Suite Sync App, the application should connect to the Google Mail server to authenticate the user account. Using the proxy settings from IE, the G Suite Sync App uses the proxy server (SafeSquid-SWG) to connect to the Google Mail server. However, during this connection process, the application should send a `Proxy-Authorization` header with the proxy authentication credentials, but it fails to do so.

Further investigation showed that the G Suite Sync App does fetch proxy authentication credentials from the IE browser and can provide them during proxy authentication. This works on Windows 10, but fails on Windows 7.

To remedy this, the G Suite Sync App must be bypassed from Proxy-Authentication.

## STEP 1:
*Note*: In SafeSquid, applications can be identified using their `User-Agent`. Since the G Suite Application does not send any `User-Agent` during the connect request, it's considered an unidentified application.

- Identify the FQDN that the application is trying to visit and create a `Request-Type`.
  
  ![Go to configure page.png](Go%20to%20configure%20page.png)
  ![RequestTypeSlide1 (1).PNG](RequestTypeSlide1%20(1).PNG)
  ![RequestTypeSlide1 (2).PNG](RequestTypeSlide1%20(2).PNG)
  ![Gsuite1 (1).JPG](Gsuite1%20(1).JPG)

  After saving, it should look like this:

  ![Gsuite1 (2).JPG](Gsuite1%20(2).JPG)

## STEP 2: 

- Create a profile under the `Policies and Profiles` section (Restriction Policies > Access Profiles).

  ![Access-policies.jpg](Access-policies.jpg)
  ![Gsuite1 (3).JPG](Gsuite1%20(3).JPG)

  After saving, it should look like this:

  ![Gsuite1 (4).JPG](Gsuite1%20(4).JPG)
