---
title: Do Bandwidth Management With Limits
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [bandwith management]
---

# Overview

SafeSquid's Limits feature allows administrators to set bandwidth limits for Download size, Upload size, and Download speed. This guide provides steps to configure these settings.

# Prerequisites

For downloading files from HTTPS websites, ensure that HTTPS Inspection in SafeSquid is enabled.

# Access The SafeSquid User Interface

Navigate to: `Go to configure --> Restriction policies --> Speed Limits`

The main interface should resemble the following images:

![Download Rate 1](Downloadrate1.png)
![Download Rate 2](Downloadrate2.png)
![Download Rate 3](Downloadrate3.png)
![Download Rate 4](Downloadrate4.png)
![Download Rate 5](Downloadrate5.png)

# How Default Entries work

- The first entry establishes the download speed at which users are permitted to download files.
    - [See More about Setup Download Speed At which the files need to download](#)
- The second entry sets a limit on the download size. Files exceeding the download transfer limit will be blocked by SafeSquid.
    - [See More about Setup Maximum limit on the Download size](#)
- The third entry defines the upload size limit. If the file size being uploaded exceeds the upload transfer limit, SafeSquid will block the upload.
    - [See More about Setup Maximum limit on the Upload size](#)
