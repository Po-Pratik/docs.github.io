---
title: Setup Your Secure Web Gateway on your preferred Linux distribution.
date: 2023-10-07 16:00:00 +05:30
categories: [How To]
tags: [HowTo]
---

# Overview

SafeSquid Appliance Builder (SAB) is an optimized version of Ubuntu Linux, optimized for easy setup of your secure web gateway. The SAB installs the Ubuntu Linux operating system, downloads and deploys the SafeSquid for Linux installation package, and the necessary dependencies. SafeSquid can also be installed on any other Linux operating system like Red-Hat, SuSe, CentOS, etc.

Choose this method of installation only if you want to setup SafeSquid on already existing infrastructure or if you want to use other Operating System in Linux family other than Ubuntu. It requires some additional configurations like Monit and bind services used by SafeSquid.

# Prerequisites

You must install required dependencies and other supporting services required for some modules of SafeSquid to work smoothly.

You can check and install required dependencies below.

Monit and Bind are other supporting services required by SafeSquid to work smoothly

Check - Configure Monit for SafeSquid Monitoring

Check - Bind Configuration with SafeSquid
Download latest version in Linux server

Go to the linux server and change the directory to “/usr/local/src” by using below command
```bash
cd /usr/local/src
```

Use "wget" command to download the latest SafeSquid package on the Linux machine on which you want to install the Safesquid. The command will download the tarball file.
```bash
wget http://downloads.safesquid.net/appliance/binary/safesquid_latest.tar.gz
```
Wget.jpg
Extract the tarball

Extract the files from tar by using below command.
```bash
tar -zxvf safesquid_latest.tar.gz
```

The output of the above command is shown below.
Untar1.jpg

All the files will be extracted in the directory having name "_mkappliance".

You have to execute/run the setup.sh script to install SafeSquid.
                        _mkappliance/installation/setup.sh

Output after script execution is shown below.
Setupsh.jpg

Installation completes if you did not get any error.
Dependency Check 

You can check if any of the dependencies missing for SafeSquid by using the "ldd" command as shown below.

```bash
ldd /opt/safesquid/bin/safesquid
```

Output for the above command is shown below.
```bash 
ldd /opt/safesquid/bin/safesquid
linux-vdso.so.1 =>  (0x00007ffebebdb000)
libldap_r-2.4.so.2 => /usr/lib/x86_64-linux-gnu/libldap_r-2.4.so.2 (0x00007ff03107e000)
libpam.so.0 => /lib/x86_64-linux-gnu/libpam.so.0 (0x00007ff030e70000)
liblber-2.4.so.2 => /usr/lib/x86_64-linux-gnu/liblber-2.4.so.2 (0x00007ff030c61000)
libgssapi.so.3 => /usr/lib/x86_64-linux-gnu/libgssapi.so.3 (0x00007ff030a23000)
libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007ff03081f000)
libresolv.so.2 => /lib/x86_64-linux-gnu/libresolv.so.2 (0x00007ff030604000)
libstdc++.so.6 => /usr/lib/x86_64-linux-gnu/libstdc++.so.6 (0x00007ff030300000)
libm.so.6 => /lib/x86_64-linux-gnu/libm.so.6 (0x00007ff02fffa000)
libgcc_s.so.1 => /lib/x86_64-linux-gnu/libgcc_s.so.1 (0x00007ff02fde4000)
libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007ff02fbc6000)
libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007ff02f7fd000)
libsasl2.so.2 => /usr/lib/x86_64-linux-gnu/libsasl2.so.2 (0x00007ff02f5e2000)
```
If any dependency is missing, then you might get error as shown below.
```bash
ldd /opt/safesquid/bin/safesquid
linux-vdso.so.1 =>  (0x00007ffebebdb000)
libldap_r-2.4.so.2 => /usr/lib/x86_64-linux-gnu/libldap_r-2.4.so.2 (0x00007ff03107e000)
libpam.so.0 => /lib/x86_64-linux-gnu/libpam.so.0 (0x00007ff030e70000)
liblber-2.4.so.2 => /usr/lib/x86_64-linux-gnu/liblber-2.4.so.2 (0x00007ff030c61000)
libgssapi.so.3 => /usr/lib/x86_64-linux-gnu/libgssapi.so.3 (0x00007ff030a23000)
libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007ff03081f000)
libresolv.so.2 => /lib/x86_64-linux-gnu/libresolv.so.2 (0x00007ff030604000)
libstdc++.so.6 => /usr/lib/x86_64-linux-gnu/libstdc++.so.6 (0x00007ff030300000)
libgmp.so.3==> not found
libm.so.6 => /lib/x86_64-linux-gnu/libm.so.6 (0x00007ff02fffa000)
libgcc_s.so.1 => /lib/x86_64-linux-gnu/libgcc_s.so.1 (0x00007ff02fde4000)
libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007ff02fbc6000)
libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007ff02f7fd000)
libsasl2.so.2 => /usr/lib/x86_64-linux-gnu/libsasl2.so.2 (0x00007ff02f5e2000)
```

If you notice that any of the dependencies are not present then, you should install that dependenies to make SafeSquid work.

# Start the SafeSquid

Further you need to Start the SafeSquid service by using below command
```bash
/etc/init.d/safesquid start
```

# Testing

You can check whether SafeSquid service is running or not by using these commands.
```bash
pidof safesquid   
```
OR         
```bash
netstat -tulnp | grep "safesquid"
```
Status check.jpg

By default SafeSquid will listen on PORT 8080. If you observe SafeSquid is listening on any one of the ports shown in the image, then its confirm that SafeSquid has started.
Note : This installation does not include the Monit and Bind configurations.

# See Also

1. [Monit configuration for SafeSquid Monitoring]()
2. [Bind configuration in SafeSquid Server]()
3. [Configure HTTPS inspection]()
4. [Integrate AD or OpenLDAP with SafeSquid]() 
