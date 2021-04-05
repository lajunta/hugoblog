---
title: "Sed Usage"
date: 2021-04-04T23:56:54+08:00
draft: false
tags: ["linux","commands"]
---

```bash
find . -type f -exec sed -i '1s;^;---\ntitle: "Test blog"\n---\n;' {} \;
```

### 查找并删除所在的行

```bash
find . -type f -exec sed -i '/^title:/d' {} \;
```

### 删除前面N,M行

```bash
find . -type f -exec sed -i '1,1d' {} \;
```