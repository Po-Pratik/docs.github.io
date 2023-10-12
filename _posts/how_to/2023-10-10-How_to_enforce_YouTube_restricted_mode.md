---
title: How to enforce YouTube restricted mode
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [youtube restrict]
---

# Overview

YouTube has countless hours of entertainment, videos, and TV shows to
keep you and your network users entertained. Apart from all these some
content are inapropriate (like pornography and potentially offensive
content) for some users. Most of the families and companies will not
prefer to have acess to such content by there kids and employees on
there network. Censorship of YouTube videos is very much needed in
these days. Some of the countries have blocked the accecc to YouTube
website.

YouTube offers a basic parental control feature, also known as
Restricted mode. This feature effectively avoids most inappropriate and
offensive video content on the YouTube service by filtering it out.
When you implement Restricted mode on YouTube, you can enforce content
restriction features only for individual browsers or users. In large
organizations, it is not possible to enable restrict mode manually for
each and every user, there is a possibility that the user himself may
disable the restricted mode.

SafeSquid provides a solution for these problems. SafeSquid provides an
option to enable restrict mode on your gateway level directly, and
enforces the restricted mode on YouTube so that users will not be able
to disable it. As YouTube supports HTTPS protocol, you just need to
enable HTTPS inspection on SafeSquid. You can also define restrictions
for a particular user or for every user based on your network
architecture.
For every request coming to SafeSquid for YouTube search a
YouTube-Restrict : Strict header will be added after which server will
give the filtered response.

# Prerequisites

HTTPS inspection, must be enabled on SafeSquid configuration. Check the
document to configure HTTPS inspection - How to configure HTTPS
inspection

Define entry for YouTube Restricted Mode

Here we have explained with a default configuration rule. If any of the
default entries is not found then you need to create new entry.

# ccess the SafeSquid Interface

## Go to configure page

![Google Safe search1.png](Google%20Safe%20search1.png)

SafeSquid SWG has many default rules in the configuration. End users just need to enable or disable those rules and create new rules if required.

![Youtube Restrict mode3.png](Youtube%20Restrict%20mode3.png)

## Enable YouTube Restricted Mode entry in Policies and profiles

Enable the default YouTube restricted mode rule from policies and profiles section.

![Youtube Restrict mode4.png](Youtube%20Restrict%20mode4.png)

This entry is applicable for all users. If you want to give an exception to any users then add that user group with negation. For example: `!ADMINS`

![Youtube Restrict mode5.png](Youtube%20Restrict%20mode5.png)

Save the policy after confirming the required entry is similar as shown below.

![Youtube Restrict mode6.png](Youtube%20Restrict%20mode6.png)

# Adding Strict header to client headers

## Go to Restriction Policies

![Youtube Restrict mode7.png](Youtube%20Restrict%20mode7.png)

## Go to Privacy control Section

![Youtube Restrict mode8.png](Youtube%20Restrict%20mode8.png)

## Go to Header filter Section

Open the Header filter section from the Privacy control menu.

![Youtube Restrict mode9.png](Youtube%20Restrict%20mode9.png)

### Turn on Global part of Header filter section

Enable the global field of the Header filter section.

![Youtube Restrict mode10.png](Youtube%20Restrict%20mode10.png)
![Youtube Restrict mode11.png](Youtube%20Restrict%20mode11.png)
![Youtube Restrict mode12.png](Youtube%20Restrict%20mode12.png)

### Go to Insert subsection

![Youtube Restrict mode13.png](Youtube%20Restrict%20mode13.png)

### Enable restricted mode entry to add strict header

![Youtube Restrict mode14.png](Youtube%20Restrict%20mode14.png)
![Youtube Restrict mode15.png](Youtube%20Restrict%20mode15.png)
![Youtube Restrict mode16.png](Youtube%20Restrict%20mode16.png)

# Testing

Try to search some explicit keywords and you will see the message as shown below.

![Youtube Restrict mode17.png](Youtube%20Restrict%20mode17.png)
![Youtube Restrict Mode18.png](Youtube%20Restrict%20Mode18.png)


# Save Configuration

Click on bottom left Icon to save the configuration.

Trouble shoot:

YouTube Restrict Mode is not working?
Save config final.png
When you click on Save config, it will give a prompt for asking the
confirmation to store your configuration  into the cloud.
Select Yes only in below cases:
  * if you want to use this same configuration in other SafeSquid
 instances.
  * if your total configuration in all sections is completed and
 validated.

Otherwise select No and click on submit.