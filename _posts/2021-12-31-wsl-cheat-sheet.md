---
layout: post
title: Windows Subsystem for Linux (WSL) Cheat Sheet
author: Graham Garnsworthy
modified_date: 2022-01-22
---

This cheat sheet lists the commands I use most often when working with WSL and describes what I use them for.

![{{ page.title }}](/assets/img/wsl-feature.png)

## List available Linux distributions

Before you can install a specific distribution, you need to know which are available. The following command will list all the available distributions.

```
wsl --list --online
```

The output from running this command will look similar to the output shown below. In this case, the **Unbutu** distibution is denoted with a **\*** indicating it is the default distribution.

```
  NAME            FRIENDLY NAME
* Ubuntu          Ubuntu
  Debian          Debian GNU/Linux
  kali-linux      Kali Linux Rolling
  openSUSE-42     openSUSE Leap 42
  SLES-12         SUSE Linux Enterprise Server v12
  Ubuntu-16.04    Ubuntu 16.04 LTS
  Ubuntu-18.04    Ubuntu 18.04 LTS
  Ubuntu-20.04    Ubuntu 20.04 LTS
```

## Install a specific Linux distribution

To use the install command, you'll need to need to meet [Microsoft's prerequisites](https://docs.microsoft.com/en-us/windows/wsl/install#prerequisites).

> You must be running Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11.

Use the following command, replacing the `<DistributionName>` with the your required distribution name, to start the installation. Alternatively, if you want to install the default distribution, you can omit the `--distribution <DistributionName>` option.

```
wsl --install --distribution <DistributionName>
```

## Unregister a Linux distribution

Unregisters the distribution specified by `<DistributionName>` and deletes the root file system.

```
wsl --unregister <DistributionName>
```
