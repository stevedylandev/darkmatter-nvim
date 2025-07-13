# darkmatter-nvim

![cover](https://files.stevedylan.dev/darkmatter-nvim.png)

A colorscheme adapted from base16-black-metal-bathory

## Features

- Support for Neovim's built-in LSP
- Treesitter highlighting
- Plugin integrations:
  - Telescope
  - Indent Blankline
  - Nvim-notify
  - Rainbow parentheses
  - Nvim-cmp
  - vim-illuminate
  - LSP semantic tokens
  - mini.completion
  - nvim-dap-ui

## Installation

### Using [packer.nvim](https://github.com/wbthomason/packer.nvim)

```lua
use {
  'stevedylandev/darkmatter-nvim',
  config = function()
    vim.cmd('colorscheme darkmatter')
  end
}
```

### Using [lazy.nvim](https://github.com/folke/lazy.nvim)

```lua
{
  'stevedylandev/darkmatter-nvim',
  lazy = false,
  priority = 1000,
  config = function()
    vim.cmd('colorscheme darkmatter')
  end,
}
```

## Usage

Simply set the colorscheme in your Neovim configuration:

```lua
vim.cmd('colorscheme darkmatter')
```

If you don't see colors, make sure you have true color support enabled:

```lua
vim.opt.termguicolors = true
```

## Configuration

You can configure the colorscheme by passing options to the setup function:

```lua
require('darkmatter').setup({
  -- All options default to true
  telescope = true,          -- Telescope plugin
  telescope_borders = false, -- Telescope borders
  indentblankline = true,    -- Indent-blankline plugin
  notify = true,             -- Nvim-notify plugin
  ts_rainbow = true,         -- Rainbow parentheses
  cmp = true,                -- Nvim-cmp plugin
  illuminate = true,         -- vim-illuminate plugin
  lsp_semantic = true,       -- LSP semantic tokens
  mini_completion = true,    -- mini.completion plugin
  dapui = true,              -- nvim-dap-ui plugin
})
```

## Credits

This colorscheme is based on the base16-black-metal-bathory palette and was inspired by various dark themes in the Neovim ecosystem, and the base for this plugin is pulled from [base16-nvim](https://github.com/RRethy/base16-nvim)
