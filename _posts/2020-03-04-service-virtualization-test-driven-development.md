---
layout: post
title: "How service virtualization relates to test-driven development"
tags: opensource service test driven develpment
date: 2020-03-04
---

![Developer image](https://opensource.com/sites/default/files/styles/image-full-size/public/lead-images/laptop_screen_desk_work_chat_text.png?itok=UXqIDRDD)

Mountebank simulates services you're dependent on so autonomous teams can continue development activities 
without having to wait on anyone.

The agile approach to software development relies on service virtualization to give each IT team autonomy. 
This approach removes blockages and allows autonomous teams to continue development activities without having 
to wait on anyone. That way, integration testing can commence as soon as teams start iterating/sprinting.

There is a great new tool called 
[mountebank](http://www.mbtest.org/) that is ideal for virtualizing any service. Using this tool, you can 
quickly stand up a local server that listens on a port you specify and takes orders. To make it simulate a 
service, you only have to tell it which port to listen to and which protocol to handle. The choice of protocols is:

- HTTP
- HTTPS
- SMTP
- TCP

[Full article](https://opensource.com/article/20/3/service-virtualization-test-driven-development)
