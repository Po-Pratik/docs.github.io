---
title: How to set website redirections.
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [redirect]
---

# Procedure

Access the SafeSquid User Interface
SafeSquid comes with sample policy, helping you in policy creation.

In SafeSquid sample policies " Enable interface access through
authentication " policy  is already present. You have to just enable
that policies, so that it becomes applicable.

Click on 'Configure' which is at top right of the SafeSquid Interface.

On the left side bar of SafeSquid Interface click on Real Time Content
Security>>  Redirect

Make the Global Section Enabled to TRUE.
Redirect-global.jpg

Then click on Redirection Policies , here you across with some default
policies.Add new policy.
Redirect-policies2.jpg

Create a policy as shown:
Redirect policy.jpg

Click on save (Save button is placed at right bottom)

Testing:

In this the URL value 'rediff.com' is redirect to 'SafeSquid.com' and
the port to redirect to 80.

Go to browser and access http://rediff.com, it must redirect to
SafeSquid.com ,we can verify in Native logs on SafeSquid interface
Reports >> Native logs as like below.
Redirect-policies3.jpg
Retrieved from
"https://docs.safesquid.com/index.php?title=How_to_redirect_to_one_webs
ite_to_another_website&oldid=2159"