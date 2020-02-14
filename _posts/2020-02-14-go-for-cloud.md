---
layout: post
title: "Go for Cloud"
tags: programming developer go golang cloud
date: 2020-02-14
---

![Golang for cloud image](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTqXFYYbLrf9ZQ03wALIuXYyJELZEZKu-8JfuqglHj65E2hfDnE)

Go has been continuously growing in the past decade, especially among the infrastructure 
teams and in the cloud ecosystem. In this article, we will go through some of the unique 
strengths of Go in this field.

- Build small binaries.
- Runtime initialization is fast.
- Build static binaries.
- Cross compile to 64-bit Linux.
- Don't ship your toolchain.
- Rebuild and redeploy with Go releases.
- Embed commit versions into binaries.
- FaaS is Go binary as a service.
- Gracefully reject incoming requests. When auto scaling down or shutting down new resources, start rejecting incoming requests to the Go program. http.Server provides Shutdown for this purpose.
- Report the essential metrics.
- Print scheduling and GC events.
- Propagate the incoming context.
- Continuously profile in production.
- Dump debuggable postmortems. 

[Full article](https://rakyll.org/go-cloud/)
