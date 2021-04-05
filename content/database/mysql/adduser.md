---
title: "Mysql Add User"
date: 2021-04-04T23:56:54+08:00
draft: false
categories: ["mysql"]
---

# Add and Grand user


```bash

CREATE DATABASE database_name;

CREATE USER 'newuser'@'10.8.0.5' IDENTIFIED BY 'user_password';

GRANT ALL PRIVILEGES ON database_name.* TO 'database_user'@'localhost';

```