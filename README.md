# ghostmatter.nvim

## An Outer Wilds themed colorscheme, featuring all your favorite colors from the neon blues and greens of Ghostmatter to the dark blues of the Eye, all the way to the reds and yellows of your favorite campfire (this might be a stretch, but hey I needed something to go off for a new theme).

#### Note: Originally a fork of [Moonlight.nvim](https://github.com/shaunsingh/moonlight.nvim). Some of the colors will likely remain similar, but the fork is mostly for the code structure at the moment.

## 🌠 Features

ghostmatter.nvim is meant to be a modern colorscheme written in lua for NeoVim that supports a lot of the new features
added to NeoVim like built-in LSP and [TreeSitter](https://github.com/nvim-treesitter/nvim-treesitter)

+ Supported plugins:
    + [TreeSitter](https://github.com/nvim-treesitter/nvim-treesitter)
    + [LSP Diagnostics](https://neovim.io/doc/user/lsp.html)
    + [Lsp Saga](https://github.com/glepnir/lspsaga.nvim)
    + [LSP Trouble](https://github.com/folke/lsp-trouble.nvim)
    + [Git Gutter](https://github.com/airblade/vim-gitgutter)
    + [git-messenger](https://github.com/rhysd/git-messenger.vim)
    + [Git Signs](https://github.com/lewis6991/gitsigns.nvim)
    + [Telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
    + [Nvim-Tree.lua](https://github.com/kyazdani42/nvim-tree.lua)
    + [NERDTree](https://github.com/preservim/nerdtree)
    + [vim-which-key](https://github.com/liuchengxu/vim-which-key)
    + [Indent-Blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim)
    + [Dashboard](https://github.com/glepnir/dashboard-nvim)
    + [BufferLine](https://github.com/akinsho/nvim-bufferline.lua)
    + [Lualine](https://github.com/hoob3rt/lualine.nvim)
    + [Neogit](https://github.com/TimUntersberger/neogit)
    + [vim-sneak](https://github.com/justinmk/vim-sneak)

+ Ability to change background on sidebar-like windows like Nvim-Tree, Packer, terminal etc.

+ Added functions for live theme switching without the need to restart NeoVim

## ⚡️ Requirements

+ Neovim >= 0.5.0

## 🌙 Installation

Install via your favourite package manager:
```vim
" If you are using Vim-Plug
Plug 'JBlocklove/ghostmatter.nvim'
```

```lua
-- If you are using Packer
use 'JBlocklove/ghostmatter.nvim'
```

## 🌓 Usage

Enable the colorscheme:
```vim
"Vim-Script:
colorscheme ghostmatter
```

```lua
--Lua:
require('ghostmatter').set()
```

To enable the `ghostmatter` theme for `Lualine`, simply specify it in your lualine settings:

```lua
require('lualine').setup {
  options = {
    -- ... your lualine config
    theme = 'ghostmatter'
    -- ... your lualine config
  }
}
```

## ⚙️ Configuration (CURRENTLY UNIMPLEMENTED WITH THE NEW NAME. USE MOONLIGHT FOR NOW. DEVELOPMENT OF THE NEW COLORS AND CONFIGS WILL BE ON THE GM BRANCH)


| Option                              | Default     | Description                                                                                                                                                     |
| ----------------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ghostmatter_italic_comments            | `false`     | Make comments italic                                                                                                                                            |
| ghostmatter_italic_keywords            | `false`     | Make keywords italic                                                                                                                                            |
| ghostmatter_italic_functions           | `false`     | Make functions italic                                                                                                                                           |
| ghostmatter_italic_variables           | `false`     | Make variables and identifiers italic                                                                                                                           |
| ghostmatter_contrast                   | `true`      | Make sidebars and popup menus like nvim-tree and telescope have a different background                                                                                       |
| ghostmatter_borders                    | `false`     | Enable the border between verticaly split windows visable
| ghostmatter_disable_background         | `false`     | Disable the setting of background color so that NeoVim can use your terminal background (Not all plugins supported)

```lua
-- Example config in lua
vim.g.ghostmatter_italic_comments = true
vim.g.ghostmatter_italic_keywords = true
vim.g.ghostmatter_italic_functions = true
vim.g.ghostmatter_italic_variables = false
vim.g.ghostmatter_contrast = true
vim.g.ghostmatter_borders = false
vim.g.ghostmatter_disable_background = false

-- Load the colorscheme
require('ghostmatter').set()
```

```vim
" Example config in Vim-Script
let g:ghostmatter_italic_comments = true
let g:ghostmatter_italic_keywords = true
let g:ghostmatter_italic_functions = true
let g:ghostmatter_italic_variables = false
let g:ghostmatter_contrast = true
let g:ghostmatter_borders = false
let g:ghostmatter_disable_background = false

-- Load the colorsheme
colorscheme ghostmatter
```

Original Readme: https://github.com/marko-cerovac/material.nvim/blob/pure-lua/README.md

