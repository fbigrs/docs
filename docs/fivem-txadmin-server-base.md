---
id: fivem-txadmin-server-base
title: "FiveM: txAdmin Import Server Base"
description: Information on how to import your own server base into a FiveM txAdmin Server - ZAP-Hosting.com documentation
sidebar_label: txAdmin Base Import
services:
  - gameserver
---

import InlineVoucher from '@site/src/components/InlineVoucher';


## Introduction

txAdmin is a completely free to use, full-featured web panel to Manage & Monitor your FiveM server. It offers a wide range of features designed to make managing a FiveM server as easy as anything. In the following, we will introduce you to the txAdmin interface, highlighting its features and explaining exactly what you can do with it.

![img](https://screensaver01.zap-hosting.com/index.php/s/YrRXBNBX2xTnRyJ/preview)

<InlineVoucher />

## Preparing the Server

The best way to get started, is to have a freshly installed txAdmin Server. This means, no active Recipe or Resources running on the server yet, the Server should be in "setup mode".
When you log into txAdmin, you should see the following:
INSERT SCREENSHOT FROM SETUP PAGE

## Uploading your Server Base

IMPORTANT: Your server base should include a resources folder, server.cfg and if the base needs a MySQL Database, also a .sql file for the import of the Database Structure

In the next step, we have to upload our Server base. Access the Server for this via FTP. 
If you are logged in via FTP, enter the "gta5-fivem-txadmin" folder, you should now see the following:

![img](https://screensaver01.zap-hosting.com/index.php/s/N9AtaKrydLRk5Sy/preview)

At this location, create a new folder. You can name the folder whatever you want, in this example, we will use "myserver" as the folder name. It should look like this:

![img](https://screensaver01.zap-hosting.com/index.php/s/FA3A5WXZytJjKBX/preview)

Now, enter the newly created folder, it should be completely empty. Inside this folder, you will now upload your "resources" folder from your server base, and your included server.cfg.
After the upload, the "myserver" folder should look like this:

![img](https://screensaver01.zap-hosting.com/index.php/s/FQNmPJ4DKLxkS6Y/preview)

## Finish the Setup in txAdmin

We now have to finish the setup in txAdmin, and let the server know what resources it should use.
For that, we log into txAdmin. The credentials for that can be found on your servers Dashboard.

![img](https://screensaver01.zap-hosting.com/index.php/s/wzcQqB3MY7k28rZ/preview)

### Setup

Now that you have successfully logged in, you can start setting up txAdmin and your server. You should now see the txAdmin homepage (Dashboard). In the top left corner, you will notice a message indicating that your server still needs to be configured. Click on **Go to the setup page** to begin the setup process.

![img](https://screensaver01.zap-hosting.com/index.php/s/oXakf3qoJaim7ex/download)

### Welcome and server name

Next, define a server name that you would like to use for your project. This name is not intended for the server list but is solely for use within the txAdmin interface and for chat/Discord messages.

![img](https://screensaver01.zap-hosting.com/index.php/s/FCmd5xQ89wSPHfe/preview)

### Deployment Type

Under Deployment Type, you now need to choose how you would like to set up your server. You have the following options: **Popular Recipes**, **Existing Server Data**, **Remote URL Template**, and **Custom Template**. For our use case we choose **Existing Server Data**

![img](https://screensaver01.zap-hosting.com/index.php/s/52HfyJSNLscApNE/preview)

### Selecting the Paths

We now have to specify the path of our uploaded resources, first copy and enter the path you can see above the field and which is marked red in this screenshot:

![img](https://screensaver01.zap-hosting.com/index.php/s/BgtBTjDJKorR8XT/preview)

The only thing we have to add there, is the folder you created at the beginning on your FTP, which in our case is "myserver".
After that is done, it should look like this:

![img](https://screensaver01.zap-hosting.com/index.php/s/nkoCR2kxCpGTHHY/preview)

Now, we simply press "Next" and then "Save".

### Adjusting the server.cfg

#### IP Configuration

After pressing "Save", you will most likely receive an Error like this:

![img](https://screensaver01.zap-hosting.com/index.php/s/doXSaTGpKYFogMR/preview)

This is normal, because the server base was built for a different IP. We simply copy the 2 lines and add them at the top of our server.cfg

![img](https://screensaver01.zap-hosting.com/index.php/s/i77BWRx73rKqsGa/preview)

Please make sure, after adding the 2 new lines at the top of the server.cfg, that you check over your server.cfg and remove every other line that starts with "endpoint_add_*"

#### Onesync

We also have to remove any lines in the server.cfg that handle "onesync", so if you see something like "set onesync on", remove that aswell.
Afterwards, simply press "Save" again in txAdmin.

#### Licensekey

While editing the server.cfg, please also adjust the "sv_licenseKey" line and add your own licensekey behind it. If you need help with your own licensekey, you can check out our guide: LICENSEKEYGUIDE

#### Finish

Now, we just press "Save & Start Server"

![img](https://screensaver01.zap-hosting.com/index.php/s/npwBepWP4W9Edop/preview)