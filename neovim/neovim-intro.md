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
* [Setting up Python for Neovim](https://github.com/deoplete-plugins/deoplete-jedi/wiki/Setting-up-Python-for-Neovim)

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

```vim
call plug#begin('~/AppData/Local/nvim/plugged')
" below are some vim plugin for demonstration purpose
Plug 'joshdick/onedark.vim'
Plug 'iCyMind/NeoSolarized'

Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'
call plug#end()
```

When you use `:PlugInstall`, all the plugins will be installed under `~/AppData/Local/nvim/plugged`. You can change this directory to where you want.

#### Example init.vim

```vim
" Specify a directory for plugins
" - For Neovim: stdpath('data') . '/plugged'
" - Avoid using standard Vim directory names like 'plugin'
call plug#begin('~/.vim/plugged')

" Make sure you use single quotes

" Shorthand notation; fetches https://github.com/junegunn/vim-easy-align
Plug 'junegunn/vim-easy-align'

" Any valid git URL is allowed
Plug 'https://github.com/junegunn/vim-github-dashboard.git'

" Multiple Plug commands can be written in a single line using | separators
Plug 'SirVer/ultisnips' | Plug 'honza/vim-snippets'

" On-demand loading
Plug 'scrooloose/nerdtree', { 'on':  'NERDTreeToggle' }
Plug 'tpope/vim-fireplace', { 'for': 'clojure' }

" Using a non-master branch
Plug 'rdnetto/YCM-Generator', { 'branch': 'stable' }

" Using a tagged release; wildcard allowed (requires git 1.9.2 or above)
Plug 'fatih/vim-go', { 'tag': '*' }

" Plugin options
Plug 'nsf/gocode', { 'tag': 'v.20150303', 'rtp': 'vim' }

" Plugin outside ~/.vim/plugged with post-update hook
Plug 'junegunn/fzf', { 'dir': '~/.fzf', 'do': './install --all' }

" Unmanaged plugin (manually installed and updated)
Plug '~/my-prototype-plugin'

" Initialize plugin system
call plug#end()
```

#### Vim-Plug Commands

```vim
" Check the status of plugins
PlugStatus
" Install a plugin
PlugInstall
```

---

## Extensions & Plugins

* [`awesome-vim`](https://github.com/akrawchyk/awesome-vim)
* [`oh-my-vim`](https://github.com/liangxianzhe/oh-my-vim)
* [`vim-galore`](https://github.com/mhinz/vim-galore)

---
