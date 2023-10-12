---
title: Deploy SafeSquid Behind Corporate Proxy
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [firewall]
---

# Overview

Use SafeSquid in front of the corporate proxy. By configuring SafeSquid, it can forward all client requests to the forward (or Parent) Proxy.

**Example scenarios:**
![Proxy Chain Scenarios](Proxy_chain_scenarios.png)

- Client(Browser) IP - 192.168.0.27
- Child Proxy IP - 192.168.27.50 (No direct internet Access)
- Parent Proxy IP - 192.168.27.100

**Configuration on child proxy:**

1. Deploy SafeSquid proxy
2. Enable SSL inspection
3. Download ROOT CA certificate from SafeSquid
4. Deploy certificate in client browsers.
5. Enable forwarding to parent proxy

**Configuration on Parent proxy:**

Just deploy the SafeSquid parent proxy.

# Prerequisites

- Enable HTTPS inspection on the child proxy. (Optionally, on the Parent proxy too)
- [How to configure HTTPS inspection](#)
- Import SafeSquid child proxy ROOT CA in client browser.

> **Note:** No extra configuration is required on the Parent Proxy server. 

# Access The SafeSquid User Interface

# Go to Configure

![Configure Page](Go_to_configure_page.png)

# Go to Application Setup

![Application Setup](Go_to_Application_setup.png)

# Go to Proxy chain

![Proxy Chain](Go_to_proxy_chain.png)

# Enable Global section

![Global Section 1](Proxy_chain5.png)
![Global Section 2](Proxy_chain6.png)
![Global Section 3](Proxy_chain7.png)

# Go to Forwarding proxies

![Forwarding Proxies](Proxy_chain8.png)

# Add an entry

![Add Entry 1](Proxy_chain9.png)
![Add Entry 2](Proxy_chain10.png)
![Add Entry 3](Proxy_chain11.png)
![Upstream Proxy IP](Enter_upstream_proxy_IP.png)
![Upstream Proxy IP 2](Proxy_chain12.png)
![Upstream Proxy Port](Proxy_chain13.png)
![Upstream Proxy Port 2](Proxy_chain14.png)
![Upstream Proxy Port 3](Proxy_chain15.png)
![Upstream Proxy Port 4](Proxy_chain16.png)
![Upstream Proxy Port 5](Proxy_chain17.png)
![Upstream Proxy Port 6](Proxy_chain18.png)

# Testing

![Testing 1](Proxy_chain19.png)
![Testing 2](Proxy_chain20.png)
![Testing 3](Proxy_chain21.png)

# Save configuration

![Save Config](Save_config_final.png)

When saving, you'll be prompted to store your configuration in the cloud. Choose "Yes" if you want to use this configuration in other SafeSquid instances or if all sections are validated. Otherwise, choose "No" and submit.
