---
title: WSL parancssorból Windows vágólapra
description: WSL parancssorból Windows vágólapra
tags: [WSL, CLI, shell, clipboard, copy]
date: '2023-09-24'
---

## WSL parancssorból Windows vágólapra

OK, a WSL egy áldás, és persze bármennyi PowerShell tutorialt olvastam eddig, csak visszanyulok a ~~gyökerekhez~~ a már megszokott dolgokhoz, pláne, hogy az megy fejből, nem kell keresni a megfejtést egy több GBs szövegfájl feldolgozásához.

Nade mi van, ha az eredmény bőven elég, ha a Windows vágólapra kerül?

    csvcut -c OSZLOPn | \
      tail -n +2 | \
      awk '/MAGIC/ { code = "nyilván, de mindent csak nem írok ide, mert ez nem awk-ról szól" }' | \
      #... several commands later  | \
      clip.exe

*Infóforrás*: [StackOverflow](https://stackoverflow.com/questions/59984528/copy-the-contents-of-a-file-to-clipboard-from-wsl-to-windows)
