---
layout: post
title: "Overthinking it and the value of simple solutions"
tags: overhthinking value simple solutions
date: 2020-02-24
---

![PostfreSQL useful image](https://images.squarespace-cdn.com/content/v1/5c6961eb7fdcb81f0e8b26b3/1573320804150-5SDJI3TBRT83W96SDION/ke17ZwdGBToddI8pDm48kH6iJLJzmydqq3Cvt1o0OI1Zw-zPPgdn4jUwVcJE1ZvWQUxwkmyExglNqGp0IvTJZamWLI2zvYWH8K3-s_4yszcp2ryTI0HqTOaaUohrI8PI2mZ3g3sJ28Z7C1NSajdf0It1pO9q06Igdf_vumPWGcQKMshLAGzx4R3EDFOm1kBS/IMG_2213.jpeg?format=750w)

*"Use the simplest tools possible and not get overwhelmed by the technology" ~ J-Zone*

This is where 
[Lockjaw](https://github.com/nomnom-insights/nomnom.lockjaw) comes in - it’s a small library which exposes 
[Postgres’ advisory locks](https://hashrocket.com/blog/posts/advisory-locks-in-postgres) as a pluggable 
[Component](https://github.com/stuartsierra/component).

With a simple solution to the locking problem, plugging it into the rest of the system was pretty straightforward. In 
fact, our existing scheduler component - 
[Eternity](https://github.com/nomnom-insights/nomnom.eternity) did not require any changes.

Both Eternity and Lockjaw are open sourced, and you can check them out (and use :-)) on our 
[GitHub page](https://github.com/nomnom-insights?language=clojure&q=&type=public&utf8=%E2%9C%93).

[Full article](https://korecki.me/blog/2019/10/8/overthinking-it-and-the-value-of-simple-solutions)
