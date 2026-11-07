<p align="center">
  <img src="https://github.com/user-attachments/assets/f22a2b1d-a052-4694-8296-0ebee04e392f" alt="mmerr" width="746">
</p>

**mmerr** is a dark colorscheme for Neovim, inspired by the anime *Cyberpunk: Edgerunners*.
Character-inspired accent colors from both seasons are woven throughout the theme.

> This is an unofficial, fan-made theme.

![mmerr screenshot](https://github.com/user-attachments/assets/e72ed3ee-7b79-4b36-9199-09a55267faa2)

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
  edit_highlights = function(groups, palette) end,
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

You can override the palette with `palette_overrides` and the highlight groups with `edit_highlights`.

#### Palette

```lua
require("mmerr").setup({
  palette_overrides = {
    bg = "#1a1b26",
  },
})
```

#### Highlight groups

`edit_highlights` is called with the highlight groups and the palette.
In this function, edit the highlight groups to change some attributes of a group, replace a group, or add your own groups.

```lua
require("mmerr").setup({
  edit_highlights = function(groups, palette)
    groups.Comment.italic = true
    groups.Pmenu.bg = nil
    groups.MyHighlightGroup = { fg = palette.red }
  end,
})
```

> [!NOTE]
> Attributes set together with `link` are ignored.
> To add attributes to a linked group, replace it with the group it links to, extended with the attributes:
>
> ```lua
> groups.FloatTitle = vim.tbl_extend("force", groups.Title, { italic = true })
> ```

## Using the palette

To use the colors in your own config, `get_palette()` returns a table of color names and their hex values:

```lua
local palette = require("mmerr").get_palette()
-- { bg = "#222641", fg = "#eff7fe", red = "#ea5950", ... }
```
