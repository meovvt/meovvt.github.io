---
title: Repository-nként különböző ssh kulcs
linkTitle: Repository-nként különböző ssh kulcs
weight: 1
description: TIL Repository-nként különböző ssh kulcs
tags: [git, CLI, ssh]
date: '2023-09-18'
---

# Repository-nként különböző ssh kulcs

Előfordulhat, hogy szeretnénk valamit nem a "fő" git(hub) accountunk alatt
fejleszteni - mint például ezt az oldalt sem szeretném.

Ehhez először is generáljunk egy új `ssh` kulcsot:

    $ ssh-keygen -t rsa -C "your_OTHER@youremail.com"

(Természetesen nem kötelező `rsa`t használni.)

A `$HOME/.ssh/` alatt jön létre az új kulcs:

    $ ls ~/.ssh/id*
    id_rsa
    id_rsa.pub
    id_rsa_OTHER
    id_rsa_OTHER.pub
    ...

Ezt követően adjuk hozzá az új kulcsot a megfelelő `host`tal az
`~/.ssh/config`-hoz, pl. itt a github-bal így néz ki:

    $ cat ~/.ssh/config
    ...
    #normal account
    Host github.com-normal
      HostName github.com
      User git
      IdentityFile ~/.ssh/id_rsa
  
    #OTHER account
    Host github.com-OTHER
      HostName github.com
      User git
      IdentityFile ~/.ssh/id_rsa_OTHER
    ...

És innéttől célszerűen a klónozást így hajtsuk végre (ha már hozzáadtuk a fenti
eset szerint a githubhoz a publikus kulcsunk, ha a másik account-tal
szeretnénk):

    $ git clone git@github.com-OTHER:username/repo

Ami még hasznos lehet, ha a meglevő repo könyvtárban a `.git/config`ban is beállítjuk:

    ...
    [core]
     ...
    sshCommand = ssh -i ~/.ssh/id_rsa_OTHER
    ...

Infóforrás:

* [SuperUser](https://superuser.com/questions/232373/how-to-tell-git-which-private-key-to-use)
* [ez a gist](https://gist.github.com/jexchan/2351996)
