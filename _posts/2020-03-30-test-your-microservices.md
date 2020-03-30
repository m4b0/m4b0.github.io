---
layout: post
title: "Test Your Microservices"
tags: test microservices development developer
date: 2020-03-30
---

![Code image](https://www.freecodecamp.org/news/content/images/size/w2000/2020/03/UiqRDTTd.png)

Microservices architecture describes the practice of breaking up an application into a series of 
smaller and more problem-solution oriented components. Then each of these components communicates 
with one another across common protocols like HTTP or the more lightweight TCP.

Software testing is important for a number of reasons, but most importantly:

- It saves money and a lot of time
- Security
- Product quality (fewer bugs and errors)
- Customer satisfaction
- It lets you sleep peacefully at night

As long as you develop an application that will be used by users and has some complexity, tests should 
not be an option – they should be mandatory.

There are various types of software testing.

Functional Testing types include:

- Unit Testing
- Integration Testing
- Smoke Testing
- Regression Testing
- Sanity Testing
- Beta/Acceptance Testing
- End to End (e2e) Testing

Non-functional Testing types include:

- Performance Testing
- Load Testing
- Stress Testing
- Security Testing
- Compliance Testing
- Usability Testing

The more complex the app gets the more types of tests you will use.

The basic tests that you should always use are the following:

- Unit Testing
- Integration Testing
- E2E Testing combined with Regression testing and Security Testing

The process goes like this: first you write tests to check if your app behaves as expected in almost 
all aspects, including corner cases. Second, if your app is already live, you write tests to check 
if any new changes to the code break the current functionality.

Side note: besides these basic tests that you should use at any type of software, there are additional 
tests you should write for microservices. Don't forget load tests, for example, to check your system's 
behavior under both normal and anticipated peak load conditions.

[Full article](https://www.freecodecamp.org/news/testing-microservices-are-they-production-ready-2/)
