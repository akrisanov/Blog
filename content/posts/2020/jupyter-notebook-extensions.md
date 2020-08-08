---
title: "Расширения для Jupyter Notebook"
tags: ["Jupyter Notebook", "Python"]
date: 2020-03-30T00:30:27+03:00
draft: false
---

Jupyter Notebook – один из часто используемых мною инструментов. Несмотря на всю мощь этого решения,
"из коробки" иногда не хватает какой-нибудь маленькой, но полезной функциональности, например,
генерации содержания по заголовкам разметки Markdown.

К счастью исправить подобные мелочи отчасти помогают расширения, которые можно найти на Github.
Существуют как официальные пакеты, поддерживаемые JupyterLab, так и созданные сообществом решения.

Хорошим примером коллективной работы является [jupyter_contrib_nbextensions](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/index.html)
– большая коллекция _неофициальных_ полезных дополнений к Jupyter.
Полный список расширений доступен на [странице документации](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions.html).

Для их подключения к вашему Jupyter Notebook потребуется выполнить три простых шага.

1. Установить pip пакет с расширениями:

```shell
$ pip3 install jupyter_contrib_nbextensions
```

2. Скопировать JavaScript и CSS файлы:

```shell
$ jupyter contrib nbextension install --user
```

3. Активировать выбранное расширение:

```shell
$ jupyter nbextension enable toc2/main
```

В ответ вы должны получить следующее сообщение:

```shell
Enabling notebook extension toc2/main...
      - Validating: OK
```

Запустив заново Jupyter Notebook, можно убедиться, что расширение было успешно установлено и активировано:

![Table of Contents](/images/toc2.png)
