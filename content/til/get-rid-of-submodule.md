---
title: Mégsem akarom azt a git submodule-t
description: Mégsem akarom azt a git submodule-t
tags: [git, CLI]
date: '2023-09-19'
---

## Mégsem akarom azt a git submodule-t

Az egyik lehetőség arra hogy új témát kapjon a hugo blog, hogy `git submodule`ként adjuk hozzá. Nade akkor később, amikor belenyúlunk már nem az igazi így.

Szóval, szabaduljunk meg tőle:

    $ git rm themes/THEMENAME
    $ git rm .gitmodules # ezt csak akkor ha csak ez az egy submodule volt

És már csak a `.git/config`ból kell kitörölni a `module`ra vonatkozó részt.

*Infóforrás*: [StackOverflow](https://stackoverflow.com/questions/1260748/how-do-i-remove-a-submodule)
