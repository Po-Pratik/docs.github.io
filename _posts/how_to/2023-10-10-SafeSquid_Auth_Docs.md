---
title: Authentication in SafeSquid
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [auth types]
---

# Proxy Authentication
  * Proxies can serve as access-control devices.
  * HTTP defines a mechanism called proxy authentication that blocks
 requests for content until the user provides valid
 access-permission credentials to the proxy.

Proxyimage.png

  * When a request for restricted content arrives at a proxy server,
 the proxy server can return a 407 Proxy Authorization Required
 status code demanding access credentials, accompanied by a
 Proxy-Authenticate header field that describes how to provide those
 credentials.
  * When the client receives the 407 response, it attempts to gather
 the required credentials, either from a local database or by
 prompting the user.
  * Once the credentials are obtained, the client resends the request,
 providing the required credentials in a Proxy-Authorization header
 field.
  * If the credentials are valid, the proxy passes the original request
 along the chain; otherwise, another 407 reply is sent.

There are 3 Ways how someone can Setup & use Authentication

# SafeSquid Users

  * This is one of the simplest methods which one could use for
 authentication.
  * Firstly, SafeSquid needs to be installed and running on the
 machine.
  * Now, navigating to http://safesquid.cfg/ in the web browser which
 has the SafeSquid machine proxy in it.
  * In this Web Page go to configure -> Access Restrictions  ->
 Allow List and create your own policy by clicking on the orange ‘+’
 icon.

Safesquidusers1.png

  * Now make sure that PAM Authentication is disabled and enter the
 required details. And it should look something like this:

Safesquidusers2.png

  * Now for the authentication purpose Simply add the username and
 password in the Username and Password Field.
  * As soon as you click on the save button it will show a prompt for
 username and password. Enter the credentials which you entered in
 the policy.
  * That’s how easy it is to authenticate in SafeSquid.

Disadvantages:
  * It has a few drawbacks of itself.
  * It is not that  secured since the password field is visible and the
 same password is set for all the users.
  * Therefore, if you want to set different password then you must make
 new policy.
  * Even though it is simple to configure it is an arduous work to
 manage it.
  * It is suitable if the number of users are less then 10.

# SafeSquid Linux Machine Users
  * For this principle you will be making the users in the Linux
 machine instead of making them in the configure page.

  * Firstly go to the Linux machine where the safesquid is installed
 and create a new user in it by firing this command: useradd
 name_of_the_user.
  * Now, give the password to that user and to do that you write:
 passwd name_of_the_user. It will ask you for a new password (if the
 user is new) and you will again have to confirm it.

RTENOTITLE

  * Now, navigating to http://safesquid.cfg/ in the web browser which
 has the safesquid machine proxy in it.
  * In this Web Page go to configure -> Access Restrictions  ->
 Allow List and create your own policy by clicking on the orange ‘+’
 icon.

Safesquidusers1.png

  * Now make sure that PAM Authentication is disabled and enter the
 required details. And it should look something like this:

Linux3.png

  * Now for the authentication purpose Simply add the username in the
 Username field.

Linux4.png

  * As soon as you click on the save button it will show a prompt for
 username and password. Enter the credentials which you entered in
 the linux machine.
  * That’s how easy it is to authenticate in safesquid through creating
 user in linux machine and using PAM Authentication.

Disadvantage:
  * Even though it is more secured then the SafeSquid User one it is
 still difficult to manage the users in the linux machine.
  * It is suitable for small organizations.

# LDAP Users

  * You can integrate a LDAP service like OpenLDAP or Microsoft AD to
 setup Basic Proxy Authentication
  * The openLDAP service is much simpler to implement and managing the
 users through LDAPadmin is much easier then the SafeSquid Users and
 the SafeSquid Linux Machine Users.
  * Microsoft AD need to up and running on the Windows server and it is
 also easy to manage through LDAPadmin.
  * These methods could be used it the number of the users in an
 organization are roughly around 50-65.
  * The integration part is a bit tricky but once it is done then there
 won’t be any problem in the future.

Read  more about How to integrate AD or OpenLDAP with SafeSquid

# Kerberos Authentication

  * You can integrate a LDAP service like OpenLDAP or Microsoft AD to
 setup Kerberos Proxy Authentication.
  * The major difference and which makes the life of the users much
 easier is that it automatically identifies User. This means that
 the user no more need to enter it’s credentials for the
 authentication purpose.
  * The setup of this is more tricky then LDAP user but once it’s done
 then it will be much easier to Authenticate the user without
 remembering the username and password or entering them again and
 again.

Read  more about Integrate a Linux Host with a Windows AD for Kerberos
SSO authentication