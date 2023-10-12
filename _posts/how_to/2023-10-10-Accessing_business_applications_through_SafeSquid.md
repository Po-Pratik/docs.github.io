---
title: Accessing business applications through SafeSquid
date: 2023-10-07 16:00:00 +05:30
categories: [development]
tags: [development]
---

# overview

There have been several instances where it has been reported that certain applications which the organizations use doesn't work through SafeSquid. This article describes a generalized way of identifying what's wrong with the application and solving it.

There are more than one reasons because of which the application may not work through SafeSquid. They can be listed as:

# Blocked URLs by SafeSquid
The applications may have certain URLs which are getting blocked by SafeSquid. You need to allow those URLs by creating policies so that the application works properly. 

To identify whether URLs are getting blocked, you need to carefully observe the extended log of SafeSquid by verifying if the status code is '403' (which means blocked) for any of the requests sent by the application. 

To view the logs, you can run the following command by taking the SSH access of the SafeSquid server:

```bash
tail -F /var/log/safesquid/extended/extended.log | grep "192.168.0.17" | grep '451'
```