---
layout: post
title: "How to use cron in Linux"
tags: opensource cron linux sysadmin
date: 2020-04-04
---

![Penguins image](https://opensource.com/sites/default/files/styles/image-full-size/public/lead-images/linux-penguins.png?itok=yKOpaJM_)

The cron utility runs based on commands specified in a cron table (**crontab**).

```
# crontab -e
SHELL=/bin/bash
MAILTO=root@example.com
PATH=/bin:/sbin:/usr/bin:/usr/sbin:/usr/local/bin:/usr/local/sbin

# For details see man 4 crontabs

# Example of job definition:
# .---------------- minute (0 - 59)
# |  .------------- hour (0 - 23)
# |  |  .---------- day of month (1 - 31)
# |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
# |  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
# |  |  |  |  |
# *  *  *  *  * user-name  command to be executed

# backup using the rsbu program to the internal 4TB HDD and then 4TB external
01 01 * * * /usr/local/bin/rsbu -vbd1 ; /usr/local/bin/rsbu -vbd2

# Set the hardware clock to keep it in sync with the more accurate system clock
03 05 * * * /sbin/hwclock --systohc

# Perform monthly updates on the first of the month
# 25 04 1 * * /usr/bin/dnf -y update
```

The first three lines in the code above set up a default environment. The environment must be set to 
whatever is necessary for a given user because cron does not provide an environment of any kind. The 
**SHELL** variable specifies the shell to use when commands are executed. This example specifies the 
Bash shell. The **MAILTO** variable sets the email address where cron job results will be sent. These 
emails can provide the status of the cron job (backups, updates, etc.) and consist of the output you 
would see if you ran the program manually from the command line. The third line sets up the **PATH** 
for the environment. Even though the path is set here, I always prepend the fully qualified path to 
each executable.

The jobs in **cron.d** and **/etc/crontab** are system jobs, which are used usually for more than one 
user, thus, additionally the **username** is needed.  **MAILTO** on the first line is optional.

Regular users with cron access could make mistakes that, for example, might cause system resources 
(such as memory and CPU time) to be swamped. To prevent possible misuse, the sysadmin can limit user 
access by creating a **/etc/cron.allow** file that contains a list of all users with permission to 
create cron jobs. The root user cannot be prevented from using cron.

The directory **/etc/cron.d** is where some applications, such as 
[SpamAssassin](http://spamassassin.apache.org/) and 
[sysstat](https://github.com/sysstat/sysstat), install cron files. Because there is no spamassassin 
or sysstat user, these programs need a place to locate cron files, so they are placed in **/etc/cron.d**.

The **[anacron](https://en.wikipedia.org/wiki/Anacron)** program performs the same function as crond, 
but it adds the ability to run jobs that were skipped, such as if the computer was off or otherwise 
unable to run the job for one or more cycles. This is very useful for laptops and other computers that 
are turned off or put into sleep mode.

As soon as the computer is turned on and booted, anacron checks to see whether configured jobs missed 
their last scheduled run. If they have, those jobs run immediately, but only once (no matter how many 
cycles have been missed). For example, if a weekly job was not run for three weeks because the system 
was shut down while you were on vacation, it would be run soon after you turn the computer on, but only 
once, not three times.

The anacron program provides some easy options for running regularly scheduled tasks. Just install your 
scripts in the **/etc/cron.[hourly|daily|weekly|monthly]** directories, depending how frequently they need 
to be run.

The **@** character is used to identify shortcuts to cron. The list below, taken from the crontab(5) man page, 
shows the shortcuts with their equivalent meanings.

```
       @reboot    :    Run once after reboot.
       @yearly    :    Run once a year, ie.  "0 0 1 1 *".
       @annually  :    Run once a year, ie.  "0 0 1 1 *".
       @monthly   :    Run once a month, ie. "0 0 1 * *".
       @weekly    :    Run once a week, ie.  "0 0 * * 0".
       @daily     :    Run once a day, ie.   "0 0 * * *".
       @hourly    :    Run once an hour, ie. "0 * * * *".
```

These shortcuts can be used in any of the **crontab** files, such as those in **/etc/cron.d**.

For more information, the man pages for 
[cron](http://man7.org/linux/man-pages/man8/cron.8.html), 
[crontab](http://man7.org/linux/man-pages/man5/crontab.5.html), 
[anacron](http://man7.org/linux/man-pages/man8/anacron.8.html), 
[anacrontab](http://man7.org/linux/man-pages/man5/anacrontab.5.html), and 
[run-parts](http://manpages.ubuntu.com/manpages/zesty/man8/run-parts.8.html) all have excellent information 
and descriptions of how the cron system works.

[Full article](https://opensource.com/article/17/11/how-use-cron-linux)
