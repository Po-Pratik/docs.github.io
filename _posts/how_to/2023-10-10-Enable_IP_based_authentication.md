---
title: Enable IP based authentication
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [user authentication, IP auth]
---

# Overview

Proxy applications often restrict access based on IP address. Network administrators in many organizations prefer to block access to specific addresses or address ranges that are believed to be malicious.

SafeSquid SWG enables control of individual or ranges of IP addresses through the Access Restrictions section in the Application Setup side menu. SafeSquid SWG ensures that users don't get locked out from their current IP address. If you're within a corporate intranet, be cautious when setting up IP policies. The IP address on your computer (e.g., 192.168.0.10) might not match the IP address seen on the internet due to potential proxying or NAT. 

Users with restricted access based on these policies will see a block template in their browser.

# Prerequisites

Ensure that your IP address isn't already added in the Access restrictions section.

# Access the SafeSquid User interface

![Interface Image](IP-based-auth-Slide1-(1).PNG)

# Go to Access restrictions

Navigate to the configure page in the SafeSquid WebGUI and open the Access Restrictions section found in the Application Setup side menu.

![Access Restrictions](IP-based-auth-Slide1-(2).PNG)

## Go to Allow list

Navigate to the Allow list subsection to create a new policy.

![Allow List](IP-based-auth-Slide1-(3).PNG)

## Create New Policy

Click on the "Add New" icon located in the bottom left corner.

![New Policy](IP-based-auth-Slide1-(4).PNG)

Input your IP address in the IP Address field. You can also specify multiple IP addresses separated by commas or define a range of IPs.

![IP Address](IP-based-auth-Slide1-(5).PNG)

Specify a unique User-Group name in the "Add to User-Groups" field. Here, we've named it "IP BASED AUTHENTICATION".

![Authentication Name](IP-based-authentication.PNG)

# Testing

To verify, try accessing a website from the specified IP address (in this example, 192.168.0.10). An authentication prompt will appear, where you'll need to enter the username and password of your Linux machine. If specific usernames and passwords are defined in the policy, only those users will be granted web access.
