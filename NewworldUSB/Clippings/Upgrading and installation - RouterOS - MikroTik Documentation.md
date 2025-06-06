---
title: "Upgrading and installation - RouterOS - MikroTik Documentation"
source: "https://help.mikrotik.com/docs/spaces/ROS/pages/328142/Upgrading+and+installation"
author:
  - "[[Māris B.]]"
published:
created: 2025-06-05
description:
tags:
  - "clippings"
---
## ==Overview==

==MikroTik devices are preinstalled with RouterOS,== so installation is usually not needed, ==except in the case where installing RouterOS on an x86 PC or virtual instance CHR==. The upgrade procedure on already installed devices is straightforward.

## ==Upgrading==

## ==Version numbering==

RouterOS versions are numbered sequentially when a period is used to separate sequences, it does *not* represent a decimal point, and the sequences do *not* have positional significance. An identifier of 2.5, for instance, is not "two and a half" or "halfway to version three", it is the fifth second-level revision of the second first-level revision. Therefore v5.2 is older than v5.18, which is newer.

==RouterOS== versions are released in several "release chains": Long term, Stable, Testing, and Development. When upgrading RouterOS, ==you can choose a release chain from which to install the new packages.==

- ==**Long term**==: Released rarely, and includes only the most critical fixes, upgrades within one number branch do not contain new features. When a **Stable** release has been out for a while and seems to be stable enough, it gets promoted into the long-term branch, replacing an older release, which is then moved to the archive. This consecutively adds new features.
- **==Stable==**: Released every few months, including ==all tested new features and fixes.==
- **==Testing==**: Released ==every few weeks==, ==only undergoes basic internal testing==, and should not be used in production.
- **==Development==**: Released when necessary. Includes raw changes and is available for software enthusiasts for testing new features.

![](https://help.mikrotik.com/docs/download/attachments/328142/SoftwareReleaseSchema_2023-06-09.png?version=1&modificationDate=1686544613901&api=v2)

## ==Standard upgrade==

The package upgrade feature connects to the MikroTik download servers and checks if there is another RouterOS version for your device under the selected release channel. ==Can also be used for downgrading==, if you, for example, are using stable release at the moment, but changed the release channel to the long-term.

After clicking the *Check For Updates* button in ==QuickSet== (or in the System → Packages menu) the *Check ==For Updates*== window will open with the current or the latest changelog (if a newer version exists). If newer version exists, buttons  ==*Download* and *Download&Install* will appear.== By cicking the *Download* button a newest version will be downloaded (manual device reboot is required), by clicking  *Download&Install*, download will start, and after a successful download will reboot a device to install the downloaded packages.

The versions offered will depend on the selected release channel. Not all versions migh be available. It will not be possible to upgrade from an older version to the latest version in one go, when using check-for-updates approach. For example, if running RouterOS v6.x, even selecting the major release upgrade channel, called "Upgrade", you will only see v7.12.1 as the available version. You must first upgrade to that intermediate version and only then newer releases will be available in the channels. This intermediate step can be done using check for updates too, but you will simply have to repeat check for updates after the first update to the intermediate version.

If custom packages are installed, the downloader will take that into account and download all necessary packages.

==It is strongly recommended to upgrade the bootloader after RouterOS update==. To upgrade the bootloader, execute command " */system routerboard upgrade* " in CLI, followed by a reboot. Alternatively, navigate to the GUI System → RouterBOARD menu and click the "Upgrade" button, then reboot the device.

  

![](https://help.mikrotik.com/docs/download/attachments/328142/Quickset-upgrade.jpg?version=1&modificationDate=1570170624131&api=v2)

![](https://help.mikrotik.com/docs/download/attachments/328142/image-2023-5-18_16-2-46.png?version=1&modificationDate=1684414966705&api=v2)

==You can **automate** the upgrade process== by running a script in the system scheduler. This script queries the MikroTik upgrade servers for new versions, if the response received says "New version is available", the script then issues the upgrade command below. Important note, this will not work, if you are running it for the first time on a release that is older. It might not see latest versions as available, if you are running v6.x, you would first have to manually select the "Upgrade" channel to do a major release upgrade to v7.12.1 intermediate version, and only afterwards newer v7 releases will be visible in the upgrade channels.

`[admin@MikroTik] >/system package update check-for-updates once :delay 3s; :if ( [get status] = "New version is available") do={ install }`

## ==Manual upgrade==

You can upgrade RouterOS in the following ways:

- WinBox – drag and drop files to the Files menu
- WebFig - upload files from the Files menu
- FTP - upload files to the root directory

==It is strongly recommended to upgrade the bootloader after upgrading RouterOS. To upgrade the bootloader, execute command " */system routerboard upgrade*== " in CLI, followed by a reboot. Alternatively, navigate to the GUI System → RouterBOARD menu and click the "Upgrade" button, then reboot the device.

RouterOS cannot be upgraded through a serial cable. Only [RouterBOOT](https://help.mikrotik.com/docs/display/ROS/RouterBOOT#RouterBOOT-SimpleUpgrade) is upgradeable using this method.

### ==Manual upgrade process==

- First step - visit [www.mikrotik.com](http://www.mikrotik.com/) and head to the Software page, then choose the architecture of the system you have the RouterOS installed on (system architecture can be found in System → Resource section);
- Download the **routeros *(main)*** and extra packages that are installed on a device;
- Upload packages to a device using one of the previously mentioned methods:

**Menu:***/system/package/update install **ignore-missing*** command allows upgrading only the RouterOS main package, while omitting packages that are either missing or not uploaded during a manual upgrade process.

#### ==Using WinBox==

Choose your system type, and download the upgrade package. Connect to your router with WinBox, Select the downloaded file with your mouse, and drag it to the Files menu. If some files are already present, make sure to put the package in the root menu, not inside the hotspot folder! The upload will start.

![](https://help.mikrotik.com/docs/download/attachments/328142/image-2023-5-18_16-16-22.png?version=1&modificationDate=1684415782639&api=v2)

After it finishes - reboot the device. The New version number will be seen in the Winbox Title and in the Packages menu

#### Using FTP

- Open your favorite SFTP program (in this case it is [Filezilla](https://filezilla.sourceforge.net/)), select the package, and upload it to your router ([demo2.mt.lv](https://demo2.mt.lv/) is the address of my router in this example). note that in the image I'm uploading many packages, but in your case - you will have one file that contains them all
- if you wish, you can check if the file is successfully transferred onto the router (optional):

`[admin@MikroTik] >/file print Columns: NAME, TYPE, SIZE, CREATION-TIME #  NAME                  TYPE       SIZE     CREATION-TIME        0  routeros-7.9-arm.npk  package    13.0MiB  may/18/2023 16:16:18 1  pub                   directory           nov/04/2022 11:22:19 2  ramdisk               directory           jan/01/1970 03:00:24`

- reboot your router for the upgrade process to begin:
```
[admin@MikroTik] >/system reboot
Reboot, yes? [y/N]: y
```
- after the reboot, your router will be up to date, you can check it in this menu:
```
[admin@MikroTik] >/system package print
```
- if your router did not upgrade correctly, make sure you check the **log**
```
[admin@MikroTik] >/log print without-paging
```

## ==RouterOS local upgrade==

**Sub-menu:**`system/package/local-update/`

You can upgrade one or multiple MikroTik routers within your local network by using one device which have all needed packages. Feature is available from **7.17beta3** version in (system > packages local update) and will replace (system > auto update) feature. Here is a simple example with 3 routers (the same method works on networks with infinite numbers of routers):

Place needed packages under Files menu, on your main router:

**Optional**, you can set mirror device between main one, if not needed, skip this step:

- Choose Local Package Sources and enable Mirror device. Set Primary Server where the packages are located, 10.155.136.50. Check Interval **minimum** setting can be set to 00:07:12, at which device will connect using Winbox to a main device and check for packages.  
	If new packages are available, it will begin to download, please note download process is slow and may require some time when large amount of files are used. In case some failures, download will resume on next Check.

![](https://help.mikrotik.com/docs/download/attachments/328142/image-2024-10-18_7-27-54.png?version=1&modificationDate=1729225674731&api=v2)

- New "packs" folder is created, where mirror device will store packages:

![](https://help.mikrotik.com/docs/download/attachments/328142/image-2024-10-18_7-28-33.png?version=1&modificationDate=1729225713905&api=v2)

- Add new package source on device which will be updated, in this example we use mirror device 10.155.136.71:

![](https://help.mikrotik.com/docs/download/attachments/328142/image-2024-10-18_7-18-47.png?version=1&modificationDate=1729225127783&api=v2)

- Once you click Refresh in Local Update packages tab, device using Winbox will try to connect to source and check if there are new packages.

![](https://help.mikrotik.com/docs/download/attachments/328142/image-2024-10-18_7-20-0.png?version=1&modificationDate=1729225200347&api=v2)

- Choose packages and click download, after download completes device will be needed to reboot for update.

![](https://help.mikrotik.com/docs/download/attachments/328142/image-2024-10-18_7-29-43.png?version=1&modificationDate=1729225783122&api=v2)

- Use system/package/local-update/refresh to automate this in your scripts and tools fetch url= can be used to download packages from our web page, for example: tool/fetch url= [https://download.mikrotik.com/routeros/7.16.1/routeros-7.16.1-arm.npk](https://download.mikrotik.com/routeros/7.16.1/routeros-7.16.1-arm.npk)

## RouterOS upgrade using Dude

#### The Dude auto-upgrade

The dude application can help you to upgrade the entire RouterOS network with one click per router.

- Set type **RouterOS** and correct password for any device on your Dude map, that you want to upgrade automatically,
- Upload required RouterOS packages to Dude files
- Upgrade the RouterOS version on devices from the RouterOS list. The upgrade process is automatic, after a click on upgrade (or force upgrade), the package will be uploaded and the router will be rebooted by the Dude automatically.

#### The Dude hierarchical upgrade

For complicated networks, when routers are connected sequentially, the simplest example is "1router-2router-3router| connection. You might get an issue, 2router will go to reboot before packages are uploaded to the 3router. The solution is Dude Groups, the feature allows you to group routers and upgrade all of them with one click!

- Select the group and click Upgrade (or Force Upgrade),

When upgrading from older versions, there could be issues with your license key. Possible scenarios:

- When upgrading from RouterOS v2.8 or older, the system might complain about an expired upgrade time. To override this, use Netinstall to upgrade. Netinstall will ignore old license restrictions and will upgrade
- When upgrading to RouterOS v4 or newer, the system will ask you to update the license to a new format. To do this, ensure your Winbox PC (not the router) has a working internet connection without any restrictions to reach [www.mikrotik.com](https://www.mikrotik.com/) and click "update license" in the license menu.

## Netinstall

[NetInstall](https://help.mikrotik.com/docs/spaces/ROS/pages/24805390/Netinstall) is a widely-used installation tool for RouterOS. It runs on Windows systems or via a command-line tool, netinstall-cli, on Linux, or through Wine (with superuser permissions required).

The NetInstall utilities can be downloaded from the [MikroTik download section](https://www.mikrotik.com/download).

[NetInstall](https://help.mikrotik.com/docs/spaces/ROS/pages/24805390/Netinstall) is also used to re-install RouterOS in cases where a previous installation has failed, been damaged, or where access passwords have been lost.

To use NetInstall, your device must support booting from Ethernet, with a direct Ethernet connection between the NetInstall computer and the target device. All RouterBOARDs support PXE network booting, which can be enabled in the RouterOS "routerboard" menu (if RouterOS is accessible) or in the bootloader settings using a serial console cable.

**Note:** For RouterBOARD devices without a serial port or RouterOS access, you can activate PXE booting using the [Reset button](https://help.mikrotik.com/docs/spaces/ROS/pages/24805498/Reset+Button).

[NetInstall](https://help.mikrotik.com/docs/spaces/ROS/pages/24805390/Netinstall) can also directly install RouterOS onto a disk (USB/CF/IDE/SATA) connected to the NetInstall Windows machine. Once installed, simply transfer the disk to the Router machine and boot from it.

  
**Attention!** Do not try to install RouterOS on your system drive. Action will format your hard drive and wipe out your existing OS.

## CD Install

## RouterOS Package Types

Information about RouterOS packages can be found [here](https://help.mikrotik.com/docs/display/ROS/Packages)