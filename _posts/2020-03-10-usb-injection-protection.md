---
layout: post
title: "USB Keystroke Injection Protection"
tags: usb keystroke injection protection security
date: 2020-03-10
---

![Lock image](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSOCzlO6oc5XHqtbEdqeQ5BWjziWrq0smDczNpsTcLYOJnGbF4K)

USB keystroke injection attacks have been an issue for a long time—problematic and affordable, due to 
the availability and price of keystroke injection tools. Those attacks send keystrokes immensely fast, 
in a human eyeblink, while being effectively invisible to the victim. Initially proposed to ease system 
administrator tasks, attackers learned how to use this technology for their purpose and compromise user systems. 

To make the life of an attacker harder, we propose a tool that measures the timing of incoming keystrokes 
and determines if it is an attack based on predefined heuristics (without a user being involved in the decision).

The tool offers two different modes of operation: `MONITOR` and `HARDENING`. When running it in monitoring 
mode it won’t block a device that was classified as malicious, but will write a log line with information 
about the device to `syslog`. If it is run in hardening mode, it will immediately block a device that was 
classified as malicious/attacking. Out of the box, the tool is shipped in `HARDENING` mode.

If the tool is running in monitoring mode, it logs information to the syslog. For one time inspection, this 
log can be read by simply using `journalctl`:

```
journalctl -u ukip.service
```

**Getting it up and running**

The [README](https://github.com/google/ukip#installation-prerequisites) on Github contains a step-by-step guide 
to prepare the tool, set it up and run it as a 
[systemd daemon](https://wiki.archlinux.org/index.php/systemd), that is enabled on reboot. Over time it may be 
necessary to revise the variables for the tool by simply adjusting the values on top of `/usr/sbin/ukip` and 
restarting of the daemon:

```
sudo systemctl restart ukip.service
```

**A note on silver bullets**

The tool is not a silver bullet against USB-based attacks or keystroke injection attacks, since an attacker 
with access to a user’s machine (required for USB-based keystroke injection attacks) can do worse things if 
the machine is left unlocked. The tool is meant to provide another layer of protection and to defend a user 
sitting in front of their unlocked machine by them seeing the attack happening. They are able to see the 
attack either because the keystrokes are delayed enough to circumvent the tool’s logic or fast enough to be 
detected by it, i.e., blocking the device by unbinding its driver and logging information to syslog.

Keystroke injection attacks are difficult to detect and prevent since they’re delivered over USB (the most 
widely used computer peripheral connector) and require a Human Interface Device Driver (available on likely 
every operating system for mouse and keyboard input). The proposed tool raises the bar making it more 
difficult for the attacker while removing the user in the decision about whether a device is malicious or 
benign, apart from the refinement of the heuristic variables mentioned above. The tool can be complemented 
with other Linux tools, such as fine-grained udev rules or open source projects like 
[USBGuard](https://usbguard.github.io/), to make successful attacks more challenging. The latter lets users 
define policies and allow/block specific USB devices or block USB devices while the screen is locked. That 
feature is specifically useful, since an attacker could plug in a device while the user is away from their 
keyboard and launch an attack once they are back. With USBGuard in place, the device would need to be 
replugged when the system is unlocked to work correctly.

[Full article](https://opensource.googleblog.com/2020/03/usb-keystroke-injection-protection.html)
