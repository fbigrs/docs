---
id: vserver-linux-java
title: "VPS: Installation of Java"
description: Information on how to install Java on your server from ZAP-Hosting - ZAP-Hosting.com documentation
sidebar_label: Install Java
services:
  - vserver
---

import InlineVoucher from '@site/src/components/InlineVoucher';

## Introduction

Java is a very popular programming language that is used worldwide for numerous programs and services. To run these programs based on Java it is absolutely necessary that Java is installed on the system. In the following you will learn how to install Java on your system for the offered Linux operating systems. 

<InlineVoucher />

## Preparation

Before starting the actual Java installation, it is important to make sure that the system is up to date. For this we connect to the server via SSH. If you don't know what SSH is and how to use it, please have a look at the following guide: [Initial access (SSH)](vserver-linux-ssh.md)

Once there, the system can be updated with the following command, depending on the operating system:

```
// Debian
sudo apt-get update

// Ubuntu
sudo apt update

// CentOS
sudo yum update

// OpenSUSE
sudo zypper up

// Fedora
sudo dnf upgrade --refresh
```



## Installation

After finishing the preparation, the Java installation can now be started. Depending on the operating system, the following commands must be executed:

**Debian**

```
sudo apt-get install default-jdk
```

**Ubuntu**

```
sudo apt install default-jdk
```

**CentOS**

```
sudo yum install java-11-openjdk
```

**Fedora**

```
sudo dnf install java-11-openjdk
```



## Version-Check

You can check if the installation was successful with the **java --version** command. The output should look similar to the following:

```
openjdk 11.0.9.1 2020-11-04
OpenJDK Runtime Environment (build 11.0.9.1+1-Ubuntu-0ubuntu1.20.04)
OpenJDK 64-Bit Server VM (build 11.0.9.1+1-Ubuntu-0ubuntu1.20.04, mixed mode)
```

## Conclusion

Congratulations, you have successfully installed and configured Java! If you have any further questions or problems, please contact our support team, who are available to help you every day! 


