---
title: Lazyvim új plugin
description: Lazyvim új plugin
tags: [til, neovim, nvim, plugin]
date: '2023-09-20'
---

## Lazyvim új plugin

Ha már úgyis `nvim`mel írom ezeket, nem ártana némi `git` integráció, amiből valamennyit a [Lazyvim](https://www.lazyvim.org/) biztosít, de itt a szép új fancy [Neogit](https://github.com/NeogitOrg/neogit), hogyan adjuk hozzá?

Nem egy bonyolult dolog: hozzuk létre (Windowson): a `~/AppData/Local/nvim/lua/plugins/neogit.lua` fájlt ezzel a tartalommal:

    {
      "NeogitOrg/neogit",
      dependencies = {
        "nvim-lua/plenary.nvim",         -- required
        "nvim-telescope/telescope.nvim", -- optional
        "sindrets/diffview.nvim",        -- optional
        "ibhagwan/fzf-lua",              -- optional
      },
      config = true
    }

És indítsuk újra a `neovim`-t, hogy települjön is.

*Infóforrások*: 

* [RTFM](https://www.lazyvim.org/configuration/plugins)
* És a [Neogit projekt oldal](https://github.com/NeogitOrg/neogit) 

