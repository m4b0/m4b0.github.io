---
layout: post
title: The best Docker base image for Python
tags: docker image python tips ubuntu centos debian
date: 2020-01-29
---

![Docker Python image](https://blog.theodo.com/static/8811a510f52bb94aaa4f936b79e105f2/939d7/docker-virtualenv.png)

When you’re building a Docker image for your Python application, you’re building 
on top of an existing image—and there are many possible choices. There are OS 
images like Ubuntu and CentOS, and there are the many different variants of 
the python base image.

Which one should you use? Which one is better? There are many choices, and it 
may not be obvious which is the best for your situation.

Related article [Why you shouldn’t use Alpine Linux](https://pythonspeed.com/articles/alpine-docker-python/)
explains why Alpine makes Python Docker builds 50× slower, and images 2× larger.

So what should you use?

As of January 2020, Debian 10 (“Buster”) is a good operating system base:

1. It’s more up-to-date than ubuntu:18.04.
2. It’s stable, and won’t have significant library changes.
3. There’s less chances of weird production bugs than Alpine.

And the official Python Docker images based off of Debian Buster also give you 
the full range of Python releases.

The official Docker Python image in its slim variant—e.g. python:3.8-slim-buster—is 
a good base image for most use cases. it’s 60MB when downloaded, 180MB when 
uncompressed to disk, it gives you the latest Python releases, and it’s got all 
the benefits of Debian Buster.

[Full article](https://pythonspeed.com/articles/base-image-python-docker-images/)
