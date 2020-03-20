---
layout: post
title: "Create a Kubernetes security policy"
tags: kubernetes k8s security policy
date: 2020-03-20
---

![Kubernetes image](https://tr4.cbsistatic.com/hub/i/r/2018/11/08/3d1a9132-f650-4780-a34b-e103bdd1bb3e/resize/770x/56f18e5a7ddbabdf443a10d189b762b6/kuberneteshero.jpg)

[Kubernetes](https://www.techrepublic.com/article/what-is-kubernetes/) is an incredibly powerful container 
management tool. If you've worked with containers long enough, you know that security has to take a central 
role in the deployment of your apps and services. Without locking down those containers, havoc could be 
wreaked on your network.

**What is a pod?**
If you're new to Kubernetes, you might not know what a pod is. Simply stated, a Kubernetes pod is a collection of processes that make up a container, such as:

- Storage resources
- Unique network IP address
- Options that govern how the container should run

In other words, a pod is a unit of deployment--either a single container or a number of containers working together.

**What is a pod security policy?**

The Kubernetes pod security policy is a resource that controls the security of a pod specification. Using 
the PodSecurityPolicy object definition, you can control things like:

- The ability to run privileged containers
- Privilege escalation
- Access to volume types
- Access to host file systems
- Usage of host networking 

But how to define the policy? As with almost everything in Kubernetes, this is defined within a YAML file.

[Full article](https://www.techrepublic.com/article/how-to-create-a-kubernetes-security-policy/)
