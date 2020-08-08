---
title: "Fatal Lock File Postmaster Pid Already Exists"
tags: ["MacOS", "Homebrew"]
date: 2020-07-27T16:46:07+03:00
draft: false
---

Иногда при обновлении PostgreSQL через Homebrew возникает следующая проблема.
"Починить" ее можно удалив файл, содержащий идентификатор запущенного процесса:

```shell
$ brew services stop postgresql

# adjust the path accordingly to your install
$ rm /usr/local/var/postgres/postmaster.pid

$ brew services start postgresql
```
