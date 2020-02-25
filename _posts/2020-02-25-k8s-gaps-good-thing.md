---
layout: post
title: "Gaps in Kubernetes Are Really a Good Thing"
tags: image sierra madre durango oceano pacifico petatlan guerrero
date: 2020-02-25
---

![Sky stars image](https://cdn.thenewstack.io/media/2020/02/f8919645-network-4851079_1920-1024x640.jpg)

Kubernetes allows users to choose from an open ecosystem of application management and infrastructure 
options and under the stewardship of the Cloud Native Computing Foundation 
([CNCF](https://www.cncf.io/)), Kubernetes has become the new Linux.

One of the reasons  Kubernetes has become the de facto choice for container orchestration is because 
of what it does not offer.

Why?

In order to support a variety of use cases, early Kubernetes developers added intentional gaps to the 
platform in order to offer flexibility to its users. Rather than being a do-it-all platform, Kubernetes 
is designed to be an extensible platform that users and vendors can tailor their environments easily 
with custom resources definitions 
([CRDs](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/)), 
the Container Storage Interface 
([CSI](https://kubernetes.io/blog/2019/01/15/container-storage-interface-ga/)) and the 
Container Networking Interface 
([CNI](https://kubernetes.io/docs/concepts/cluster-administration/networking/)) based on their own 
requirements. The intentional gaps in Kubernetes offer flexibility in both infrastructure and application 
layers.

*Building Blocks of the Cloud Native Environment*
![Building blocks of cloud native environment image](https://cdn.thenewstack.io/media/2020/02/8df4ec2c-screen-shot-2020-02-24-at-22.39.47-1024x577.png)

Kubernetes is clearly the best platform for container orchestration and is designed to run in any 
environment. However, the principles based on which Kubernetes is built also makes it challenging 
to get it up and running out-of-the-box. The resulting challenge is there are many intentionally 
added gaps in Kubernetes left for the community and vendors to solve.

When adopting Kubernetes in an organization, it is thus important to consider how to minimize the 
required time, effort and cost with infrastructure and application management that can meet a holistic 
set of requirements. An integrated approach is one way to deliver faster time-to-value while ensuring 
all these gaps are filled.

[Full article](https://thenewstack.io/why-those-gaps-in-kubernetes-are-really-a-good-thing/)
