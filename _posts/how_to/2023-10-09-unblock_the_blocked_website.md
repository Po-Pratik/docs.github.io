---
title: Unblock the blocked website
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [troubleshooting]
---

# Overview

Some websites are blocked due to entries created in SafeSquid configuration, and it's not clear which security filter is responsible for the blocking. To address this, we need to identify the filter causing the block and create a new entry to allow the blocked website or modify the existing entry.

## Prerequisites

You must have knowledge of the different types of security filters available in SafeSquid.

For more details about SafeSquid configuration, refer to [this link](link-to-safe-squid-configuration).

# Finding the Reason for Blocking

You can find the reason for blocking in two ways:

1. By observing the SafeSquid Extended Logs.

2. By using the SafeSquid block template shown on the browser.

## Profiles

If a website is blocked with Access profile rules, you should receive a SafeSquid blocked template and a 403 status code.

Read more about [Providing Access to the Blocked Website](link-to-access-profiles).

## Text Analyzer

If a website is blocked with Text Analyzer, you should receive a SafeSquid blocked template and a 403 status code.

Read more about [Unblocking the Website Blocked with Text Analyzer](link-to-text-analyzer).

## Image Analyzer

Image Analyzer blocks inappropriate images by using their Threshold score.

Read more about [Unblocking the Website Blocked with Image Analyzer](link-to-image-analyzer).

## Cookie Filter

Cookie filter blocks logins to websites.

Read more about [Unblocking the Website Blocked with Cookie Filter](link-to-cookie-filter).

## Elevated Privacy

Elevated privacy blocks third-party cookies.

Read more about [Unblocking the Website Blocked with Elevated Privacy](link-to-elevated-privacy).

## Header Filter

Read more about [Unblocking the Website Blocked with Header Filter](link-to-header-filter).

## SSL Errors

Read more about [Unblocking the Website Blocked with SSL Errors](link-to-ssl-errors).
