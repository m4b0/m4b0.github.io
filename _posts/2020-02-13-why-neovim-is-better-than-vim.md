---
layout: post
title: "Why Neovim is Better than Vim"
tags: programming developer sysadmin vim neovim
date: 2020-02-13
---

![Neovim logo image](https://raw.githubusercontent.com/neovim/neovim.github.io/master/logos/neovim-logo-300x87.png)

Neovim is exactly what it claims to be. It fixes every issue I have with Vim: The plugin API. 
The codebase. The community. The BDFL.

Neovim’s plugin API is backwards-compatible with Vim, but it also allows asynchronous execution. 
Users have already made plugins that Vim can never have. For example, Neomake allows async linters. 
That feature alone is worth making the switch for.

Neovim’s codebase is a substantial improvement. They’ve replaced much of the hacky, platform-specific 
code with libuv. They’ve fixed the problems with indentation, style, and bad file encodings. They’ve 
removed old code for ancient, unused platforms. They’ve drastically increased test quality and 
coverage. There’s still much to be done, but the difference is already worlds better.

If you are a Vim user, I strongly recommend switching to Neovim. It’s the Vim you’re used to, but 
with plugins you never knew you wanted.

References:

- [Installing Neovim](https://github.com/neovim/neovim/wiki/Installing-Neovim)

[Full article](https://geoff.greer.fm/2015/01/15/why-neovim-is-better-than-vim/)
