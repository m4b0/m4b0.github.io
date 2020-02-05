---
layout: post
title: OpenCensus to monitor your Kubernetes cluster
tags: devops opencensus monitor kubernetes k8s cluster
date: 2020-02-05
---

![Kubernets monitor image](https://opensource.com/sites/default/files/styles/image-full-size/public/lead-images/ship_captain_devops_kubernetes_steer.png?itok=LAHfIpek)

While Prometheus has become the de facto standard for monitoring Kubernetes 
for many users, there may be reasons why you might choose another approach for 
metric telemetry.

One reason is that using Prometheus introduces another component in your cluster 
that needs to be maintained and updated and will require additional management 
to ensure data persistence over the long term. Another reason is that Prometheus 
collects an incredibly large set of metrics right out of the box, and this could 
become cost-prohibitive in situations where metric volume is an input into your 
overall observability costs.

[OpenCensus](https://opencensus.io/) is a set of open source libraries for observability 
instrumentation. OpenCensus is the currently recommended library to use for instrumenting services 
to collect traces and metrics. The OpenTracing and OpenCensus projects have been merged into 
[OpenTelemetry](https://opentelemetry.io/), which will become the recommended library.

Unlike [Prometheus](https://prometheus.io/docs/concepts/metric_types/), where you have 
to define the metric kind upfront, OpenCensus simply requires you to collect the measurements 
and then aggregate them in the view before sending them to the exporter. The measurements 
support integer and float values. From there, you can use create histograms using the 
distribution aggregation, add up the number of samples using the count aggregation, or 
add up the collected values using the sum aggregation.

[Full article](https://opensource.com/article/20/2/kubernetes-opencensus)
