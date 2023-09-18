
---
title: Keressük meg a leghosszabb sort egy szöveges fájlban Linuxon
linkTitle: Keressük meg a leghosszabb sort egy szöveges fájlban Linuxon
weight: 1
description: TIL Keressük meg a leghosszabb sort egy szöveges fájlban Linuxon
tags: [CLI, linux, sort, line, search, awk]
date: '2023-09-18'
---

## Keressük meg a leghosszabb sort egy szöveges fájlban Linuxon

    awk '{ print length, $0 }' FILE | sort -n | cut -d" " -f2-

Infóforrás:

* [AskUbuntu](https://askubuntu.com/questions/165501/how-do-i-sort-a-wordlist-by-string-length)
