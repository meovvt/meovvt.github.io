---
title: git add * visszavonása
linkTitle: git add * visszavonása
weight: 1
description: TIL hogyan vonjak vissz egy `git add *`-t.
tags: [git, CLI, undo]
date: '2023-09-15'
---

# `git add *` visszavonása

Az imént egy `npm install -D` után de még a `.gitignore` setup előtt kiadtam
egy `git add *`-t, kár volt.

Szerencsére az undo nem bonyolult: `git reset HEAD -- .`

Infóforrás: [StackOverflow](https://stackoverflow.com/questions/19730565/how-to-remove-files-from-git-staging-area).
