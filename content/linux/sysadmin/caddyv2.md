---
title: "Candy V2 Config"
date: 2021-04-06T14:16:30+08:00
draft: false
tags: ["linux","sysadmin"]
---
Caddy Server V2 config
===

```bash
https://a.canbe.top {
  root * /var/www/html
  encode gzip
  reverse_proxy 127.0.0.1:9008
  tls  /etc/letsencrypt/live/canbe.top/fullchain.pem /etc/letsencrypt/live/canbe.top/privkey.pem
}

https://mpcroom.canbe.top {
  root * /home/ubuntu/static
  encode gzip
  file_server
  tls  /etc/letsencrypt/live/canbe.top/fullchain.pem /etc/letsencrypt/live/canbe.top/privkey.pem
}
```