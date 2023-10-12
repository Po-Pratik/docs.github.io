---
title: How to allow social networking sites in lunch hours
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [lunch hours]
---

# Overview

Most network administrators can access and track anything employees do on their computers. Many employees waste time on social networking sites, risking not only their employment status but also their reputations. Many organizations block access to social networking sites to limit distractions. However, recognizing the importance of work-life balance, some organizations are choosing to allow limited access during lunch hours.

# Prerequisite

- HTTPS Inspection should be enabled in SafeSquid. If not enabled, you can check our document - [How to enable HTTPS Inspection](#).
- Ensure the SScore section is enabled as TRUE (Application setup >> SScore).

# Access the SafeSquid User Interface

![Social Lunch (1).png](Social%20Lunch%20(1).png)

Click on the Search Icon at the bottom right corner of the SafeSquid WebGUI.

![Social Lunch (2).PNG](Social%20Lunch%20(2).PNG)

# Search default policy: LUNCH

Enter "LUNCH" into the value field and click search.

![Social Lunch (3).png](Social%20Lunch%20(3).png)

This will show the default LUNCH policy under the Time Profile section.

# Go to Time Profiler

Open the default LUNCH policy.

![Social Lunch (4).PNG](Social%20Lunch%20(4).PNG)

## Edit LUNCH policy

Modify the lunch time as needed and save.

![Social Lunch (5).png](Social%20Lunch%20(5).png)

Ensure the global part of the Time Profiler section is enabled.

![Social Lunch (6).PNG](Social%20Lunch%20(6).PNG)

By default, this setting is FALSE.
![Social Lunch (7).png](Social%20Lunch%20(7).png)

After enabling, save the policy.
![Social Lunch (8).PNG](Social%20Lunch%20(8).PNG)

# Go to Access Profiles

Open Access Profiles from the Restriction Policies menu.

![Social Lunch (9).png](Social%20Lunch%20(9).png)

## Create New Policy

Create a new policy and incorporate the default LUNCH profile.

![Social Lunch (10).PNG](Social%20Lunch%20(10).PNG)

Select the default "Socialnetworks" category.
![Social Lunch (11).png](Social%20Lunch%20(11).png)

Set the action to ALLOW.
![Social Lunch (12).PNG](Social%20Lunch%20(12).PNG)

Specify a unique profile name and save.
![Social Lunch (13).PNG](Social%20Lunch%20(13).PNG)

# Testing

## Access Social Networking Sites in LUNCH Time

During lunch hours, you should be able to freely access social networking sites. Outside of these hours, access attempts should display a BLOCK template.
