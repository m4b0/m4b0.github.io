---
layout: post
title: "Apache X-Forwarded-For"
tags: apache logs config forwarded
date: 2020-03-04
---

![Apache support image](https://www.apache.org/img/support-apache.jpg)

When configuring Apache X-Forwarded-For take in consideration the differences for Apache versions 2.2 and 2.4.

Example to allow specific IP addresses (Apache 2.4):
```
SetEnvIF X-Forwarded-For "1.1.1.1" AllowIP
SetEnvIF X-Forwarded-For ^10\. AllowIP

<RequireAny>
    Require env AllowIP
</RequireAny>
```

References:
- [Apache Module mod_remoteip](https://httpd.apache.org/docs/2.4/mod/mod_remoteip.html)
- [Apache logs](https://httpd.apache.org/docs/2.4/logs.html)
- [Apache Module mod_log_config](http://httpd.apache.org/docs/current/mod/mod_log_config.html)
- [How do I capture client IP addresses in my ELB access logs?](https://aws.amazon.com/premiumsupport/knowledge-center/elb-capture-client-ip-addresses/)
- [HOWTO: Log Client IP AND X-Forwarded-For IP in Apache](https://www.techstacks.com/howto/log-client-ip-and-xforwardedfor-ip-in-apache.html)

[Full article](https://dryja.info/apache2-block-allow-ip-simple-guide/)
