# Introduction to Neovim

> Neovim is a refactor, and sometimes redactor, in the tradition of Vim (which itself derives from Stevie). It is not a rewrite but a continuation and extension of Vim. Many clones and derivatives exist, some very clever—but none are Vim. Neovim is built for users who want the good parts of Vim, and more.

[neovim.io](https://neovim.io/)

---

## Links & Resources

* [`neovim/neovim`](https://github.com/neovim/neovim)
* [`neovim/wiki`](https://github.com/neovim/neovim/wiki)
* [Documentation](https://neovim.io/doc/)

[](.)

* [Neovim Setup Guide](https://jdhao.github.io/2018/12/24/centos_nvim_install_use_guide_en/)
* [Neovim Configuration Windows](https://jdhao.github.io/2018/11/15/neovim_configuration_windows/)

---

## Install Neovim using Chocolately

* [`chocolately/neovim`](https://chocolatey.org/packages?q=neovim)

```powershell
    choco install neovim -y
```

---

## Basic Usage

```powershell
nvim --version # get version
nvim # start neovim
nvim :checkhealth # run a health check
nvim :help init.vim # configuration information
```

### Configuration File Location

[Neovim Windows init.vim location #3700](https://github.com/neovim/neovim/issues/3700#issuecomment-157778920)

> ➡️ ~/AppData/Local/nvim/init.vim

* Windows 10: `~/APPDATA/Local/nvim/init.vim`

### Install plugin-manager vim-plug

To install vim-plug on Windows, open a PowerShell terminal (not Windows CMD), and execute the following command:

```powershell
md ~\AppData\Local\nvim\autoload
$uri = 'https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
(New-Object Net.WebClient).DownloadFile(
  $uri,
  $ExecutionContext.SessionState.Path.GetUnresolvedProviderPathFromPSPath(
    "~\AppData\Local\nvim\autoload\plug.vim"
  )
)
```

In Neovim config file, use the following settings for vim-plug:

```powershell
call plug#begin('~/AppData/Local/nvim/plugged')
" below are some vim plugin for demonstration purpose
Plug 'joshdick/onedark.vim'
Plug 'iCyMind/NeoSolarized'

Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'
call plug#end()
```

When you use `:PlugInstall`, all the plugins will be installed under `~/AppData/Local/nvim/plugged`. You can change this directory to where you want.

---

## Extensions & Plugins

* [`awesome-vim`](https://github.com/akrawchyk/awesome-vim)
* [`oh-my-vim`](https://github.com/liangxianzhe/oh-my-vim)
* [`vim-galore`](https://github.com/mhinz/vim-galore)

---
