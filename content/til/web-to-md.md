---
title: Weblap markdownra konvertálása
linkTitle: Weblap markdownra konvertálása
weight: 1
description: Weblap markdownra konvertálása
tags: [web, CLI, conversion, TODO, pandoc]
date: '2023-09-15'
---

## Tegyük fel, hogy egy weblapot lementenénk markdownként

Nyilván sok megoldás van rá, és lehet akár böngésző kiegészítő is, vagy pl. `lynx -dump`-pal is, de a `pandoc` erre is jó(bb, mert többféle output formátumot kezel): `pandoc -f html -t markdown https://URL > output.md`

Persze az output még takarítandó, de akkor is :-).

#TODO: szkriptesíteni, hogy rögtön ilyen poszt legyen belőle.

Infóforrás: [az igazán nagyszerű kézikönyv](https://pandoc.org/MANUAL.html).
