---
title: Access Remote Desktop Applications Through SafeSquid
date: 2023-10-07 16:00:00 +05:30
categories: [development]
tags: [development]
---

# Case 1: There is no direct Internet access to the client Machine

## A) HTTPS ENABLED
- **Any desk**: Unable to connect to the remote server through proxy.
- **Team viewer**: Unable to connect to the remote server through proxy.
- **AmmyAdmin**: Unable to connect to the remote server through proxy.

## B) HTTPS DISABLED
- **Any desk**: Can connect to the remote server through proxy.
- **Team viewer**: Can connect to the remote server through proxy.
- **AmmyAdmin**: Can connect to the remote server through proxy.

## How to block in the above (B) scenario:
1. Enable the default entry in access profiles named as: BLOCK APPLICATIONS
2. Enable HTTPS inspection in SafeSquid.

# Case 2: There is a direct Internet access to the client Machine

## A) HTTPS ENABLED
- **Any desk**: Can connect to the remote server. It should not use proxy settings if there is a direct Internet connection.
- **Team viewer**: Can connect to the remote server through proxy. Uses proxy settings, but if blocking rules are applied on the proxy, then it will use direct Internet connection. Thus, it's not possible to block TeamViewer with proxy when there's a direct internet connection.
- **AmmyAdmin**: Unable to connect to the remote server through proxy.

## B) HTTPS DISABLED
- **Any desk**: Can connect to the remote server. It doesn't use proxy settings if there's a direct Internet connection.
- **Team viewer**: Can connect to the remote server through proxy.
- **AmmyAdmin**: Can connect to the remote server through proxy.

## How to block in the above (B) scenario:
1. It's not possible to block AnyDesk and TeamViewer with a direct Internet connection, because they don't use the proxy settings configured in the settings.
2. AmmyAdmin can be blocked by enabling the default entry in Access profiles or by enabling HTTPS Inspection.
