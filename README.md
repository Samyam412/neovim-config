# Neovim Configuration (LazyVim)

Welcome to my customized Neovim configuration repository! This setup leverages the power of [LazyVim](https://github.com/LazyVim/LazyVim) and fine-tuned key mappings for an efficient coding experience.

## Features

- **LazyVim Integration**: Clean, modular plugin management via [lazy.nvim](https://github.com/folke/lazy.nvim).
- **Custom Keymaps**: Tailored keybindings for navigation, splits, tabs, and editing workflows.
- **Plugin Support**: Tools like Prettier, ESLint, and Harpoon2 are pre-configured for smooth development.
- **Performance Tweaks**: Disabled unused built-in plugins for faster startup.
- **Undo Tree**: Visualize and toggle undo history seamlessly.

## Requirements

- **Neovim**: Version 0.8 or higher.
- **Git**: For plugin management.
- **Language Tools**: Tools like `eslint`, `prettier`, and respective LSP servers for your languages.

## Installation

1. **Install Neovim** (v0.8+):
   - Check your version:
     ```bash
     nvim --version
     ```

2. **Clone the repository** into your Neovim config folder:
   ```bash
   git clone https://github.com/Samyam412/neovim-config.git ~/.config/nvim
   ```

3. **Start Neovim** to automatically bootstrap LazyVim:
   ```bash
   nvim
   ```

4. **Install Plugins**: LazyVim will handle plugin installation automatically on first launch.

## Key Bindings

### General Mappings

| Key               | Action                         |
|-------------------|--------------------------------|
| `x`               | Delete without yanking         |
| `+` / `-`         | Increment / Decrement numbers  |
| `<C-a>`           | Select all                     |
| `<Leader>rn`      | Rename symbol (IncRename)      |

### Editing

| Key                 | Action                               |
|---------------------|--------------------------------------|
| `<Leader>p`         | Paste without yanking               |
| `<Leader>d`         | Delete to blackhole register        |
| `<S-Up>` / `<S-Down>` | Move lines up/down in visual mode |
| `J`                 | Join lines without cursor movement  |
| `<C-d>` / `<C-u>`   | Scroll down/up and center           |
| `n` / `N`           | Search next/prev with centering     |

### Splits and Tabs

| Key               | Action                        |
|-------------------|-------------------------------|
| `ss` / `sv`       | Split horizontally/vertically |
| `sh/sk/sj/sl`     | Move focus between splits     |
| `<C-S-Up/Down>`   | Resize window vertically      |
| `<C-S-Left/Right>`| Resize window horizontally    |
| `te`              | Open a new tab                |
| `<Tab>` / `<S-Tab>` | Navigate tabs forward/back |

### Undo Tree

| Key               | Action                        |
|-------------------|-------------------------------|
| `<Leader>ut`      | Toggle Undo Tree              |

### Save and Quit

| Key               | Action                        |
|-------------------|-------------------------------|
| `<Leader>w`       | Save file                     |
| `<Leader>q`       | Quit                          |
| `<Leader>Q`       | Quit all                      |

## Plugin Configuration

This setup uses LazyVim with the following additional configurations:

- **Harpoon2**: Efficient file navigation.
- **Prettier**: Code formatting support.
- **ESLint**: Linting for JavaScript/TypeScript projects.
- **UndoTree**: Visual undo history management.

To modify plugins, update the `lua/plugins` directory.

### `plugins` Directory Structure

| File               | Description                      |
|--------------------|----------------------------------|
| `autosave.lua`     | Auto-save configuration          |
| `colorscheme.lua`  | Colorscheme setup                |
| `telescope.lua`    | File searching and fuzzy finding |
| `treesitter.lua`   | Syntax highlighting              |
| `undotree.lua`     | Undo Tree integration            |

## Performance Tweaks

Unused default plugins have been disabled to reduce startup time:

```lua
performance = {
    rtp = {
        disabled_plugins = {
            "gzip",
            "tarPlugin",
            "tohtml",
            "tutor",
            "zipPlugin",
        },
    },
}
```

## Troubleshooting

- **Check Dependencies**:
   ```bash
   :checkhealth
   ```
- **Plugin Issues**: Run LazyVim plugin manager with `\u` to verify and update plugins.
- **Neovim Version**: Ensure Neovim is up-to-date.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

---

Enjoy coding with your optimized Neovim setup! 🚀
