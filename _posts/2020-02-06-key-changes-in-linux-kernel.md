---
layout: post
title: 4 Key Changes in Linux Kernel 5.6
tags: linux kernel
date: 2020-02-06
---

![Linux image](https://i0.wp.com/itsfoss.com/wp-content/uploads/2020/02/linux-kernel-5.6.jpg?w=800&ssl=1)

**1**.- WireGuard Support
[WireGuard](https://itsfoss.com/wireguard/) 
will be added to Linux 5.6 – potentially replacing 
[OpenVPN](https://openvpn.net/) for a variety of reasons.

You can learn more about 
[WireGuard](https://www.wireguard.com/) on their official site to know the benefits. Of course, 
if you’ve used it, you might be aware of the reasons why it’s potentially better than OpenVPN.

**2**.- USB4 Support
Linux 5.6 will also include the support of USB4.

In case you didn’t know about USB 4.0 (USB4), you can read the 
[announcement post](https://www.usb.org/sites/default/files/2019-09/USB-IF_USB4%20spec%20announcement_FINAL.pdf).

**3**.- F2FS Data Compression Using LZO/LZ4
Linux 5.6 will also come with the support for F2FS data compression using LZO/LZ4 algorithms.

**4**.- Fixing the Year 2038 problem for 32-bit systems
Unix and Linux store the time value in a 32-bit signed integer format which has the maximum value 
of 2147483647. Beyond this number, due to integer overflow, the values will be stored as a negative number.

This means that for a 32-bit system, the time value cannot go beyond 2147483647 seconds 
after Jan. 1, 1970. In simpler terms, after 03:14:07 UTC on Jan. 19, 2038, due to integer 
overflow, the time will read as Dec. 13, 1901 instead of Jan. 19, 2038.

Linux kernel 5.6 has a fix for this problem so that 32-bit systems can run beyond the year 2038.

**5**.- Improved Hardware Support
Obviously, with the next release, the hardware support will improve as well. The plan to 
support newer wireless peripherals will be a priority too.

The new kernel will also add the support for MX Master 3 mouse and other wireless Logitech products.

In addition to Logitech products, you can expect a lot of different hardware support as 
well (including the support for AMD GPUs, NVIDIA GPUs, and Intel Tiger Lake chipset support).

**6**.- Other Changes
Also, in addition to all these major additions/support in Linux 5.6, there are several other 
changes that would be coming with the next kernel release:

- Improvements in AMD Zen temperature/power reporting
- A fix for AMD CPUs overheating in ASUS TUF laptops
- Open-source NVIDIA RTX 2000 “Turing” graphics support
- FSCRYPT inline encryption.

[Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=Linux-5.6-Spectacular) 
tracked a lot of technical changes arriving with Linux 5.6. So, if you’re curious about 
every bit of the changes involved in Linux 5.6, you can check for yourself.

[Full article](https://itsfoss.com/linux-kernel-5-6/)
