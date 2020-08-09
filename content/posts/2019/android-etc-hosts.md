---
title: "Обновление файла /etc/hosts на эмуляторе Android"
tags: ["Android", "Отладка"]
date: 2019-06-27T16:41:50+03:00
draft: false
---

Следующие действия помогают облегчить процесс отладки приложения если у вас нет устройства под рукой:

```shell
$ android-sdk-macosx/tools/emulator -avd <avdname> -writable-system
$ ./adb root
$ ./adb remount

# copy hosts file from local machine to Android device
$ ./adb push <local>/hosts /etc/hosts

$ ./adb shell
$ cat /etc/hosts
$ ping customsite.com
```
