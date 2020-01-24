---
layout: post
title: Infrastructure as Code with Terraform
tags: infrastructure code terraform
date: 2020-01-24
---

![Terraform logo](https://www.datocms-assets.com/2885/1506458612-blog-terraform.svg)

What is Infrastructure as Code, IaC? It is infrastructure (CPUs, memory, disk, 
firewalls, etc.) defined as code within definition files.

So how does IaC fit into the infrastructure lifecycle? IaC can be applied throughout 
the lifecycle, both on the initial build, as well as throughout the life of the infrastructure. 

IaC makes changes idempotent, consistent, repeatable, and predictable. 

Since code is checked into version control systems such as GitHub, GitLab, BitBucket, 
etc., it is possible to review how the infrastructure evolves over time. The idempotent 
characteristic provided by IaC tools ensures that, even if the same code is applied 
multiple times, the result remains the same.

Successfully managing the lifecycle of infrastructure is hard, and the impact of poor 
management decisions can be significant, ranging from financial and reputational losses 
to even loss of life when considering government and military dependencies on infrastructure. 
Adopting the use of an IaC tool such as HashiCorp Terraform, in conjunction with related and 
established tools, processes, and workflows, is a necessary step in mitigating these risks.

[Full article](https://www.hashicorp.com/blog/infrastructure-as-code-in-a-private-or-public-cloud/)
