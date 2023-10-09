---
title: Setup HTTPS Inspection.
date: 2023-10-07 16:00:00 +05:30
categories: [getstarted,setup,activateinstance]
tags: [setup,activate]
---

# Overview

Over the couple of years, the internet is changing its dimensions in terms of security. The web is shifting towards HTTPS, to deliver secure services to users. “The main motivation for HTTPS is authentication of the visited website and protection of the privacy and integrity of the exchanged data”. The authentication happens based on the public key of the website verified by the client browser using a trusted certificate authority. So, the users know they are talking to the right websites and their data is safe.

Until 2010, only 20% of websites were using the HTTPS protocol and the rest of the 80% of websites were on HTTP. This equation started changing from 2010. For example, earlier Google services including Google search were running on HTTP, for security reasons Google started services on HTTPS over HTTP. This change in the web threw challenges to security vendors and customers, but both are ready for a better web & security.

HTTP traffic is plain text-based message transfer over the network, the traffic can be seen and filtered by any device in the middle. Malware detection and data leak prevention are performed by security products on HTTP traffic to keep users and organizations safe. But HTTPS traffic is encrypted and traffic cannot be seen, filtered without decrypting traffic and decryption is only possible by trusted parties.

Decrypting HTTPS traffic for scanning is called HTTPS Inspection. If security products do not scan HTTPS traffic, then some users can upload confidential documents to Google Drive and share wherever they want. Also, such users can download a malicious file and spread it on the company network which can completely hit organizational productivity. There's a lot more that can happen, so security experts always recommend the usage of HTTPS inspection-enabled products for enhanced security.

Most of the old security products implemented before 2010 do not have the ability to scan HTTPS traffic including SafeSquid NTLM editions. SafeSquid SWG was implemented in 2012 with HTTPS inspection support and continuously improved HTTPS inspection performance with SSL context caching and session resumption techniques.

To perform HTTPS inspection, SafeSquid should have a trusted certificate authority(CA). You can use your enterprise CA as SafeSquid CA or you can generate a self-signed CA for the organization using SafeSquid's Self Service Portal.

# Client Scenario

The director of network security in a financial organization wants to protect the enterprise network from any external threats coming from the web in the form of malware. To accomplish this, the director appoints a Network administrator to make sure the computer network is up-to-date and operating as intended. The Network administrator needs to gain visibility into these sites otherwise bypass encrypted traffic and control access to malicious websites. The Network administrator should do the following:

- Intercept and examine all the traffic, including SSL/TLS (encrypted traffic), coming in and going out of the enterprise network.
- Bypass interception of requests to websites containing sensitive information, such as user financial information or emails.
- Block access to harmful URLs identified as serving harmful or adult content.
- Identify end-users (employees) in the enterprise who are accessing malicious websites and block internet access for these users or block the harmful URLs.

# Solution

To achieve all of the above, the Network administrator should set up a SafeSquid Secure Web Gateway (SWG) in the organization. The proxy server checks all the encrypted and unencrypted traffic passing through the enterprise network. It prompts for user authentication, and associates the traffic with a user. URL categories can be specified to block access to Illegal/Harmful, Adult, Malware, and SPAM websites.

# Benefits of HTTPS inspection

- You can forbid the use of personal Google accounts for any Google application like Gmail, YouTube, etc.
- You can permit users with bypass privilege to access Facebook in Read Only mode. Users are not allowed to make posts, shares, play games, chat with other Facebook Users, post on their timeline, or Like posts made by others.
- You can enforce SafeSearch for users accessing Google Search, Yahoo Search, Bing Search, YouTube.
- You can permit the use of Google SSO for login to web applications.
- You can use Virus scanning for both HTTP and HTTPS sites.
- You can forbid users from uploading files to any website.

# Configure the HTTPS inspection 

## Setup HTTPS inspection

Generate SSL (Self-Signed) certificates from the self-service portal.

You have to generate an SSL certificate from the self-service portal before configuring HTTPS inspection.

- [Setup your SSL (Self Signed) certificates from the self-service portal](#)
- [Download SSL (Self-Signed) Certificate from SafeSquid User Interface](#)

## Importing SafeSquid SSL certificate into your browser

When SafeSquid is installed in your network with HTTPS inspection enabled and SSL certificate not installed into the browser, then you will get an error while accessing the HTTPS websites. You have to install the SafeSquid SSL certificate into the browsers.

- [Importing into Mozilla Firefox](#)
- [Importing into Internet Explorer or Chrome Browser](#)

## Enabling HTTPS inspection on SafeSquid User Interface

- [How does HTTPS work?](#)
- [How does HTTPS inspection work with SafeSquid?](#)

# Troubleshooting

- [SSL certificate downloaded with zero size OR unable to download SSL certificate](#)
- [Application not working with HTTPS inspection](#)
- [SSL certification errors](#)
- [Certificate manageability](#)

# See Also

- [Integrate AD or OpenLDAP with SafeSquid](#)
- [Enforce Safe Searches](#)
- [Enforce YouTube Restricted Mode](#)
- [Defend Against Malware And External Attacks](#)

