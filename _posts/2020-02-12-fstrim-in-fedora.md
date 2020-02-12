---
layout: post
title: "Extend the life of your SSD drive with fstrim"
tags: ssd drive fstrim fedora
date: 2020-02-12
---

![Keyboard image](https://opensource.com/sites/default/files/styles/image-full-size/public/lead-images/linux_keyboard_desktop.png?itok=I2nGw78_)

A new systemd service to make your life easier.

Opensource.com’s Don Watkins first wrote about TRIM in his 2017 article 
["Solid-state drives in Linux: Enabling TRIM for SSDs."](https://opensource.com/article/17/1/solid-state-drives-linux-enabling-trim-ssds)

**A new TRIM service**

A systemd service for TRIM exists. Fedora 
[introduced](https://fedoraproject.org/wiki/Changes/EnableFSTrimTimer) this into their 
distribution in version 30, and, although it is not enabled by default in versions 30 and 31, 
it is planned to be in version 32. If you’re working on Fedora Workstation 31 and you want 
to begin using this feature, you can enable it very easily. I’ll also show you how to test 
it below. This service is not unique to Fedora. The existence and status will depend on an 
individual distribution basis.

This service seems like the best way to run TRIM on your drives. It is much simpler than 
having to create your own crontab entry to call the fstrim command. It is also safer not 
having to edit the fstab file. It has been interesting to watch the evolution of solid-state 
storage technology and nice to know that it appears Linux is moving toward a standard and 
safe way to implement it.

[Full article](https://opensource.com/article/20/2/trim-solid-state-storage-linux)
