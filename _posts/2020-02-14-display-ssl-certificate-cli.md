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

Improvement.

```bash
echo | openssl s_client -showcerts -servername gnupg.org -connect gnupg.org:443 2>/dev/null | openssl x509 -inform pem -noout -text | grep "Not After" | sed 's/$/ - gnupg.org/'
```

With result:

```bash
Not After : Apr  3 00:55:19 2020 GMT - gnupg.org
```

Reference for [*servername*](https://stackoverflow.com/questions/43785703/using-servername-param-with-openssl-s-client).

Essentially it works a little like a "Host" header in HTTP, i.e. it causes the requested domain name to be passed as part of the SSL/TLS handshake (in the SNI - Server Name Indication extension). A server can then host multiple domains behind a single IP. It will respond with the appropriate certificate based on the requested domain name.

[Full article](https://serverfault.com/questions/661978/displaying-a-remote-ssl-certificate-details-using-cli-tools)
