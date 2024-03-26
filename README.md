# Jot.lua

Jot down everything about the *project* in one place.

**Features:**

* Jot per project in a `markdown` file.
* Customizable jot window

## Installation

* With **lazy.nvim**
```lua
{
  "letieu/jot.lua",
  dependencies = { "nvim-lua/plenary.nvim" }
}
```
* With **packer.nvim**
```lua
use {
  'letieu/jot.lua',
  requires = {{'nvim-lua/plenary.nvim'}}
}
```

## Usage

Open
```lua
require('jot').open()
```

Close use `quit_key` in config

Map open to a key
```lua
vim.keymap.set("n", "<leader>fj", function() require("jot").open() end, { noremap = true, silent = true })
```

## Config

Default config

```lua
{
  quit_key = "q",
  notes_dir = vim.fn.stdpath("cache") .. "/jot",
  win_opts = {
    split = "right",
    focusable = false,
  },
}
```

## Q&A
- What differentiates `jot.lua` from `flote.nvim`?
  - `flote.nvim` open in a floating window, I want to open in a split window.
  - `jot.lua` can customize the window options. Can use floating window if you want.
  - `jot.lua` use `plenary.nvim` to handle file operations.
  - `jot.lua` no need `setup` call

## Inspiration and Thanks
- [Flote.nvim](https://github.com/JellyApple102/flote.nvim) by @JellyApple102