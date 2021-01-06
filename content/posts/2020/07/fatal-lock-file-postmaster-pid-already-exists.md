---
title: "Fatal Lock File Postmaster Pid Already Exists"
tags: ["MacOS", "Homebrew"]
date: 2020-07-27T16:46:07+03:00
draft: false
---

Иногда при обновлении PostgreSQL через Homebrew возникает следующая проблема.
"Починить" ее можно удалив файл, содержащий идентификатор запущенного процесса и заново запустив
сервис БД:

```shell
$ brew services stop postgresql

$ rm /usr/local/var/postgres/postmaster.pid

$ brew services start postgresql
```
<!--more-->
