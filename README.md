<p align="center">
  <img src="https://github.com/user-attachments/assets/f22a2b1d-a052-4694-8296-0ebee04e392f" alt="mmerr" width="746">
</p>

**mmerr** is a dark colorscheme for Neovim, inspired by the anime *Cyberpunk: Edgerunners*.

It aims to be a simple theme with a cyberpunk edge, using as few colors as possible.
Character-inspired accent colors from both seasons are woven throughout the theme.
(Rebecca is my oshi! And congrats on the release of Season 2!!🎉)

> This is an unofficial, fan-made theme.

![mmerr screenshot](https://github.com/user-attachments/assets/295af4a1-09d9-48bc-9eaa-77bcc879b317)

## Requirements

- Neovim 0.10+
- True color terminal

## Installation

Install with your favorite plugin manager. For example, with [lazy.nvim](https://github.com/folke/lazy.nvim):

```lua
{
  "mmugi/mmerr.nvim",
  lazy = false,
  priority = 1000,
  opts = {}, -- see Configuration
}
```

## Usage

```lua
vim.cmd.colorscheme("mmerr")
```

## Configuration

To customize the default settings, call `setup()` before loading the colorscheme.

```lua
-- Default Options
require("mmerr").setup({
  transparent_bg = false, -- unsets the background colors
  terminal_colors = true, -- sets the colors for :terminal
  palette_overrides = {},
  highlight_overrides = {},
})

-- setup() must be called before loading the colorscheme
vim.cmd.colorscheme("mmerr")
```

> [!TIP]
> With lazy.nvim, you can pass the same table as `opts` instead:
>
> ```lua
> {
>   "mmugi/mmerr.nvim",
>   lazy = false,
>   priority = 1000,
>   opts = {
>     transparent_bg = true,
>   },
> }
> ```

### Overrides

You can override the palette and highlight groups with `palette_overrides` and `highlight_overrides`.

#### Palette

```lua
require("mmerr").setup({
  palette_overrides = {
    bg = "#1a1b26",
  },
})
```

#### Highlight groups

```lua
require("mmerr").setup({
  highlight_overrides = function(palette)
    return {
      Comment = { fg = palette.lavender, italic = true },
      MyPluginGroup = { fg = palette.rose },
    }
  end,
})
```

Each entry replaces the whole group, so attributes you don't specify are cleared.
You can also add groups for other plugins or your own config.

## Using the palette

To use the colors in your own config, `get_palette()` returns a table of color names and their hex values:

```lua
local palette = require("mmerr").get_palette()
-- { bg = "#222641", fg = "#eff7fe", red = "#ea5950", ... }
```
