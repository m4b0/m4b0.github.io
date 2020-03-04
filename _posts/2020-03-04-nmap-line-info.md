---
layout: post
title: "Nmap command line info gathering magic"
tags: sysadmin nmap security network
date: 2020-03-04
---

![Computer image](https://www.redhat.com/sysadmin/sites/default/files/styles/full/public/2020-02/business-computer-connection-contemporary-450035%20Cropped.jpg?itok=8ANNA9Hc)

Nmap and its associated files provide a lot of valuable information, but you have to know how to get it.

I've used Nmap for years, and I continue to discover new things about it. For example, recently I was teaching someone to scan a remote host for open TCP ports and then changed the default SSH port to one not detected during a default Nmap scan. To my surprise, after we changed the port, a typical, quick hacker-style scan readily revealed my attempt at security by obscurity. The problem is that I changed the default SSH port to 2222, and the change was detected. A quick Nmap probe scans the 1,000 most popular ports, which I assumed were the ones between 1 and 1024, with the 1,000 number being the computer 1,000 (1,024).

Surprise! I was wrong.

The fact is that Nmap does indeed use 1,000 ports for a quick scan, but the operative word in the description above is that it uses the 1,000 most popular ports for scans. The 1,000 most popular ports are not bound by the first 1,024 consecutive ports. The 1,000 ports are all over the place—ranging from one to 65389.

To view these one-thousand ports, use the following command:

> $ sudo nmap -sT --top-ports 1000 -v -oG -
>
> # Nmap 7.70 scan initiated Mon Feb  3 12:12:04 2020 as: nmap -sT --top-ports 1000 -v -oG -
> # Ports scanned: TCP(1000;1,3-4,6-7,9,13,17,19-26,30,32-33,37,42-43,49,53,70,79-85,88-90...

These are only the top 1,000 TCP ports. If you want to see the corresponding 1,000 UDP ports, use this command:

> $ sudo nmap -sU --top-ports 1000 -v -oG -
>
> # Nmap 7.70 scan initiated Mon Feb  3 12:51:41 2020 as: nmap -sU --top-ports 1000 -v -oG -
> # Ports scanned: TCP(0;) UDP(1000;2-3,7,9,13,17,19-23,37-38,42,49,53,67-69,80,88,111-113,120,123,135-139,158,161-162,177,192,199,207...

[Full article](https://www.redhat.com/sysadmin/nmap-info)
