---
layout: post
title: "Kubernetes For Your DevOps Pipeline"
tags: kubernetes k8s devops pipeline
date: 2020-02-11
---

![Kubernetes pipeline image](https://rancher.com/img/featured-images/featured-images_ci-cd.png)

Kubernetes has seen an incredible rise over the past few years as organizations 
leverage containers for complex applications, micro-services and even cloud-native 
applications. And with the rise of Kubernetes, DevOps has gained more traction. While 
they may seem very different — one is a tool and the other is a methodology — they work 
together to help organizations deliver fast. This article explains why Kubernetes is 
essential to your DevOps strategy.

From a technology point of view, DevOps typically focuses on CI/CD (continuous integration 
and continuous delivery or continuous deployment). Here is a quick explanation:

- **Continuous integration**: developers make constant updates to source code within a 
shared repository, which is then scanned and checked by an automated build, allowing teams 
to detect problems early.

- **Continuous deployment**: once approved, code is released into production, resulting in 
many production deployments every day.

- **Continuous delivery**: software is built and can be released at any time – but by a 
manual process

Kubernetes allows organizations to run applications within containers in a distributed 
manner. It also handles scaling, resiliency and availability. Additionally, Kubernetes 
provides:

- Load balancing
- Ability to provide access to storage (persistent and non-persistent)
- Service discovery
- Automated rollouts, upgrades and rollbacks
- Role-based access control (RBAC)
- Security controls for running applications within the platform
- Extensibility to leverage a large and growing ecosystem to support DevOps

**The Kubernetes DevOps Connection**

By now we can start to see a correlation between DevOps teams creating applications 
and running containers and needing an orchestration engine that keeps them running at 
scale. This is where Kubernetes and DevOps fit together. Kubernetes helps teams respond 
to customer demands without having to worry about the infrastructure layer – Kubernetes 
does this for them. The orchestration engine within Kubernetes takes over the once-manual 
tasks of deploying, scaling and building more resiliency into the applications; instead, 
it has the controls to manage this on the fly.

Kubernetes is essential for DevOps teams looking to automate, scale and build resiliency 
into their applications while minimizing the infrastructure burden. Letting Kubernetes manage 
an application’s scale and resiliency based on metrics, for example, allows developers to focus 
on new services instead of worrying whether the application can handle the additional requests 
during peak times. The following are key reasons why Kubernetes is essential to a DevOps team:

**Deploy Everywhere**. As noted previously, Kubernetes handles the ability to deploy an 
application anywhere without having to worry about the underlying infrastructure. This 
abstraction layer is one of the biggest advantages to running containers. Wherever deployed, 
the container will run the same within Kubernetes.

**Infrastructure and Configuration as Code**. Everything within Kubernetes is “as-code,” 
ensuring that both the infrastructure layer and the application are all declarative, portable 
and stored in a source repository. By running “as-code,” the environment is automatically 
maintained and controlled.

**Hybrid**. Kubernetes can run anywhere – whether on-premises, in the cloud, on the edge. It’s 
your choice. So, you’re not locked in to either an on-premises deployment or a cloud-managed 
deployment. You can have it all.

**Open Standards**. Kubernetes follows open-source standards, which increases your flexibility 
to leverage an ever-growing ecosystem of innovative services, tools and products.

**Deployments with No Downtime**. Since applications and services get continuously deployed 
during the day, Kubernetes leverages different deployment strategies. This reduces the impact 
on existing users while giving developers the ability to test in production (phased approach 
or blue-green deployments). Kubernetes also has a rollback capability – should that be necessary.

**Immutability**. This is one of the key characteristics of Kubernetes. The oft-used analogy, 
“cattle, not pets,” means that containers can (and should) be able to be stopped, redeployed and 
restarted on the fly with minimal impact (naturally, there will be an impact on the service the 
container is operating).

[Full article](https://rancher.com/blog/2020/create-kubernetes-devops-pipeline/)
