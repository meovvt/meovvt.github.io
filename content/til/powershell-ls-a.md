---
title: Powershell ls vs. rejtett fájlok
description: Powershell ls vs. rejtett fájlok
tags: [til, powershell, CLI, shell]
date: '2023-09-19'
---

## Powershell ls vs. rejtett fájlok

Jó, jó ez a [PowerShell](https://learn.microsoft.com/en-us/powershell/), akarom
szeretni is, de azért amikor az jön szembe, hogy listázzuk ki a rejtett
fájlokat is, és nyilván múltamból fakadóan kiadom (hiszen van alias), hogy `ls
-a`, de az nyilván nem megy, és némi keresés után kiderül, hogy a helyes
megoldás:

    $ Get-Item -Force *

Nos akkor azért eltünődöm, hogy biztos akarom-e szeretni.

*Infóforrás*: [StackOverflow](https://stackoverflow.com/questions/29688848/list-hidden-sub-directories-and-sizes)
