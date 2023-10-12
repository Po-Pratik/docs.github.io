---
title: Transparent Redirection With SafeSquid And WCCP
date: 2023-10-11 16:00:00 +05:30
categories: [How To]
tags: [wccp]
---

# GOAL

Are you looking for

Transparent redirection of traffic?

So, no user need to set proxy settings in browsers.

Load balance traffic & Scaling up?

Add more proxies to serve traffic and distribute traffic across
multiple proxies.

Service assurance and high availability?

 If one proxy fails, then other proxies should serve
clients traffic.

If you are here for any of above challenges then SafeSquid with WCCP is
a solution for you.

# What is WCCP?

Web Cache Communication Protocol (WCCP) is a Cisco-developed
content-routing protocol that provides a mechanism to redirect traffic
flows in real-time. It has built-in load balancing, scaling, fault
tolerance, and service-assurance (failsafe) mechanisms.

# How it works with SafeSquid?

Enable WCCP support in routers. This can be done only if your router
supports WCCP.

Ex: CISCO ASA routers.

2.Configure SafeSquid to interact with WCCP enabled routers using WCCP
section.

3.Configure end users to use WCCP enabled router as gateway.

The story is over. Now all your clients traffic will be transparently
redirected to SafeSquid proxy by router and SafeSquid serves traffic.

The below picture will tell you whole story.
WCCP.png

WCCP Describes the communication between WCCP enabled Router and
SafeSquid Proxy(Web-cache) to implement transparent redirection with
scaling and fail-safe benefits.

1.Enable WCCP and transparent redirection support in Routers(Gateway).

2.Configure SafeSquid Proxies(Web-Caches) with WCCP enabled router
information to work in coordination to participate in transparent
redirection. SafeSquid proxies will send HERE I AM messages to routers
and routers acknowledge with I SEE YOU messages. After then all
together will be ready to serve clients traffic. One of the SafeSquid
proxies will become master & implement redirection rules and inform to
router using REDIRECT ASSIGNMENT. Routers are ready to forward traffic
as told by SafeSquid proxy.

3.Users are configured to use WCCP enabled router as gateway and router
denies direct access to the internet and redirects incoming
packets(traffic) to the group of SafeSquid proxies which are interacted
with router using WCCP Protocol. SafeSquid proxies will serve traffic.

# Benefits

1.End users does not need to configure proxy in their browsers.

2.Fail Safe - If a proxy fails remaining proxies will handle the
traffic

3.Scale Up - Add any number of proxies without disturbing environment

4.Load balance- Traffic will be distributed across all proxies.
