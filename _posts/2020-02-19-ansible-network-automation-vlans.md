---
layout: post
title: "Ansible network automation, vlans resource modules"
tags: ansible network automation vlans modules
date: 2020-02-19
---

![Ansible logo image](https://www.ansible.com/hs-fs/hubfs/Images/blog-social/ansible-blog_network-gray.png?width=1024&name=ansible-blog_network-gray.png)

In October of 2019, as part of Red Hat Ansible Engine 2.9, the Ansible Network Automation team 
[introduced the concept of resource modules](https://www.ansible.com/blog/network-features-coming-soon-in-ansible-engine-2.9). 
These opinionated network modules make network automation easier and more consistent for those 
automating various network platforms in production.  The goal for resource modules was to avoid 
creating overly complex jinja2 templates for rendering network configuration. This blog post goes 
through the eos_vlans module for the Arista EOS network platform.

There are currently **three ways to push configuration using resource modules**.  These are the **merged**, 
**replaced** and **overridden** parameters. These allow much more flexibility for network engineers to adopt 
automation in incremental steps.  We realize that most folks will start with the merged parameter as 
they gain familiarity with the new resource module concepts. Over time organizations will move towards 
the overridden parameter as they adopt a standard SoT (source of truth) for their data models, 
wherever they reside.

[Full article](https://www.ansible.com/blog/deep-dive-on-vlans-resource-modules-for-network-automation)
