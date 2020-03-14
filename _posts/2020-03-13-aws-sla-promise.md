---
layout: post
title: "AWS SLA: keep your availability promise?"
tags: aws sla availability promise
date: 2020-03-13
---

![Calculator image](https://cloudonaut.io/images/2019/01/calculate.jpg)

Are you offering availability of 99.99% or more to your clients? Bad news, you might not be able to keep your promise!

Recently AWS announced a bunch of new Service Level Agreements (SLA). Therefore, it is now possible to calculate 
the expected availability of most of the architectures on AWS.

![Calculation image](https://cloudonaut.io/images/2019/01/aws-sla-ec2.png)

Are you looking for a way to increase the expected availability of your architecture? Deploy your workload to 
multiple regions. But be warned, doing so comes with additional complexity caused by the need to synchronize 
your data between multiple regions.

Notes:
- Calculating for multiple regions, the result will be around 99.98% for expected availability.

References:
- [How do you calculate the compound Service Level Agreement (SLA) for cloud services?](https://devops.stackexchange.com/questions/711/how-do-you-calculate-the-compound-service-level-agreement-sla-for-cloud-servic)

[Full article](https://cloudonaut.io/aws-sla-are-you-able-to-keep-your-availability-promise/)
