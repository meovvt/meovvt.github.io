---
title: 'jpg-ből gif a parancssorban'
description: 'jpg-ből gif a parancssorban'
tags: [jpg, gif, cli]
date: '2023-09-20'
---

## jpg-ből gif a parancssorban

Tegyük fel hogy van egy rakás szépen sorba rendezett `jpg` fájlunk és animálni szeretnénk.

ImageMagick to the rescue:

    $ convert -delay 20 -loop 0 *.jpg new.gif

*Infóforrás*: [AskUbuntu](https://askubuntu.com/questions/648244/how-do-i-create-an-animated-gif-from-still-images-preferably-with-the-command-l)

