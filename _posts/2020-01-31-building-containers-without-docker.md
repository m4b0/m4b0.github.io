---
layout: post
title: Building containers without Docker
tags: openfaas opensource containers buildkit docker kaniko oci kubernetes
date: 2020-01-31
---

![OpenFaaS logo image](https://avatars2.githubusercontent.com/u/27013154?s=400&v=4)

There are several ways to build containers without the need for Docker itself. 
[OpenFaaS](https://github.com/openfaas/) as the case-study, which uses OCI-format 
container images for its workloads. The easiest way to think about OpenFaaS is as 
a CaaS platform for [Kubernetes](https://kubernetes.io/) which can run microservices, 
and add in FaaS and event-driven tooling for free.

See also [OpenFaaS.com](https://openfaas.com/)

[Full article](https://blog.alexellis.io/building-containers-without-docker/)
