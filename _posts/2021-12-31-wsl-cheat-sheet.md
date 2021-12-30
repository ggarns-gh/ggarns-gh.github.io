---
layout: post
title: Windows Subsystem for Linux (WSL) Cheat Sheet
author: Graham Garnsworthy
modified_date: 2022-01-01
---

![{{ page.title }}](/assets/img/wsl-feature.png)

The following commands are those I use most often when working with WSL. They can be run from either the Windows Command Prompt or from a PowerShell terminal.

## List available Linux distributions

Lists the available Linux distributions that can be installed.

```
wsl --list --online
```

The output from running this command will look similar to the output shown below.

```
NAME            FRIENDLY NAME
Ubuntu          Ubuntu
Debian          Debian GNU/Linux
kali-linux      Kali Linux Rolling
openSUSE-42     openSUSE Leap 42
SLES-12         SUSE Linux Enterprise Server v12
Ubuntu-16.04    Ubuntu 16.04 LTS
Ubuntu-18.04    Ubuntu 18.04 LTS
Ubuntu-20.04    Ubuntu 20.04 LTS
```

## Unregister a Linux distribution

Unregisters the distribution specified by `<DistributionName>` and deletes the root file system.

```
wsl --unregister <DistributionName>
```
