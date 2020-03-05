---
layout: post
title: "Let’s use Kubernetes! - Now you have 8 problems"
tags: kubernetes k8s issues problems
date: 2020-03-05
---

![Kubernetes image](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQA4MrqwAQ0sRnVz75oXFe5mDq3vpYgb4ZN2UISQcdu9CvZLCDg)

If you’re using Docker, the next natural step seems to be Kubernetes, aka K8s: that’s how you run things 
in production, right?

Well, maybe. Solutions designed for 500 software engineers working on the same application are quite 
different than solutions for 50 software engineers. And both will be different from solutions designed 
for a team of 5.

**If you’re part of a small team, Kubernetes probably isn’t for you: it’s a lot of pain with very little 
benefits.**

Let’s see why.

Kubernetes has plenty of moving parts—concepts, subsystems, processes, machines, code—and that means plenty of problems.

The Kubernetes code base as of early March 2020 has more than 580,000 lines of Go code. That’s actual code, 
it doesn’t count comments or blank lines, nor did I count vendored packages. A 
[security review from 2019](https://github.com/kubernetes/community/blob/master/wg-security-audit/findings/Kubernetes%20Final%20Report.pdf) 
described the code base as follows:

> “…the Kubernetes codebase has significant room for improvement. The codebase is large and complex, with 
large sections of code containing minimal documentation and numerous dependencies, including systems external 
to Kubernetes. There are many cases of logic re-implementation within the codebase which could be centralized 
into supporting libraries to reduce complexity, facilitate easier patching, and reduce the burden of 
documentation across disparate areas of the codebase.”

Kubernetes is a complex system with many different services, systems, and pieces.

Here’s what that security review I mentioned above had to say:

> “Kubernetes is a large system with significant operational complexity. The assessment team found 
> configuration and deployment of Kubernetes to be non-trivial, with certain components having confusing 
> default settings, missing operational controls, and implicitly defined security controls.”

The more you buy in to Kubernetes, the harder it is to do normal development: you need all the different 
concepts (Pod, Deployment, Service, etc.) to run your code. So you need to spin up a complete K8s system 
just to test anything, via a VM or nested Docker containers.

More moving parts means more opportunity for error.

There is no such thing as best practices in general; there are only best practices for a particular 
situation. **Just because something is trendy and popular doesn’t mean it’s the right choice for you.**

In some situations Kubernetes is a really great idea. In others it’s a timesink with no benefit.

Unless you really need all that massive complexity, there are wide variety of tools that will do just 
as well: from Docker Compose on a single machine, to Heroku and similar systems, to something like 
Snakemake for computational pipelines.

[Full article](https://pythonspeed.com/articles/dont-need-kubernetes/)
