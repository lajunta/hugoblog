---
title: "Generate random number"
date: 2021-04-04T23:56:54+08:00
draft: false
tags: ["linux","commands"]
---
生成随机数
===

xxd
---

```bash
xxd -g 2 -l 64 -p /dev/random | tr -d "\n"
```

