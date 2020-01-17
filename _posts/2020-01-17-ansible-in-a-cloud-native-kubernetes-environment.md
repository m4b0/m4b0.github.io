---
layout: post
title: Ansible in a cloud-native Kubernetes environment
tags: games research train brain
date: 2020-01-17
---

![Ansible logo](https://www.ansible.com/hs-fs/hubfs/Images/blog-social/blog_ansible-and-kubernetes-c.png?width=2048&name=blog_ansible-and-kubernetes-c.png)

*While Ansible can do almost everything for you, it may not be the right tool for every aspect 
of your infrastructure automation. Sometimes there are other tools which may more cleanly 
integrate with your application developers' workflows, or have better support from app vendors.*

![Ansible areas](https://www.ansible.com/hs-fs/hubfs/Images/blog-social/Ansible_cloud-native-venn-diagram.png?width=914&name=Ansible_cloud-native-venn-diagram.png)

Ansible fits into the processes for 
- Container Builds
- Cluster Management
- Application Lifecycles

Kubernetes can’t manage your entire application lifecycle, nor can it bootstrap itself; 
you should not settle for automating the inside of a Kubernetes cluster while using manual 
processes to build and manage your cluster; this becomes especially dangerous if you manage 
more than one cluster, as is best practice for most environments (at least having a staging 
and production cluster, or a private internal cluster and a public facing cluster).

For teams who already use Ansible, it's a no-brainer to migrate their existing Ansible knowledge, 
roles, modules, and playbooks into Kubernetes management playbooks and Ansible-based operators. 
For teams new to Ansible, its flexibility for all things related to IT automation (Networking, 
Windows, Linux, Security, etc.) and ease of use make it an ideal companion for cloud-native 
orchestration.

[Full article](https://www.ansible.com/blog/how-useful-is-ansible-in-a-cloud-native-kubernetes-environment)
