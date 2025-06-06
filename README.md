# VSCode Vim Configuration

If you use neovim often but have to use VSCode or Cursor for some reason, this configuration might help you get a similar experience, where most of the editor features are accessible via vim motions.

This is my personal config with some other stuff for languages and UI customizations, feel free to take what you like

## 🚀 Quick Start

### Installation

1. **Copy the settings**: Replace your VSCode settings with the provided `settings.json`
   - **macOS/Linux**: `~/.config/Code/User/settings.json`
   - **Windows**: `%APPDATA%\Code\User\settings.json`
2. **Install required extensions** (see list below)
3. **Restart VSCode**

### Required Extensions

Install these extensions for full functionality:

1. Vim (Vim motions and allows you to bind leader key to all sorts of actions, unlike vscode-neovim): https://marketplace.visualstudio.com/items?itemName=vscodevim.vim
2. Search Preview (Extension to peek at files and oldflies while searching, just like telescope): https://marketplace.visualstudio.com/items?itemName=zaidalsaheb.search-preview
3. Periscope(Ripgrep through entire code base with peeking): https://marketplace.visualstudio.com/items?itemName=JoshMu.periscope
4. Harpoon(Fast navigation between files, persists across sessions unlike marks): https://marketplace.visualstudio.com/items?itemName=tobias-z.vscode-harpoon
5. LazyGit(better git interface): https://marketplace.visualstudio.com/items?itemName=TomPollak.lazygit-vscode




## ⌨️ Key Mappings

All custom mappings use `<Space>` as the leader key.

### File Navigation (Harpoon)
| Key | Action |
|-----|--------|
| `<leader>a` | Add current file to Harpoon |
| `<leader>e` | Edit Harpoon file list |
| `<leader>pe` | Quick pick Harpoon files |
| `<leader>1-4` | Go to Harpoon file 1-4 |

### Search & Files
| Key | Action |
|-----|--------|
| `<leader>fg` | Search in files (Periscope) |
| `<leader>ff` | Quick open with preview |
| `<leader><leader>` | Recent files by usage |

### Git Integration
| Key | Action |
|-----|--------|
| `<leader>lg` | Toggle LazyGit |

### Code Actions
| Key | Action |
|-----|--------|
| `<leader>gd` | Go to definition |
| `<leader>gf` | Format document |
| `-` | Open file explorer (vsnetrw) |

### UI Customizations
- Sidebar moved to right side
- Relative line numbers enabled
- Breadcrumbs disabled for cleaner look
- Editor actions hidden
- Sticky scroll disabled

## 🔧 Customization

### Changing the Leader Key
To use a different leader key, modify:
```json
"vim.leader": "<your-key>"
```

### Adding Custom Keybindings
Add new mappings to the `vim.normalModeKeyBindings` array:
```json
{
    "before": ["<leader>", "your", "keys"],
    "commands": ["command.name"]
}
```