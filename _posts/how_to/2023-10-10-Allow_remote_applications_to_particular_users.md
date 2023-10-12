---
title: Allow remote applications to particular users
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [remote app]
---

# Overview

For security reasons, all traffic to users has been blocked. However, there may be certain users within the network who need access to remote applications. SafeSquid can be configured to allow these specific users to access remote applications.

# How it works?

When a user attempts to access a remote application software, SafeSquid will first verify the user's permissions. If the user is granted access to the remote application, SafeSquid will then cross-check the user-agent or website added in the `Custom Settings > Request types` section. Access will only be provided if both the user and application permissions match. For example, if user Samidha is permitted to access the xyz application but attempts to access the abc application, SafeSquid will deny her request.

# How to Allow Remote Applications?

## Allow anydesk

[Tutorial or steps to allow anydesk would be here.]

## How to create a policy without Application Signature

Remote applications are already categorized in SafeSquid's Application Signatures. To allow a remote application:

1. First, check if the application is categorized under the default Application Signatures.
2. If the application isn't categorized:
    * Identify the User-agent using SafeSquid's extended logs or another traffic capturing tool.
    * Add the User-agent or websites to the `Request Types`.
3. Associate the created user group and Request Type in `Access Profiles` and decide whether to block or allow access.
