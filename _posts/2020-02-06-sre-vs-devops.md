---
layout: post
title: SRE vs. DevOps
tags: sre devops
date: 2020-02-06
---

![SRE v DevOps image](https://pbs.twimg.com/media/CTFGZxwUkAAO7gs.jpg:large)

SRE vs. DevOps: competing standards or close friends?

Site Reliability Engineering (SRE) and DevOps are two trending disciplines with quite a 
bit of overlap. In the past, some have called SRE a competing set of practices to DevOps.

The [DevOps movement](https://itrevolution.com/devops-culture-part-1/) 
began because developers would write code with little understanding of how it would run 
in production. They would throw this code over the proverbial wall to the operations team, 
which would be responsible for keeping the applications up and running. This often resulted 
in tension between the two groups, as each group's priorities were misaligned with the needs 
of the business. DevOps emerged as a culture and a set of practices that aims to reduce the 
gaps between software development and software operation. However, the DevOps movement 
[does not explicitly define *how* to succeed](https://www.sethvargo.com/the-ten-myths-of-devops/) 
in these areas. In this way, DevOps is like an abstract class or interface in programming. 
It defines the overall behavior of the system, but the implementation details are left up to the author.

SRE, which evolved at Google to meet internal needs in the early 2000s independently of 
the DevOps movement, happens to embody the philosophies of DevOps, but has a much more 
prescriptive way of measuring and achieving reliability through engineering and operations 
work. In other words, SRE prescribes how to succeed in the various DevOps areas. For example, 
the table below illustrates the five DevOps pillars and the corresponding SRE practices:

DevOps | SRE
-------|----
Reduce organization silos	| Share ownership with developers by using the same tools and techniques across the stack
Accept failure as normal	| Have a formula for balancing accidents and failures against new releases
Implement gradual change	| Encourage moving quickly by reducing costs of failure
Leverage tooling & automation	| Encourages "automating this year's job away" and minimizing manual systems work to focus on efforts that bring long-term value to the system
Measure everything	| Believes that operations is a software problem, and defines prescriptive ways for measuring availability, uptime, outages, toil, etc.

If you think of DevOps like an interface in a programming language, **class SRE implements DevOps**. 
While the SRE program did not explicitly set out to satisfy the DevOps interface, both disciplines 
independently arrived at a similar set of conclusions. But just like in programming, classes often 
include more behavior than just what their interface defines, or they might implement multiple 
interfaces. SRE includes additional practices and recommendations that are not necessarily part of 
the DevOps interface.

DevOps and SRE are not two competing methods for software development and operations, but rather 
close friends designed to break down organizational barriers to deliver better software faster. If 
you prefer books, check out 
[How SRE relates to DevOps](https://www.safaribooksonline.com/library/view/how-sre-relates/9781492030645/) 
(Betsy Beyer, Niall Richard Murphy, Liz Fong-Jones) for a more thorough explanation.

[Full article](https://cloud.google.com/blog/products/gcp/sre-vs-devops-competing-standards-or-close-friends)
