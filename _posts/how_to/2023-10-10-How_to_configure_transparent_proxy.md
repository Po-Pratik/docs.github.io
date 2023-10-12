---
title: How to configure transparent proxy
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [transparent]
---

# Overview

Internet is an essential part of most company’s business
infrastructure.However, it can be a risky place, but there are ways to
minimize risks so your business can thrive. Analysts encourage
organizations to deploy a secure web gateway (SWG) to protect their
networks against access by malicious software.

Initially, the Internet was designed with the assumption that
connections between entities are explicit and stateful. An SWG
intercepts and examines inbound and outbound web traffic and, in
effect, becomes a proxy for the user, who no longer interacts directly
with the web site. At first, browsers had to be explicitly configured
to use the web gateway, which led to the concept of a direct proxy. As
networks grew and endpoint management became increasingly complex, the
need emerged to control web communications without directly
manipulating the endpoint. This led to the concept of a transparent
proxy.

The key difference between a direct (or explicit) proxy and a
transparent proxy is that a direct proxy is known to the application,
which realizes it is talking to a proxy and not the destination server,
whereas transparent proxy mode is an intercept model and requires fewer
changes to be implemented on the endpoint. Applications think they are
going straight to the destination but, in reality, a network service is
redirecting the traffic to the proxy, which then forwards it to its
destination.

# Client Scenario

Stark tech is having 200 employees.Stark tech wants to provide internet
services to the employees through WIFI. When the employees opens their
web browser, they’re connected to a proxy server that manages all of
the network’s communication.

Since this is a new employee, the proxy displays a web page in the
browser asking the employee to agree certain terms and conditions. If
the employee accepts, then the proxy routes it's traffic to the actual
destination using transparent proxy.

# What is transparent proxy?

A transparent proxy (also called inline proxy, intercepting proxy, or
forced proxy) is a server that sits between your computer and the
Internet and redirects your requests and responses without modifying
them. A proxy server that does modify your requests and responses is
defined as a non-transparent proxy.

Transparent proxies act as intermediaries between a user and a web
service. When a user connects to a service, the transparent proxy
intercepts the request before passing it on to the provider.
Transparent proxies are considered transparent because the user isn’t
aware of them. On the other hand, the servers hosting the service
recognize that the proxied traffic is coming from a proxy and not
directly from the user.

SafeSquid support both HTTP and HTTPS websites in transparent mode.The
HTTPS websites in transparent mode is called as SSL transparent mode.

# How SafeSquid transparent proxy works ?

Transparent proxy2.png
  * Bob is using a laptop in Stark tech and want to access internet
 services via Stark tech WIFI network.
  * Bob enable WIFI on his laptop.
  * Identified Stark tech WIFI network and tried to connect to Stark
 tech WIFI.
  * Now admin of the Stark tech receive an IP address of Bomb(say
 192.168.24.20) to check filtering policies, serve traffic.
  * The traffic will come to router and router will send traffic to
 SafeSquid Secure web gate way with port 80 and 443 respectively.
  * The redirection rules on SafeSquid Secure web gateway will redirect
 traffic to SafeSquid Proxy with port 8080 and 8443 (SSL
 transparent)respectively(By enabling IP forwarding).
  * When Bob set SafeSquid Proxy IP address 192.168.221.222 as a
 gateway, Bob will get access of WIFI network and he can access all
 HTTP as well as HTTPS websites transparently.
  * SafeSquid transparent proxies are extremely versatile.
  * The following list contains usefulness of SafeSquid transparent
 proxy to Bob.

 1. Proxy caches created copies of the data stored on a server and
 serve the cached content to Bob. This reduces the strain on the web
 service by having the proxy provide the content instead of the
 service itself.
 2. Filtering proxies prevent access to certain websites or web
 services. These are commonly implemented by organizations to
 prevent users from accessing resources that are unrelated or
 disruptive to the organization.
 3. Gateway proxies modify or block network traffic based on certain
 policies. Locations that offer public Wifi often implement gateways
 that require users to register or accept an agreement before they
 can use the service.

# Prerequisites

  * Deploy SafeSquid Secure web gateway (SAB)
  * Enable SafeSquid SSL transparent facility on two ports, one is port
 8081 for HTTP traffic and other one is port 8433 for HTTPS traffic.
 Also Enable SSL Inspection to control SSL traffic. If not enabled,
 you can check our document - How To Enable HTTPS Inspection
  * Redirect traffic from port 80 and 443 to 8081 and 8443
 respectively. The redirection can take place on router if router
 supports redirection.
  * Make sure IP tables-persistent package is installed (to save IP
 table rules)
  * If your router only supports traffic forwarding then you should
 redirect traffic on SafeSquid server using IP tables.

# Configure Transparent proxy

## Redirect traffic from Port 80 and 443 to 8080 and 8443 respectively

### STEP 1: To forward requests for all destination ports

1. **Enable forwarding in /etc/sysctl.conf**: Change the following:

    ```
    net.ipv4.ip_forward=0 >> net.ipv4.ip_forward=1
    ```

2. **Reload configurations**:

    ```
    sysctl -p
    ```

3. **Flush the iptables rules**:

    ```
    iptables -F -t nat
    ```

### STEP 2: Redirect traffic

1. **Redirect requests for port 80 to 8080**:

    ```
    iptables -A PREROUTING -t nat -s 192.168.0.0/16 -p tcp --dport 80 -j REDIRECT --to 8080
    ```

2. **Redirect requests for port 443 to 8443 (for SSL transparent proxy)**:

    ```
    iptables -A PREROUTING -t nat -s 192.168.0.0/16 -p tcp --dport 443 -j REDIRECT --to 8443
    ```

### STEP 3: Save IP table

1. **Install iptables-persistent**:

    ```
    apt-get install iptables-persistent
    ```

2. **Save IP table configuration**:

    ```
    iptables-save >> /etc/iptables/rules.v4
    ```

> **Note**: Redirection policies will not flush even if you reboot the proxy server.

### Access the SafeSquid interface

#### Go to the Configure Page.
![Transparent Proxy.png](Transparent Proxy.png)
![Slide3.png](Slide3.png)
#### Enable policy from Network settings.
![Slide4.png](Slide4.png)
#### Restart SafeSquid Service
[Restart the SafeSquid Service from Interface.]()
#### Remove Proxy settings from browser
![Slide5.png](Slide5.png)
![Slide7.png](Slide7.png)
![Slide8.png](Slide8.png)
![Slide9.png](Slide9.png)
#### Configure Network
![Slide10.png](Slide10.png)
![Slide11.png](Slide11.png)
![Slide12.png](Slide12.png)
![Slide13.png](Slide13.png)
Open the network and share center and go to "Local area connection" as shown. (In our case Proxy IP: 192.168.221.222).
![Slide14.png](Slide14.png)

**Now you can access all the HTTP and HTTPS websites successfully without setting proxy inside the browser.**

# Benefit

Transparent proxies are an unobtrusive way to add features and
functionality to a user’s browsing experience.
  * Enterprises experience greater control over how their customers
 interact with their services by routing and modifying requests as
 they come in.
  * Users interact with web services more easily since their
 connections are seamlessly and invisibly passed through the proxy,
 leaving configuration to the service providers.

Conclusion

Transparent proxies shape the way we interact with the web. Whether
they’re serving data faster through caching, filtering out unwanted
content, or giving businesses more control over their networks,
transparent proxies add functionality to the Internet without adding
inconvenience.
From: 
[https://www.maxcdn.com/one/visual-glossary/transparent-proxy/?utm_sourc
e=text](https://www.maxcdn.com/one/visual-glossary/transparent-proxy/?utm_sourc
e=text)

SafeSquid transparent proxies shape the way we interact with the web.
Whether they’re serving data faster through caching, filtering out
unwanted content, or giving businesses more control over their
networks, SafeSquid transparent proxies add functionality to the
Internet without adding inconvenience.
