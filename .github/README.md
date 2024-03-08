## AstroNvim personal fork of IFilella
Original branch in [AstroNvim](https://github.com/AstroNvim/AstroNvim)

##  Requirements

- [Nerd Fonts](https://www.nerdfonts.com/font-downloads) (_Optional with manual intervention:_ See [Documentation on customizing icons](https://docs.astronvim.com/Recipes/icons)) <sup>[[1]](#1)</sup>
- [Neovim 0.8+ (_Not_ including nightly)](https://github.com/neovim/neovim/releases/tag/stable)
- [Tree-sitter CLI](https://github.com/tree-sitter/tree-sitter/blob/master/cli/README.md) (_Note:_ This is only necessary if you want to use `auto_install` feature with Treesitter)
- A clipboard tool is necessary for the integration with the system clipboard (see [`:help clipboard-tool`](https://neovim.io/doc/user/provider.html#clipboard-tool) for supported solutions)
- Terminal with true color support (for the default theme, otherwise it is dependent on the theme you are using) <sup>[[2]](#2)</sup>
- Optional Requirements:
  - [ripgrep](https://github.com/BurntSushi/ripgrep) - live grep telescope search (`<leader>fw`)
  - [lazygit](https://github.com/jesseduffield/lazygit) - git ui toggle terminal (`<leader>tl` or `<leader>gg`)
  - [go DiskUsage()](https://github.com/dundee/gdu) - disk usage toggle terminal (`<leader>tu`)
  - [bottom](https://github.com/ClementTsang/bottom) - process viewer toggle terminal (`<leader>tt`)
  - [Python](https://www.python.org/) - python repl toggle terminal (`<leader>tp`)
  - [Node](https://nodejs.org/en/) - node repl toggle terminal (`<leader>tn`)

> <sup id="1">[1]</sup> All downloadable Nerd Fonts contain icons which are used by AstroNvim. Install the Nerd Font of your choice to your system and in your terminal emulator settings, set its font face to that Nerd Font. If you are using AstroNvim on a remote system via SSH, you do not need to install the font on the remote system.

> <sup id="2">[2]</sup> Note when using default theme: For MacOS, the default terminal does not have true color support. You will need to use [iTerm2](https://iterm2.com/), [Kitty](https://sw.kovidgoyal.net/kitty/), [WezTerm](https://wezfurlong.org/wezterm/), or another [terminal emulator](https://gist.github.com/XVilka/8346728#terminal-emulators) that has true color support.

## 🛠️ Installation

### Linux/Mac OS (Unix)

#### Install neovim
Install neovim from [https://github.com/neovim](https://github.com/neovim/neovim/blob/master/INSTALL.md)

#### Make a backup of your current nvim and shared folder

```shell
mv ~/.config/nvim ~/.config/nvim.bak
mv ~/.local/share/nvim ~/.local/share/nvim.bak
```

#### Clone the repository

```shell
git clone --depth 1 https://github.com/IFilella/AstroNvim_IFilella ~/.config/nvim
nvim
```

## 📦 Basic Setup

#### Install LSP

Enter `:LspInstall` followed by the name of the server you want to install<br>
Example: `:LspInstall jedi_language_server`

Note: If error during Lsp installation execute:
- MacOS:
```
brew install node
```
- Linux
```
sudo apt-get install npm
```

#### Install language parser

Enter `:TSInstall` followed by the name of the language you want to install<br>
Example: `:TSInstall python`

#### Install Debugger

Enter `:DapInstall` followed by the name of the debugger you want to install<br>
Example: `:DapInstall python`

#### Manage plugins

Run `:Lazy check` to check for plugin updates

Run `:Lazy update` to apply any pending plugin updates

Run `:Lazy clean` to remove any disabled or unused plugins

Run `:Lazy sync` to update and clean plugins

#### Update AstroNvim

Run `:AstroUpdate` to get the latest updates from the repository<br>

#### Update AstroNvim Packages

Run `:AstroUpdatePackages` (`<leader>pa`) to update both Neovim plugins and Mason packages

## Package Instalation with Mason

```
:Mason
```

```
:MasonInstall <plugin>
```

Plugins:
- Flake8: Syntaxis checker

## 🗒️ Links

[AstroNvim Website](https://astronvim.com)
[AstroNvim Documentation](https://docs.astronvim.com)
[Core AstroNvim LUA API Documentation](https://api.astronvim.com)

- [Basic Usage](https://docs.astronvim.com/basic-usage/walkthrough) is given for basic usage
- [Default Mappings](https://docs.astronvim.com/basic-usage/mappings) more about the default key bindings
- [Default Plugin Configuration](https://docs.astronvim.com/configuration/plugin_defaults) more about the provided plugin defaults
- [Advanced Configuration](https://docs.astronvim.com/configuration/config_options) more about advanced configuration

### 📹 Videos

There have been some great review videos released by members of the community! Here are a few:

- [Neovim With AstroNvim | Your New Advanced Development Editor](https://www.youtube.com/watch?v=GEHPiZ10gOk) (Version: 3, Content By: [@Cretezy](https://github.com/Cretezy))
- [Why I'm quitting VIM by Carlos Mafla](https://www.youtube.com/watch?v=71GDopdc9rw) (Version: 2, Content By: [@gigo6000](https://github.com/gigo6000))
- [Astro Vim - All in one Nvim config!! by John McBride](https://www.youtube.com/watch?v=JQLZ7NJRTEo) (Version: 1, Content By: [@jpmcb](https://github.com/jpmcb))

## 🚀 Contributing

If you plan to contribute, please check the [contribution guidelines](CONTRIBUTING.md) first.

## ⭐ Credits

Sincere appreciation to the following repositories, plugin authors and the entire neovim community out there that made the development of AstroNvim possible.

- [Plugins](https://docs.astronvim.com/acknowledgements#plugins-used-in-astronvim)
- [NvChad](https://github.com/NvChad/NvChad)
- [LunarVim](https://github.com/LunarVim)
- [CosmicVim](https://github.com/CosmicNvim/CosmicNvim)

<div align="center" id="madewithlua">

[![Lua](https://img.shields.io/badge/Made%20with%20Lua-blue.svg?style=for-the-badge&logo=lua)](https://lua.org)

</div>
