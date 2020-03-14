---
layout: post
title: "Writing Safe Shell Scripts"
tags: sysadmin tools bash automation
date: 2020-03-13
---

![Dodo image](https://sipb.mit.edu/images/grumpyfuzzball_half.png)

Writing shell scripts leaves a lot of room to make mistakes, in ways that will cause your scripts to 
break on certain input, or (if some input is untrusted) open up security vulnerabilities. Here are some 
tips on how to make your shell scripts safer.

The simplest step is to avoid using shell at all. Many higher-level languages are both easier to write 
the code in in the first place, and avoid some of the issues that shell has. For example, Python will 
automatically error out if you try to read from an uninitialized variable (though not if you try to 
write to one), or if some function call you make produces an error.

- Shell settings
```
set -euf -o pipefail
```
- Quote liberally
- Passing filenames or other positional arguments to commands
- Temporary files
- Use [ShellCheck](https://www.shellcheck.net/) to check for bugs
- Google has a Shell [Style Guide](https://google.github.io/styleguide/shell.xml).

**Conclusion**
When possible, instead of writing a "safe" shell script, use a higher-level language like Python. If you 
can't do that, the shell has several options that you can enable that will reduce your chances of having 
bugs, and you should be sure to quote liberally.

[Full article](https://sipb.mit.edu/doc/safe-shell/)
