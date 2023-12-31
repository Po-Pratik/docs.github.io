---
title: Split the load between different ISPs
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [load balancing]
---

SafeSquid has an option in 'Network Settings', to add new interface for
outgoing connection.
This is useful in networks where you need to split the load between
different ISPs. It can also be useful to switch different ISPs due to
slow net connection or discontinuity.

You wish to -
1. Forward outgoing request of the user group 'Accounts' and 'Finance'
to ISP whose connection is on interface with IP 192.168.0.175
2. Forward outgoing request of the user group 'IT' and 'System' to ISP
whose connection is on interface with IP 192.168.0.180

Note : The binding profiles must be exist in Profiles and policies (
Access Profiles ) section. (in above example : Accounts, Finance, IT,
System profiles are already created in Access Profiles).
Then, in 'Network Settings' section, add the following rules under the
'Interface' subsection -

NETWORK SETTINGS.png
