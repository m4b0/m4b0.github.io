---
layout: post
title: "Restricted Shell to limit user access"
tags: restricted shell security
date: 2020-02-21
---

![Restricted shell image](https://tr3.cbsistatic.com/hub/i/r/2020/02/13/c93f67d5-5e9b-4330-bdea-287cfea26423/resize/770x/f8b751f8663f503a09345df8d527ca4d/rbash-error.jpg)

Learn how to prevent Linux users from executing certain commands and confining them to their 
home directory by employing rbash.

You have users logging in to your Linux system. Those users might have not have sudo rights, but 
they quite possibly could have free rein to poke around most of the system directory tree. You 
don't want that. Why? Although those users might not be able to edit the vast majority of your 
configuration files, you certainly don't want those users viewing them. Same holds true for your 
client data--you want that locked down.

But how do you prevent users from being able to access your directory hierarchy without having to 
tweak the permissions of every file and folder on the system, which could seriously complicate things?

One way is by employing a tool called Restricted Bash (rbash).

[Full article](https://www.techrepublic.com/article/how-to-use-restricted-shell-to-limit-user-access-to-a-linux-system/)
