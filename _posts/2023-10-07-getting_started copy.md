---
title: Getting Started
date: 2023-10-07 16:00:00 +05:30
categories: [getstarted]
tags: [minimumrequirements]
---

# Introduction

SafeSquid is an RFC 2616 compliant HTTP/1.1 proxy server, specially designed to provide maximum protocol, and payload security.

SafeSquid based Secure Web Gateways enable your users to safely access the web.
SafeSquid, when setup in Reverse Proxy mode, secures your web applications.

SafeSquid is a highly scalable software, that enables scaling up by increasing the hardware provisioning, or scaling out by creating an application cluster.

While the installable packages for both these platforms are different for obvious reasons, the configuration and operation is quite identical. So you can choose platform of your choice, to host SafeSquid Proxy Service. Yes, the advantages of deploying SafeSquid on Linux are overall higher because the Linux operating system is better suited for servers. But then if you are more comfortable with Microsoft®Windows, you can happily deploy on Windows. Migration from either of the platforms to the other is not very difficult, really!

 
# System Requisites

Use SafeSquid Appliance Builder (SAB) to setup your secure web gateway. SAB is an Ubuntu Linux operating system ISO, customized to provide automatic setup of all the necessary files and services. SAB enables you to transform a standard Intel® hardware architecture for servers, into a hardware web security appliance, or a setup a virtual appliance on any virtualization infrastructure like VmWare® or Microsoft Hyper-V®.

Use the SafeSquid installation packages (tar.gz) if you wish to setup secure web gateway on other Linux distributions like RedHat®, SuSe®, CentOS®, etc.

Use Windows installer package to setup SafeSquid on a Microsoft Windows system.

# Hardware Requirements
## Minimal Hardware

* RAM: 4 GB
* CPU: 4 Core
* HDD: 160 GB (Depending upon the number of logs and database you want to keep)

 
## Recommended Hardware

SafeSquid is SMP-aware so if you need to serve a large number of users, you should use hardware with multiple CPU cores, and ability to use more RAM efficiently.
While the above specified Minimal Hardware should enable you to do a functional setup of SafeSquid, actual hardware requirements would vary depending upon the number of users, concurrent connections, and features you intend to enable. As a thumb rule - add 2 CPU cores and 4GB RAM per 100 concurrent connections.
### Suggested Hardware Sizing 

|CPU (cores)    | RAM (GB)  | 	HDD  |Max Concurrent Connections|Approx Users|
|:---------------:|:-----------:|:--------:|:--------------------------:|:------------:|
|4 	            |   8 	    | 500GB  |      	 100 	        |   25       |
|4 	            |   16   	| 1TB 	 |           500 	1       |   50       |
|8 	            |   16   	| 2TB 	 |           1000 	        |   350      |
|8 	            |  32   	| 4TB 	 |           1500 	        |   600      |
|16 	        |  32   	| 4TB 	 |           2000 	        |   1000     |
|16 	        |  64   	| 8TB 	 |           2500 	        |   1500     |

If you intend to use SafeSquid's HTTPS Inspection feature, using processors with "AES-NI", is recommended.

[How to find out AES-NI (Advanced Encryption) Enabled on Linux System](https://www.cyberciti.biz/faq/how-to-find-out-aes-ni-advanced-encryption-enabled-on-linux-system/)

# Installation and Activation
## Get Product Activation Key

Before downloading the SafeSquid installer(s), you MUST register to create your account on SafeSquid's self-service portal at - [key.safesquid.com](https://key.safesquid.com/).. Registration is free, and requires just a few minutes. Your registered account also provides the management of SafeSquid's cloud-backed features, like Custom Web Categorization, VPN support, Configuration Backup, Subscription management, etc.

All registered users are provided with a Product Activation Key. After the actual installation, you must upload this activation key via SafeSquid's Browser based Interface. Your users may not be able to access the web until then. Use the same Activation Key across all your instances of SafeSquid, to ensure easy replication of policies, and other common aspects.

Read more about Registration Process for [key.safesquid.com](https://key.safesquid.com/).

## Download Installation Package
### SafeSquid Appliance Builder

SafeSquid Appliance Builder (SAB) is the most recommended installer. You may download it using the link displayed when you log into your registered account. 
Alternatively you may download it from - [safesquid.iso](https://downloads.safesquid.com/appliance/safesquid.iso). 
SAB is a customized version of Ubuntu 18.04 x86_64 minimal iso. You may create a virtual appliance using the SAB iso on any virtualization infrastructure, or boot a standard Intel Server hardware to create a hardware appliance.

Read more about [Setup Your Secure Web Gateway With SafeSquid Appliance Builder]()

### Legacy SafeSquid for Linux

Read more about [Setup Your Secure Web Gateway on your preferred Linux distribution]()

## Activate your Product

Before you start accessing the web via SafeSquid you must activate it. Read more about [How to Activate a SafeSquid Instance]()

# Basic Setup

If you plan to use HTTPS inspection, then you must first [configure HTTPS inspection]()

Integration of SafeSquid Proxy Service with your [Microsoft Active Directory](), or [OpenLDAP service](), would be the most recommended immediate next step.

The [How To]() section could provide you with a fair idea of the rest of the goals that you may want to achieve. 