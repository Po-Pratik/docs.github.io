---
title: Configure
layout: post
icon: fa fa-gear
order: 3
---

# Configuration

Your enterprise network could have its own unique characteristics, constraints, and demands. You might need to configure each of SafeSquid's features for optimal results.

SafeSquid's embedded REST-based Web UI lets you access the configuration settings using any standard web browser like Firefox, Chrome, etc. The configuration for each feature is an independent section, grouped for convenience. [Read here](#) to learn how to access SafeSquid's UI.

SafeSquid loads configurations from the disk into memory when starting. The Web UI interacts directly with the memory configuration, enabling almost immediate effect for most changes without disrupting ongoing web sessions. However, these changes are "volatile" and would be lost when the SafeSquid process restarts. An option to "Save Settings" is at the bottom-right of the UI, ensuring changes remain effective upon restarts. Every time you save settings, the current configuration is backed-up, and the new configuration is saved on the disk. An option to save the new configuration to "SafeSquid Cloud-based Disaster Recovery" is also available.

## Application Setup

This set of SafeSquid features is generally configured during the initial pilot roll-out and seldom revisited afterward. These configurations ensure the application is deployed securely and is readily available for your enterprise network.

### Network Settings

Network settings define the sockets on which SafeSquid will listen and accept client connections. Choose additional bindings (roles) for this socket. Also, specify interfaces for outgoing connections [here](#).

[Read more about Network Settings](#)

### Integrate LDAP

Large network enterprises typically manage user credentials via a centralized system. This centralized system ensures user identification across all networked enterprise resources and services. Users benefit from a single set of credentials for access across the networked enterprise. Integrating a web gateway with a Directory Service can authenticate users based on Directory Service Credentials, control access based on role and hierarchy, and log and report user activity.

[Read more about Integrate LDAP](#)

### Access Restrictions

Access restrictions let you set rules governing internet access based on IP addresses, IP ranges, LDAP users, Basic authentication, etc.

[Read more about Access Restrictions](#)

### Accelerators

Accelerators optimize resource use and response times.

#### Caching

Content caching improves bandwidth efficiency by serving locally stored copies of previously fetched pages or files.

[Read more about Caching](#)

#### Prefetching

SafeSquid can analyze HTML pages to identify links to embedded content and initiate fetch and cache processes.

[Read more about Prefetching](#)

### System Configuration

Tune various parameters according to network infrastructure.

[Read more about System Configuration](#)

### Proxy Chain

The Proxy Chain section lets you forward requests through another proxy, SOCKS4, or SOCKS5 firewall.

[Read more about Proxy Chain](#)

### FTP Browsing

Configure how FTP connections are established and displayed.

[Read more about FTP Browsing](#)

### WCCP

Use WCCP routers to enforce a transparent proxy.

[Read more about WCCP](#)

## Real-time Content Security

Configure security filters like SSL inspection, antivirus, content modification, and image scanning.

### HTTPS Inspection

By enabling HTTPS Inspection, SafeSquid can perform deep content inspection of encrypted HTTPS traffic.

[Read more about HTTPS Inspection](#)

### Clam Antivirus

ClamAV is an open-source antivirus engine that detects viruses, trojans, malware, and other threats. Integrate your own ClamAV server with SafeSquid for additional protection.

[Read more about Clam Antivirus](#)

### Text Analyzer

The Text Analyzer can identify websites serving inappropriate content based on a keyword scoring system.

[Read more about Text Analyzer](#)

### Redirect

Redirect one URL to another for better control over user access.

[Read more about Redirect](#)

### DNS Blacklist

Set up a DNSBL service to prevent users from visiting dangerous websites.

[Read more about DNS Blacklist](#)

### Image Analyzer

Block inappropriate images by analyzing their graphical content in real time.

[Read more about Image Analyzer](#)

### ICAP

Integrate different types of ICAP servers with SafeSquid for better content scanning and control.

[Read more about ICAP](#)

### Content Modifier

Modify the content of web pages, headers, and files in real-time to ensure better user safety.

[Read more about Content Modifier](#)

### DLP

Data Loss Prevention (DLP) restricts users from sending sensitive or critical information outside the corporate network.

[Read more about DLP](#)

### SqScan

SqScan is a built-in module in SafeSquid that offers protection against viruses, trojans, malware, and other threats.

[Read more about SqScan](#)

## Custom Settings

### Categorize Web-Sites

SafeSquid comes with over 40 million categorized websites. Group websites into custom categories or re-categorize them based on your organizational needs.

[Read more about Categorize Web-Sites](#)

### Time Profiler

Set up time-based Internet access policies to control user access during specific times.

[Read more about Time Profiler](#)

### Response Types

Manage response profiles based on the responses received from web servers.

[Read more about Response Types](#)

### Request Types

Manage profiling based on the requests sent to the web server.

[Read more about Request Types](#)

### Templates

Customize templates used by SafeSquid to communicate with users under various conditions.

[Read more about Templates](#)

### External Applications

Use external programs or scripts to parse file contents.

[Read more about External Applications](#)

## Restriction Policies

### Privacy Control

Ensure safe information exchange between users and websites.

#### Cookie Filter

Control cookies for different websites to ensure user safety and privacy.

[Read more about Cookie Filter](#)

#### Header Filter

Control how SafeSquid edits HTTP headers passing between the user's browser and the Internet.

[Read more about Header Filter](#)

#### Elevated Privacy

Block third-party domain cookies and control tracking of user activity across different sites.

[Read more about Elevated Privacy](#)

### Access Profiles

Set up profiled Internet access policies to ensure better control over user web access.

[Read more about Access Profiles](#)

### Speed Limits

Configure bandwidth-related settings to ensure efficient network use.

[Read more about Speed Limits](#)
