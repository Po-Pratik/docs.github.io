---
title: How to block anonymous proxies
date: 2023-10-07 16:00:00 +05:30
categories: [development]
tags: [development]
---

# Access the SafeSquid User Interface

SafeSquid comes with a sample policy, helping you in policy creation.

**Note:** HTTPS Inspection should be enabled in SafeSquid. If not enabled, you can check our document - [How to enable HTTPS Inspection](http://docs.safesquid.com/index.php/Configure_HTTPS_Inspection).

- Click on 'Configuration' which is at the top right of the SafeSquid Interface.
- On the left sidebar of SafeSquid Interface, click on `Real Time Content Security` > `Text Analyzer`.

![Text-global](Text-global.jpg)

- Ensure the Global Section is set to TRUE and click on the Filtering policies subsection.
- Under the Filtering Policies subsection, search for "Anonymous Proxy". Ensure all those policies are set to TRUE.

![Anonymous proxy-policy](Annonymous_proxy-policy.jpg)

- On the left sidebar of SafeSquid Interface, click on `Restriction Policies` > `Access Profiles`.
- Search for "BYPASS TEXT FILTER" under the Filtering Policies subsection. Ensure all those policies are set to TRUE.

![Anonymous proxy-policy2](Annonymous_proxy-policy2.jpg)

- Click Save. (Save button is located at the bottom right.)

# Testing:

Try accessing a web proxy (e.g., hide.me) through SafeSquid. The page should be blocked.
