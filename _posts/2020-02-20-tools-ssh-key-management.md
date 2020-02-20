---
layout: post
title: "Tools for SSH key management"
tags: opensource tools ssh key management
date: 2020-02-20
---

![Devices image](https://opensource.com/sites/default/files/styles/image-full-size/public/lead-images/osdc_BUS_Apple_520.png?itok=ZJu-hBV1)

Time-saving shortcuts for a commonly used open source tool.

```
$ ssh-keygen
```
This will create a key-pair (a public and private key) in ~/.ssh/. Keep the private 
key (id_rsa) on the PC and never share it. You can share the public key (id_rsa.pub) 
with others or place it on other servers.

```
$ ssh-copy-id pi@192.168.1.20
```

You can use this to give yourself (or others) access to a computer or server by importing their keys from GitHub.

```
$ ssh-import-id gh:bennuttall
```

Give someone else access to a server without asking them for their keys:

```
$ ssh-import-id gh:waveform80
```

Storm helps you add SSH connections to your SSH config, so you don’t have to remember them all. 
You can install it with pip:

```
$ sudo pip3 install stormssh
```

Then you can add an SSH connection to your config with the following command:

```
$ storm add pi3 pi@192.168.1.20
```

You can list, search, and edit saved connections easily using Storm’s 
[documentation](https://stormssh.readthedocs.io/en/stable/usage.html). All Storm actually does 
is manage items in your ssh config file at ~/.ssh/config.

[Full article](https://opensource.com/article/20/2/ssh-tools)
