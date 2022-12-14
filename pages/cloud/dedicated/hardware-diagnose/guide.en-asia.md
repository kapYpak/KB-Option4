---
title: Hardware Diagnostics
slug: hardware-diagnostics
excerpt: This guide will show you how to diagnose hardware issues on your server.
section: Security
---

**Last updated 21st June 2018**

## Objective

At some point during the life of your server, you may encounter a fault due to a hardware issue. For these issues, your server is equipped with some diagnostic tools to help identify faulty hardware components.

**This guide will show you how to diagnose hardware issues on your server.**


## Requirements

* a [Dedicated Server](https://www.ovh.com/asia/dedicated-servers/){.external}
* [rescue mode activated](../ovh-rescue/){.external}


## Instructions

### Activate rescue mode

You can activate rescue mode by logging into your [OVHcloud control panel](https://ca.ovh.com/auth/?action=gotomanager&from=https://www.ovh.com/asia/&ovhSubsidiary=asia){.external}, and going to your server's page. Then go to `General information`{.action} > `Boot`{.action} and click the `ยทยทยท`{.action} button and click `Modify`{.action} button  to change the boot mode.

![General Information](images/rescue-mode-01_2020.png){.thumbnail}

On the next screen, select `Boot on rescue mode`{.action}. If your server has a Linux-based OS, select `rescue64-pro`{.action} from the dropdown list. If you have a Windows server, select `WinRescue`{.action}. Lastly, type your email address in the text field, then click `Next`{.action}.

![Change the Netboot](images/rescue-mode-03_2020.png){.thumbnail}

Confirm your options on the next screen, and then reboot your server to apply your changes. Your server will now reboot in rescue mode, and you will receive the credentials for logging in via the email address you provided. To exit rescue mode, simply change the boot mode back to `Boot on the hard disk`{.action}, then reboot your server.

![Reboot the server](images/rescue-mode-02_2020.png){.thumbnail}

### Use the web interface

Once your server has rebooted, you'll receive an email with your rescue mode access credentials. The email will also contain a link to the rescue mode web interface. The link usually looks like this: <https://your_servers_ip_address:444>.

After clicking the link, you be taken to the web interface, as shown below.

![Web interface](images/rescue-mode-04.png){.thumbnail}

### Run all hardware tests

From the top of the web interface, you can click the `Start all tests`{.action} button, which will run all available hardware tests simultaneously.

![Start all tests](images/rescue-mode-042.png){.thumbnail}

### Run separate hardware tests

The web interface allows you to run separate tests for:

- Processors
- Network connection
- Memory
- Disk partitions

You will also be able to view your server's SMART logs, which give you detailed hard disk information.

 
#### Processors

The processor test checks the working order of your server's processor, and needs about 30 minutes to run successfully. If the server crashes during this test, then it means that the processor is faulty.

To start the test, click the button as shown below.

![Processor test](images/processors.png){.thumbnail}

#### Network Connection
The network connection test checks your internal and external bandwidth. To start the test, click the button as shown below.

![Network test](images/network-connection.png){.thumbnail}

#### Memory

The memory test checks the integrity of your server's RAM modules. If the server crashes during this test, then it means that the one or more of your RAM modules is faulty.

To start the test, click the button as shown below.

![Memory test](images/memory.png){.thumbnail}

#### Disk Partitions

The partitions test is comprised of a disk access test and a file system check. The disk access test checks if the system can communicate with your server's hard drives. The file system check uses the `fsck -fy` command to check the entire file system.

> [!warning]
>
> Running a file system check on a damaged hard drive can result in data loss.
>

![Disk test](images/partitions.png){.thumbnail}

## Go further

Join our community of users on <https://community.ovh.com/en/>.
