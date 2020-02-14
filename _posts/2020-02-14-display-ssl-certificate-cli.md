---
layout: post
title: "Display a remote SSL certificate details using CLI tools"
tags: ssl certificat command line tools
date: 2020-02-14
---

![SSL certificate image](https://i.stack.imgur.com/cNg6A.png)

Get the full certificate information form a command line tool.

```bash
echo | openssl s_client -showcerts -servername gnupg.org -connect gnupg.org:443 2>/dev/null | openssl x509 -inform pem -noout -text
```

[Full article](https://serverfault.com/questions/661978/displaying-a-remote-ssl-certificate-details-using-cli-tools)
