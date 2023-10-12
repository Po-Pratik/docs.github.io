---
title: Allow Outlook To Work Through SafeSquid
date: 2023-10-07 16:00:00 +05:30
categories: [development]
tags: [development]
---

# Outlook Issues with SafeSquid Authentication and SSL Inspection

Many users have reported issues with MS Outlook when authentication (Negotiate or basic) and/or SSL inspection are enabled in SafeSquid. Typically, SafeSquid is deployed in environments where a preceding firewall only allows traffic on ports 80 and 443 from SafeSquid, blocking all other ports.

# Deep Dive into the Problem

Upon investigation, it was observed that Outlook uses more than just HTTP and HTTPS protocols. It also operates on other protocols such as SMTP(S), IMAP(S), and POP(S) which are not HTTP(S) traffic. Additionally, Outlook sends DNS queries over UDP and interacts with LDAP on ports 389 and 636.

Interestingly, Outlook is found to support proxy authentications (Negotiate and basic) and can also negotiate SSL using a certificate deployed in Internet Explorer. The solution to this problem involves allowing the necessary traffic on your firewall.

# Solutions

To allow Outlook traffic, you have two primary methods:

1. Configure iptables rules on the SafeSquid server.
2. Configure these policies in your organization's firewall.

Here are the iptables rules to allow the necessary Outlook traffic:

```bash
# Allow established incoming connections
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT

# Allow loopback connections
iptables -A INPUT -i lo -m comment --comment "Allow loopback connections" -j ACCEPT

# Allow incoming ping requests
iptables -A INPUT -p icmp -m comment --comment "Allow Ping to work as expected" -j ACCEPT

# Allow specific incoming ports
iptables -A INPUT -p tcp -m multiport --dports 22,25,53,110,389,465,587,636,953,993,995 -j ACCEPT
iptables -A INPUT -p tcp -m multiport --dports 1023,3268,3269,5222,5269,5280,8080 -j ACCEPT

# Allow specific incoming UDP ports
iptables -A INPUT -p udp -m multiport --dports 53,953 -j ACCEPT

# Allow established outbound connections
iptables -A FORWARD -m state --state RELATED,ESTABLISHED -j ACCEPT

# Allow specific outbound ports
iptables -A FORWARD -p tcp -m multiport --dports 22,25,53,110,389,465,587,636,953,993,995 -j ACCEPT
iptables -A FORWARD -p tcp -m multiport --dports 1023,3268,3269,5222,5269,5280,8080 -j ACCEPT

# Allow specific outbound UDP ports
iptables -A FORWARD -p udp -m multiport --dports 53,953 -j ACCEPT

# Drop remaining traffic
iptables -P INPUT DROP
iptables -P FORWARD DROP
```
These iptables rules ensure that Outlook works smoothly even when SafeSquid's authentication and/or SSL inspection are enabled.