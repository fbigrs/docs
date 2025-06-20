---
id: minecraft-custom-seed
title: "Minecraft: Configure Custom Seed"
description: Information about the configuration of a custom World Seed for your Minecraft server from ZAP-Hosting - ZAP-Hosting.com documentation
sidebar_label: Configure custom Seed
services:
  - gameserver
---

import InlineVoucher from '@site/src/components/InlineVoucher';

### What is a seed?

A seed in Minecraft is a code—usually a string of numbers or letters—that serves as the starting point for the game’s world generator. It determines the layout of terrain, structures, biomes, and resources in your world. While each seed produces a unique world, using the same seed with the same game version and world settings will always recreate the same world.

:::info
With a already existing world, the seed can not be changed. Seeds are responsible for world generation and only with a newly created world after the seed was configured, it will have an effect.
:::

<InlineVoucher />

### Enter your seed

First things first, stop your server and head over to your server.properties, the server configuration file. You can find it in the game server administration under Configs.

There, we search for the "level-seed=" line:

![](https://screensaver01.zap-hosting.com/index.php/s/58xmKGA8YwQkjZp/preview)

In the example, we have added "12345" as our seed. You would have to replace this with your custom seed you want to use ofcourse.

If you now want the seed to be active on the server, you have to create a new world. The easiest way for to achieve this, is to simply change the "level-name" option under "Settings".
You can enter a name name there simply like "world1".

You can also find a guide on recreating an existing world in our guide here: [Recreate World](minecraft-worlds.md#recreate-the-world)

Now start your server and you should see your new world with your custom seed.


