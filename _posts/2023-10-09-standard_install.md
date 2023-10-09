---
title: Standard Installation.
date: 2023-10-07 16:00:00 +05:30
categories: [getstarted,sab,setup]
tags: [setup]
---

# Standard Installation

The Standard Installation Mode is recommended, and the setup uses mostly pre-configured sub-choices.

![Standard Installation 1](Standard Installation 1.png)

## Network Autoconfigure

Press *Yes* If you want to use DHCP to automatically configure.

![Standard installation 2](Standard installation 2.png)

## DNS Search Domain

Type any domain name here. By default, it will take domain.local.

![Standard Installation 3](Standard Inastallation 3.png)

### Language Selection

Choose the language to be used for the installation process. English is selected as the default language. Change it only if you are not very comfortable with English.

![Language Selection](Language Selection.png)

### Country Selection

Select your country location which will used to set your time zone. This selection is related to ensure correct time settings of the system. Choose 'other' only if your location is not listed.

![Standard Installation 4](Standard Inastallation 4.png)

### Keyboard layout Selection

Select the keyboard layout that matches the origin of the keyboard attached to the system.

![Keyboard selection](Keyboard selection.png)

### Hostname of Your Server

Integration with your Active Directory Service requires proper assignment of the Fully Qualified Domain Name. It is therefore strongly recommended to carefully select the desired hostname for your secure web gateway. The default host name is SWG. You can give any hostname as per your choice other than safesquid.

![Standard Installation 5](Standard Inastallation 5.png)

### Choose the mirror of Ubuntu archive

Select the country to find a mirror of the ubuntu archive that is close to you on the network to download required packages.

![Standard Installation Mirror](Standard Inastallation Mirror.png)

You don’t need to add any HTTP proxy here. Leave this blank and press continue.

![Standard Installation mirror blank](Standard Installation mirror blank.png)

### Load Additional Component

All the required hardware and additional components details will be loaded automatically.

![Standard Installation additional](Standard Installation additional.png)

> **Note:** If you face any error while installing SafeSquid Appliance Builder (SAB-ISO), you will get debugging logs information by pressing ALT+F4. To return back to previous screen press ALT+F1.

### Configure the Clock

Using Yes or No you can configure the clock. You need to scroll down and search your continent and nearby locations time zone.

![Clock](Clock.png)

### Setting Up partitions

Installation will proceed with partitioning process required for SafeSquid automatically.

![Setting partition](Setting partition.png)

### Installation of base system

Installation will automatically install the base system. You have to wait for some time to finish the process completely.

![Installation of base system](Installation of base system .png)

### Configuring the apt

Installation will proceed with configuring apt packages one after the other in this part.

![Configuring the apt](Configuring the apt.png)

### Select and install software

Installation process will complete the OS installation in this part.

![Select and install software](Select and install software.png)

### Grub Boot Loader

![Standard Installation 11](Standard Inastallation 11.png)

### Finishing installation

Final process of finishing the installation is the last step where preseed file will be executed.

![Finishing installation](Finishing installation.png)

### Login to the Server

If you observe the screen by default it will give you username along with the password. You need to enter the same username and password for first login.

- **User name:** administrator
- **Password:** safesquid

![Name and password](Name and password.png)

You need to reset the password on the first login.

![Resetpassword](Resetpassword.png)

You land into console where SafeSquid SWG will be seen as shown below after successfully login.

![Admin1](Admin1.PNG)

---

> **Note1:** If you are doing standard installation on Physical machine using USB bootable pendrive, after installation has been completed with USB bootable pendive and initial login with administrator (sudo -i), run the following commands:

```shell
grub-install /dev/sda
update-grub
reboot
```
As soon as you remove the USB bootable pendrive, it should display a prompt for login.

> **Note:** The above commands are only required to run if it displays a blank screen after removing the USB bootable pendrive.

## Setting Up Two Network Cards for Static Addressing

First, find the name of the card using the command:

```shell
dmesg | grep -i network
```

You can also search for "eth" instead of "network".

In this case, configure two network cards, `eth0` and `eth1`:

```shell
[ 1.165623] e1000 0000:00:03.0: eth0: Intel(R) PRO/1000 Network Connection
[ 1.645478] e1000 0000:00:08.0: eth1: Intel(R) PRO/1000 Network Connection
```

Use the following command to find available network interfaces:

```shell
ifconfig
```

For `eth0`, it's already configured during SafeSquid Appliance Builder(SAB) installation.

To enable `eth1`, edit the network configuration:

```shell
vim /etc/network/interfaces
```

The file content:

```shell
# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

# The loopback network interface
auto lo
iface lo inet loopback

# The primary network interface
auto eth0
iface eth0 inet static
    address 192.168.223.101
    netmask 255.255.0.0
    network 192.168.0.0
    broadcast 192.168.255.255
    gateway 192.168.1.10

# The secondary network interface
auto eth1
iface eth1 inet static
    address 10.1.0.101
    netmask 255.255.0.0
    network 10.1.0.0
    broadcast 10.1.255.255
    gateway 10.1.0.100
```

To restart the `eth1` network interface:

```shell
service network-interface restart INTERFACE=eth1 
```
