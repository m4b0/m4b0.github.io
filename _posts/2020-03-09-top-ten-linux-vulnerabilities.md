---
layout: post
title: "10 Linux/Open Source Vulnerabilities of All Time"
tags: security linux vulnerabilities
date: 2020-03-09
---

![Linux vulnerabilities image](https://www.datamation.com/imagesvr_ce/4182/10LinuxOpenSourceVulnerabilities_0.jpg)

Over the past decade, there have been a few high profile open source vulnerabilities, that made some 
substantial impact. All of the issues were patched in short order by the upstream projects, yet not 
every user patched quickly, leaving some exposed to risk.

# Heartbleed

![Heartbleed image](https://www.datamation.com/imagesvr_ce/4466/10LinuxOpenSourceVulnerabilities_1.jpg)

No conversation about open source vulnerabilities can be had without mentioning Heartbleed. Disclosed 
in 2014, the Heartbleed vulnerability was found in the open source OpenSSL cryptographic library and 
enabled attackers to exploit encrypted communications. 
[http://heartbleed.com/](http://heartbleed.com/)

# ShellShock

![ShellShock image](https://www.datamation.com/imagesvr_ce/5367/10LinuxOpenSourceVulnerabilities_2.jpg)

Also disclosed in 2014, the Shellshock vulnerability was particularly impactful, exposing a risk in 
the BASH (Bourne Again Shell) that could have enabled an attacker to inject and execute arbitrary 
commands on a vulnerable server. 
[http://www.gnu.org/software/bash/](http://www.gnu.org/software/bash/)

# CVE-2014-7188 The Flaw that Rebooted the Public Cloud

![Rebooted image](https://www.datamation.com/imagesvr_ce/8180/10LinuxOpenSourceVulnerabilities_3.jpg)

While some vulnerabilities are publicly reported before most users get the chance to patch, that 
wasn't the case with CVE-2014-7188, which was a critical flaw in the Xen hypervisor. Xen at the 
time of the flaw's disclosure (2014), was the primary virtualization tool for multiple public 
cloud providers, including Amazon. Thanks to a well executed private disclosure process, the cloud 
providers were all able to patch and reboot their clouds, before users were put at risk.

# Apache Struts CVE-2017-5638 - The Flaw that Breached Equifax

![Struts image](https://www.datamation.com/imagesvr_ce/2720/10LinuxOpenSourceVulnerabilities_4.jpg)

In 2017, the open source Apache Struts project reported CVE-2017-5638 which is a remote code 
execution (RCE) flaw. Failure to patch the flaw was cited by Equifax as the root cause that 
enabled attackers (identified by the U.S Department of Justice in 2020 as being from China) to 
exploit Equifax, exposing hundreds of millions of Americans to risk.

# Dirty Cow

![Dirti cow image](https://www.datamation.com/imagesvr_ce/9507/10LinuxOpenSourceVulnerabilities_5.jpg)

Dirty COW (Copy On Write) is a Linux privilege escalation vulnerability formally disclosed in 2016 as 
CVE-2016-5195. According to the bug disclosure, "an unprivileged local user could use this flaw to gain 
write access to otherwise read-only memory mappings and thus increase their privileges on the system." 
[https://dirtycow.ninja/](https://dirtycow.ninja/)

# GHOST

![Ghost image](https://www.datamation.com/imagesvr_ce/2521/10LinuxOpenSourceVulnerabilities_6.jpg)

GHOST (gethostbyname) CVE-2015-0235 is a vulnerability in the open-source Linux GNU C Library (glibc). 
While it could have potentially enabled an attacker to execute arbitrary code, the actual impact of the 
flaw was mitigated by other controls in Linux.

# CARPE DIEM

![Carpe diem image](https://www.datamation.com/imagesvr_ce/3247/10LinuxOpenSourceVulnerabilities_7.jpg)

One of the most widely deployed open source technologies is the Apache HTTPD web server. In 2019, 
CVE-2019-0211 was reported and given the name CARPE DIEM. CARPE: stands for CVE-2019-0211 Apache Root 
Privilege Escalation; and DIEM is because the exploit triggers once a day.

# Samba CVE-2017-7494

![Samba image](https://www.datamation.com/imagesvr_ce/8006/10LinuxOpenSourceVulnerabilities_8.jpg)

The CVE-2017-7494 flaw in the widely deploy Samba file sharing server was disclosed around the same 
time as the EternalBlue flaw in Windows that led to the WannaCry ransomware attack. Though different 
then EternalBlue, the Samba flaw similarly is a remote code execution issued that could have enabled 
an attacker to execute a worm or ransomware attack.

# Spectre/ Meltdown

![Spectre/meltdown image](https://www.datamation.com/imagesvr_ce/8181/10LinuxOpenSourceVulnerabilities_9.jpg)

Neither Spectre or Meltdown are 'pure' open source vulnerabilities though they have had widespread 
impact on open source system. Spectre and Meltdown are CPU flaw first disclosed in 2017 that could 
be exploited by code running in an operating system. Linux vendors and kernel developers have been 
scrambling every since to patch and fix the seemingly endless stream of variants.

# SUDO CVE-2019-14287

![Sudo image](https://www.datamation.com/imagesvr_ce/8994/10LinuxOpenSourceVulnerabilities_10.jpg)

Sudo (short for Super User Do) is a primary tool in Linux giving users super user permissions to execute 
administrative actions. With CVE-2019-14287, Sudo restrictions could potentially be bypassed giving an 
attacker full access to a vulnerable system.

[Full article](https://www.datamation.com/applications/slideshows/10-linuxopen-source-vulnerabilities-of-all-time.html)
