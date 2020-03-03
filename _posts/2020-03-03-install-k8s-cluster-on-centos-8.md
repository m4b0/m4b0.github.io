---
layout: post
title: "Install a Kubernetes Cluster on Red Hat CentOS 8"
tags: kubernetes k8s redhad centos
date: 2020-03-03
---

![Trailer image](https://cdn.thenewstack.io/media/2020/03/3ee82415-truck-1030846_640.jpg)

If you’ve migrated over from Red Hat’s 
[CentOS 7](https://www.centos.org/download/) to 
[CentOS 8](https://www.centos.org/), you’ve probably noticed a lot of changes have 
taken place. Many of those changes have caused admins to approach their tasks 
differently. Such is the case with installing Kubernetes. If you’re looking to deploy a 
Kubernetes cluster on CentOS 8, the changes made to the operating system will directly affect you.

In order to successfully install Kubernetes (and create a cluster), you’ll need at least two machines.

At the moment, Kubernetes cannot work with Podman (which is 
[now the default container engine](https://thenewstack.io/check-out-podman-red-hats-daemon-less-docker-alternative/) 
for both RHEL and CentOS). Because of this, you’ll need to install the docker engine. There is a bit 
of trickery to be had for this process.

Give it a try and see if it doesn’t become your go-to path for getting Kubernetes up and running on CentOS 8.

[Full article](https://thenewstack.io/how-to-install-a-kubernetes-cluster-on-red-hat-centos-8/)
