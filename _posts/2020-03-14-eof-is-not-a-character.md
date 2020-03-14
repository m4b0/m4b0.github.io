---
layout: post
title: "EOF is not a character"
tags: linux eof programming
date: 2020-03-14
---

![EOF image](https://ruslanspivak.com/eofnotchar/eofnotchar_notachar.png)

Let’s recap the main points about EOF with added details for more clarity:

- EOF in ANSI C is not a character. It’s a constant defined in <stdio.h> and its value is usually -1
- EOF is not a character in the ASCII or Unicode character set
- EOF is not a character that you find at the end of a file on Unix/Linux systems
- There is no explicit “EOF character” at the end of a file on Unix/Linux systems
- EOF(end-of-file) is a condition provided by the kernel that can be detected by an 
application ~~when a read operation reaches the end of a file~~ (if k is the current file position and m is the size of a file, performing a read() when k >= m triggers the condition)

[Full article](https://ruslanspivak.com/eofnotchar/)
