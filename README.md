# VS Code Configuration Documentation

This document describes the VS Code extensions and custom keybindings configured in this setup.

## Required VS Code Extensions

The following extensions are required for the `settings.json` configuration to work properly:

### Core Extensions

1. **Vim** (`vscodevim.vim`)
   - Provides Vim emulation for VS Code
   - Configured with custom keybindings, relative line numbers, and clipboard integration
   - EasyMotion and incremental search enabled

2. **Material Icon Theme** (`pkief.material-icon-theme`)
   - Icon theme for the file explorer
   - Configured to hide explorer arrows and full saturation

3. **Catppuccin** (`catppuccin.catppuccin-vsc`)
   - Color theme (Catppuccin Frappé variant)
   - Configured without italic keywords and comments

4. **Prettier** (`esbenp.prettier-vscode`)
   - Code formatter for TypeScript, JavaScript, JSON, and JSONC files
   - Set as default formatter with format-on-save enabled for:
     - TypeScript (`.ts`)
     - TypeScript React (`.tsx`)
     - JavaScript (`.js`)
     - JSON (`.json`)
     - JSONC (`.jsonc`)

5. **CSharpier** (`csharpier.csharpier-vscode`)
   - Code formatter for C# files
   - Set as default formatter with format-on-save and format-on-type enabled

6. **Coverage Gutters** (`ryanluker.vscode-coverage-gutters`)
   - Displays test coverage information in the editor
   - Configured to read various coverage file formats (lcov.info, cobertura.xml, etc.)

7. **Custom UI Style** (extension for custom CSS)
   - Allows custom styling for VS Code UI elements
   - Configured to adjust quick input widget position

### C# Development Extensions (Implied)

8. **.NET and C# Extensions** (`ms-dotnettools.csdevkit`, `ms-dotnettools.vscode-dotnet-runtime`)
   - Required for C# development features
   - Referenced in globalStorage

### Optional/Related Extensions

9. **GitHub Copilot** (`github.copilot-chat`)
   - AI-powered code completion
   - Next edit suggestions enabled

## Custom Keybindings

### Window Navigation

| Keybinding | Command | Description |
|------------|---------|-------------|
| `Ctrl+W E` | `workbench.view.explorer` | Open Explorer view |
| `Ctrl+W T` | `workbench.view.extension.test` | Open Test view |
| `Ctrl+W G` | `workbench.view.scm` | Open Source Control view |
| `Ctrl+W Q` | `workbench.view.extension.sln_explorer` | Open Solution Explorer |
| `Ctrl+W X` (uppercase) | `workbench.view.extensions` | Open Extensions view |
| `Ctrl+W X` (lowercase) | `workbench.action.closeGroup` | Close editor group |
| `Ctrl+N` | `workbench.action.toggleSidebarVisibility` | Toggle sidebar visibility |

### Editor Pane Navigation

| Keybinding | Command | Description |
|------------|---------|-------------|
| `Ctrl+W Left` | `workbench.action.navigateLeft` | Focus editor pane to the left |
| `Ctrl+W Right` | `workbench.action.navigateRight` | Focus editor pane to the right |
| `Ctrl+W Up` | `workbench.action.navigateUp` | Focus editor pane above |
| `Ctrl+W Down` | `workbench.action.navigateDown` | Focus editor pane below |
| `Ctrl+W Enter` | `workbench.action.focusActiveEditorGroup` | Return focus to editor from Explorer |

### Editor Pane Management

| Keybinding | Command | Description |
|------------|---------|-------------|
| `Ctrl+W S` | `workbench.action.splitEditorDown` | Split editor horizontally (below) |
| `Ctrl+W V` | `workbench.action.splitEditorRight` | Split editor vertically (right) |
| `Ctrl+W W` | `workbench.action.closeActiveEditor` | Close active editor |
| `Ctrl+Shift+W` | `workbench.action.closeActiveEditor` | Close active editor (alternative) |
| `Shift+Alt+W` | `workbench.action.closeWindow` | Close window |

### View Size Adjustment

| Keybinding | Command | Description |
|------------|---------|-------------|
| `Alt+Left` | `workbench.action.decreaseViewSize` | Decrease view size |
| `Alt+Right` | `workbench.action.increaseViewSize` | Increase view size |

### Terminal

| Keybinding | Command | Description |
|------------|---------|-------------|
| `Alt+I` | `workbench.action.terminal.toggleTerminal` | Toggle terminal visibility |
| `Ctrl+Up` | `workbench.action.terminal.scrollUp` | Scroll terminal up (when focused) |
| `Ctrl+Down` | `workbench.action.terminal.scrollDown` | Scroll terminal down (when focused) |
| `Ctrl+PageUp` | `workbench.action.terminal.scrollUpPage` | Scroll terminal up one page (when focused) |
| `Ctrl+PageDown` | `workbench.action.terminal.scrollDownPage` | Scroll terminal down one page (when focused) |

### Code Actions & Navigation

| Keybinding | Command | Description |
|------------|---------|-------------|
| `Ctrl+Space` | `editor.action.showHover` | Show hover information |
| `Ctrl+P` | `workbench.action.quickOpen` | Quick open (when in Vim Normal mode) |
| `Ctrl+T` | `workbench.action.showAllSymbols` | Go to symbol (when in Vim Normal mode) |
| `Ctrl+K Ctrl+C` | `editor.action.commentLine` | Comment/uncomment line |
| `Ctrl+G E` | `editor.action.marker.nextInFiles` | Go to next error/warning |

### Testing

| Keybinding | Command | Description |
|------------|---------|-------------|
| `Alt+T` | `testing.runAtCursor` | Run test at cursor |
| `Alt+D` | `testing.debugAtCursor` | Debug test at cursor |
| `Q` | `editor.closeTestPeek` | Close test peek view (in Vim Normal mode) |

### File Explorer

| Keybinding | Command | Description |
|------------|---------|-------------|
| `Alt+N` | `explorer.newFile` | Create new file (when Explorer is visible) |
| `Ctrl+W Down` | `workbench.action.nextSideBarView` | Next sidebar view (when sidebar focused) |
| `Ctrl+W Up` | `workbench.action.previousSideBarView` | Previous sidebar view (when sidebar focused) |

## Vim-specific Keybindings

These are configured within the Vim extension settings:

### Normal Mode

| Keybinding | Action | Description |
|------------|--------|-------------|
| `å` | `{` | Jump to previous paragraph |
| `ä` | `}` | Jump to next paragraph |
| `gi` | Go to Implementation | Navigate to implementation |
| `gr` | Go to References | Show references |
| `<leader>d` | `dd` | Delete line (leader = Space) |
| `Ctrl+N` | `:nohl` | Clear search highlights |
| `Space f f` | Find in Files | Search across all files |
| `Space x` | Close Editor | Close active editor |

### Insert Mode

| Keybinding | Action | Description |
|------------|--------|-------------|
| `jj` | `<Esc>` | Exit insert mode |

### Additional Vim Settings

- **Leader key**: `Space`
- **Relative line numbers**: Enabled
- **System clipboard**: Enabled
- **Incremental search**: Enabled
- **Search highlighting**: Enabled
- **EasyMotion**: Enabled

## Notes

- The configuration uses a window-management style similar to Vim/tmux with `Ctrl+W` as the primary prefix for navigation
- Terminal scrolling is remapped to avoid conflicts with editor navigation
- Arrow keys are enabled in Vim modes for easier navigation
- Format-on-save is enabled for TypeScript, JavaScript, JSON, and C# files
