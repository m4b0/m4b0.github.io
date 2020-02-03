---
layout: post
title: Troubleshoot Kubernetes with the power of tmux and kubectl
tags: kubernetes k8s tmux kubectl
date: 2020-02-03
---

![Working in a computer image](https://opensource.com/sites/default/files/styles/image-full-size/public/lead-images/OSDC_women_computing_4.png?itok=VGZO8CxT)

A kubectl plugin that uses tmux to make troubleshooting Kubernetes much simpler.

Kubernetes is a thriving open source container orchestration platform that offers 
scalability, high availability, robustness, and resiliency for applications. One 
of its many features is support for running custom scripts or binaries through its 
primary client binary, kubectl. Kubectl is very powerful and allows users to do 
anything with it that they could do directly on a Kubernetes cluster.

This is one of many examples from a 
[repository of common Kubernetes aliases](https://github.com/ahmetb/kubectl-aliases/blob/master/.kubectl_aliases) 
that shows one way to simplify functions in kubectl. For something simple like 
this scenario, an alias is sufficient.

To create something more powerful than a simple alias, you can use 
[kubectl plugins](https://kubernetes.io/docs/tasks/extend-kubectl/kubectl-plugins/). 
Plugins are like standalone scripts written in any scripting language but are 
designed to extend the functionality of your main command when serving as a 
Kubernetes admin.

[Tmux](https://opensource.com/article/19/6/tmux-terminal-joy) 
is a very powerful tool that many sysadmins and ops teams rely on to troubleshoot 
issues related to ease of operability—from splitting windows into panes for running 
parallel debugging on multiple machines to monitoring logs. One of its major 
advantages is that it can be used on the command line or in automation scripts.

Aliases are always helpful for simple troubleshooting in Kubernetes environments. 
When the environment gets more complex, a kubectl plugin is a powerful option for 
using more advanced scripting. There are no limits on which programming language 
you can use to write kubectl plugins. The only requirements are that the naming 
convention in the path is executable, and it doesn't have the same name as an 
existing kubectl command.

To read the complete code or try the plugins, check the 
[kube-plugins-github](https://github.com/abhiTamrakar/kube-plugins) 
repository.

[Full article](https://opensource.com/article/20/2/kubernetes-tmux-kubectl)
