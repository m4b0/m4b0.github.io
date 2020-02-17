---
layout: post
title: "Three Types of Data"
tags: programming developer data types
date: 2020-02-16
---

![Programming image](https://www.thoughtco.com/thmb/whvt-RBRW6jBsH8s6I9mT7jyirw=/1885x1414/smart/filters:no_upscale()/GettyImages-1132551777-bf613698e593460982c78604fd9b0d3b.jpg)

Three different categories of data in software: 
- Constants, 
- State, and 
- Cached Values. 

By "data" I generally mean "variables in code", but the same principles could be applied to files on a disk, 
or tables in a database, or whatever else.

These three categories are disjoint: that is, if a piece of data falls into one of them, it should not also 
be treated like one of the others. Different languages will vary in their ability to express this constraint 
via the type system or otherwise, so it's better to think of it as a convention or a frame of mind (though 
if you can actually enforce it, that is of course all the better).

A Constant, in this context, is **information that doesn't change during the course of running the program**.

State is **information that naturally changes during the course of running the program**.

Cached values are **information that is derived directly from Constants and/or State**.

To summarize:

- Constants are neither replaceable nor mutable
- State is arbitrarily replaceable and mutable
- Cached Values are replaceable under specific circumstances but not mutable

[Full article](https://www.brandonsmith.ninja/blog/three-types-of-data)
