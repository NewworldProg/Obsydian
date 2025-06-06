---
title: "Packages - RouterOS - MikroTik Documentation"
source: "https://help.mikrotik.com/docs/spaces/ROS/pages/40992872/Packages"
author:
  - "[[Unknown User (olga)]]"
published:
created: 2025-06-05
description:
tags:
  - "clippings"
---
## ==Summary==

==RouterOS features are separated in "packages", which are files with.npk extension==. Most of the features are ==combined in one ***routeros*** package==, but some features are separate. Installing the corresponding NPK package can enable specific features (like container, dude). ==Packages are provided only by MikroTik, and no 3rd parties are allowed to make them==. You can download extra packages separately from our download page, or, since v7.18, it is possible to add extra packages directly from your router.

## ==Minimum requirements==

==RouterOS requires only the system package to operate at bare minimum==, but for most devices normal operation and features are available when you install the "routeros" bundle package.  

In case of wireless devices, several wireless packages are available, depending on the hardware you are using:

- Starting from RouterOS 7.13, the ***routeros*** (system) package and one of the following wireless packages are needed for the basic operation of a simple home router.
	1. 802.11ax WiFi APs require radio drivers, which are provided by the ***wifi-qcom*** package (for RouterOS version before 7.13 it was called the *wifiwave2* package).
	2. Previous generation WiFi APs require a ***wireless*** package.

More information about which wireless package to use is available in the [Wireless manual](https://help.mikrotik.com/docs/spaces/ROS/pages/1409138/Wireless).

Other packages are optional and not required for a home router. Install them only if you are sure of their purpose.

## ==Installing packages==

#### ==Manual download==

To manually download and install extra packages, download the necessary package from the [MikroTik download](https://mikrotik.com/download) page, selecting the RouterOS section based on your device's architecture found in the System/Resources menu. Extract the archive and upload the required package to your router using any convenient method, and proceed to reboot the router.

#### ==Download directly from the router==

Since 7.18 it is possible to download/install extra packages directly from the router, using the *System Packages* section.

1. After executing the ***Check For Updates*** command, available packages will be listed in the  *Packages* list, but they will show up as disabled. The available package list comes from the MikroTik download server. Those packages are available, but not yet in your router (as indicated by the flags X (Disabled) and A (available).
2. To download an extra package, first, select package and click ***Enable***
3. To make the router download the package, click ***Apply Changes*** and the device will ask for a reboot

This feature is also shown in our [v7.18 announcement video](https://youtu.be/wJw50I7STck?si=nJUGdR8z3qjNv69H&t=22).

|  |  |  |  |
| --- | --- | --- | --- |
| ![](https://help.mikrotik.com/docs/download/thumbnails/40992872/packages1.png?version=1&modificationDate=1743574896732&api=v2) | ![](https://help.mikrotik.com/docs/download/thumbnails/40992872/packages2.png?version=1&modificationDate=1743574895808&api=v2) | ![](https://help.mikrotik.com/docs/download/thumbnails/40992872/packages3.png?version=1&modificationDate=1743574894869&api=v2) | ![](https://help.mikrotik.com/docs/download/thumbnails/40992872/packages4.png?version=1&modificationDate=1743574894459&api=v2) |

### ==Verification of install==

To make sure package is installed successfully, check the "Log" section after the device is rebooted. If the package is installed successfully, you will see a message about it. If there have been conflicts or some requirement is not met, this will be explained, so you can take further steps to rectify that.

![](https://help.mikrotik.com/docs/download/attachments/40992872/packages5.png?version=1&modificationDate=1743575012701&api=v2) ![](https://help.mikrotik.com/docs/download/attachments/40992872/error.png?version=1&modificationDate=1743575016550&api=v2)

### System packages

|  |  |
| --- | --- |
| **routeros-arm** (*arm*) | system package for arm devices |
| **routeros-arm** *(arm64)* | system package for arm64 devices |
| **routeros-mipsbe** (*mipsbe*) | system package for mipsbe devices |
| **routeros-mmips** (*mmips*) | system package for mmips devices |
| **routeros-smips** (*smips*) | system package for smips devices |
| **routeros-tile** (*tile*) | system package for tile devices |
| **routeros-ppc** (*ppc*) | system package for ppc devices |
| **routeros** (*x86, CHR*) | system package for x86 installations and CHR environment |

### Extra packages

|  |  |
| --- | --- |
| **calea** (*arm, arm64, mipsbe, mmips, tile, ppc, x86, CHR*) | Data gathering tool for specific use due to "Communications Assistance for Law Enforcement Act" in the USA |
| **container** *(arm, arm64, x86, CHR)* | [Container](https://help.mikrotik.com/docs/display/ROS/Container) implementation of Linux containers,allows users to run containerized environments within RouterOS |
| **dude** (*arm, arm64, mmips, tile, x86, CHR*) | [Dude](https://wiki.mikrotik.com/wiki/Manual:The_Dude) tool that allows monitoring of network environment |
| **extra-nic** (arm64) | arm64 CPU architecture, Network Interface Card(NIC) support, recommended for UEFI installation on non MikroTik boards |
| **gps** (*arm, arm64, mipsbe, mmips, tile, ppc, x86, CHR*) | [Global Positioning System](https://help.mikrotik.com/docs/display/ROS/GPS) devices support |
| **iot** (*arm, arm64, mipsbe, mmips, tile, ppc, x86, CHR*) | Enables:  - [MQTT](https://help.mikrotik.com/docs/display/ROS/MQTT) - [LoRa](https://help.mikrotik.com/docs/display/ROS/General+Properties) (for devices with LR8/9/2 miniPCie cards) - [Bluetooth](https://help.mikrotik.com/docs/display/ROS/Bluetooth) (for devices with Bluetooth chip) - [GPIO](https://help.mikrotik.com/docs/display/ROS/GPIO) (for devices with GPIO pins) - [Modbus](https://help.mikrotik.com/docs/pages/viewpage.action?pageId=61046813) (for devices with RS485 port) |
| **iot-bt-extra** (arm, arm64) | A package for ARM, ARM64 devices which enables the use of USB Bluetooth adapters (must support LE 4.0+).  ***note**:* Not all adapters were tested. We can not guarantee beforehand that a specific adapter will work. |
| **lora** *(arm, arm64, mipsbe, mmips, tile, ppc, x86, CHR)* | Dummy package for [Lora](https://help.mikrotik.com/docs/display/ROS/General+Properties) support. LoRa package is not obligatory anymore and is left only for compatibility reasons. LoRa functionality is moved into iot package. |
| **lte** *(mipsbe)* | Required package only for SXT LTE (RBSXTLTE3-7), which contains drivers for the built-in LTE interface. |
| **rose-storage** (*arm, arm64, tile, x86, CHR*) | Additional [enterprise data center functionality](https://help.mikrotik.com/docs/display/ROS/ROSE-storage) in RouterOS, support disk monitoring, improved formatting, RAIDs, rsync, iSCSI, NVMe over TCP, NFS, and improved SMB |
| **tr069-client**  (*arm, arm64, mipsbe, mmips, smips, tile, ppc, x86, CHR*) | [TR069 Client](https://help.mikrotik.com/docs/display/ROS/TR-069) package |
| **ups** (*arm, arm64, mipsbe, mmips, tile, ppc, x86, CHR*) | [APC ups management](https://help.mikrotik.com/docs/display/ROS/UPS) interface |
| **user-manager** (*arm, arm64, mipsbe, mmips, tile, ppc, x86, CHR*) | [MikroTik User Manager](https://help.mikrotik.com/docs/display/ROS/User+Manager) server for controlling Hotspot and other service users. |
| **wifi-qcom** (*arm, arm64*) | Mandatory driver package for 802.11ax interfaces. Introduced in 7.13. [Wifi CAPsMAN](https://help.mikrotik.com/docs/display/ROS/WiFi#WiFi-WiFiCAPsMAN) support comes with the system package. |
| **wifi-qcom-ac** (*arm*) | Optional [Wifi](https://help.mikrotik.com/docs/display/ROS/WiFi) driver package for compatible 802.11ac interfaces. Introduced in 7.13. |
| **wireless** (*arm, arm64, mipsbe, mmips, tile, ppc, x86, CHR*) | Utilities and drivers for managing WiFi (up to 802.11ac) and 60GHz wireless interfaces.   This package is bundled into RouterOS for versions up to 7.12. Starting with 7.13, it is a separate package.    The **wireless** package conflicts with  **wifi-qcom** and  **wifi-qcom-ac** packages - they cannot be active at the same time. |
| **zerotier** *(arm, arm64)* | Enables [ZeroTier](https://help.mikrotik.com/docs/display/ROS/ZeroTier) functionality |

## Working with packages

**Menu:***/system package*

Commands executed in this menu will take place only on restart of the router. Until then, the user can freely schedule or revert set actions.

|  |  |
| --- | --- |
| **disable** | schedule the package to be disabled after the next reboot. No features provided by the package will be accessible |
| **downgrade** | will prompt for the reboot. During the reboot process will try to downgrade the RouterOS to the oldest version possible by checking the packages that are uploaded to the router. |
| **enable** | schedule package to be enabled after the next reboot |
| **uninstall** | schedule package to be removed from the router. That will take place during the reboot. |
| **unschedule** | remove scheduled task for the package. |
| **print** | outputs information about the packages, like: version, package state, planned state changes, etc. |
| **update** | manages the *"check-for-updates"* channel and performs RouterOS upgrades |
| **apply-changes** | apply scheduled changes and reboot device |

**Menu:***/system/check-installation*

The "Check installation" function ensures the integrity of the RouterOS system by verifying the readability and correct placement of files. Its primary purpose is to confirm the health and status of your NAND/Flash storage.

**Menu:***/system/package/update install ignore-missing* command allows upgrading only the RouterOS main package, while omitting packages that are either missing or not uploaded during a manual upgrade process.

## ==Auto install==

It is also possible to **automatically** install packages after uploading them to the router with FTP or SFTP. The package file must be named with the extension \*.auto.npk. Once the file will be uploaded, router will automatically go into reboot in order to install the package.

".auto.npk" in the filename is mandatory for a package to be automatically installed.

## Examples

### Listing packages

*zerotier* package is disabled, but installed; *iot* package is available on the server, but has not been downloaded to the router and enabled; *dude* package is scheduled for uninstall.

`/system package print  Flags: X - DISABLED Columns: NAME, VERSION, SCHEDULED #    NAME      VERSION  SCHEDULED               0    dude      7.9      scheduled for uninstall 1 X  zerotier  7.9                              2    routeros  7.9  3 XA iot       7.9`

Uninstall package

`/system package uninstall dude; /system reboot;  Reboot, yes? [y/N]: `

Disable package

`/system package disable zerotier; /system reboot; Reboot, yes? [y/N]: `

Downgrade

`/system package downgrade; /system reboot; Reboot, yes? [y/N]:  ` 

Cancel uninstall or disable action

`/system package unschedule zerotier; /system package unschedule dude;`