---
title: Bash Basics
tags: [Bash, Notebooks/Bash]
created: '2019-03-16'
modified: '2019-06-26'
---

# Bash Basics

16/03/2019

> Introduction to `bash` (**B**orn **A**gain **SH**ell) and the `git-bash` terminal.

----

Git for Windows provides a BASH emulation used to run Git from the command line.

Download git-for-windows: [Here](https://gitforwindows.org/)

Update git-for-windows using the following command:

```bash
git update-git-for-windows
```

----

## Links & Resources

- [Bash Website](https://www.gnu.org/software/bash/)
- [`bash-it`](https://github.com/Bash-it/bash-it)
- [`bash-powerline`](https://github.com/riobard/bash-powerline)
- [`bobthecow/git-flow-completion`](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion)
- [`lyze/posh-git-sh`](https://github.com/lyze/posh-git-sh)
- [Customize bash prompt](https://www.howtogeek.com/307701/how-to-customize-and-colorize-your-bash-prompt/)

----

### Install `git-flow-completion`

Download and place `git-flow-completion.bash` in home directory (~/ in msysgit shell)

Add a `.bashrc` file to your home directory with the following line (or add this line to existing .bashrc file):

```bash
source ~/git-flow-completion.bash
```

----

### Install `posh-git-sh`

Download and place `git-prompt.sh` file to somewhere (e.g., ~/git-prompt.sh).

Add the following line to your `~/.bashrc`. (You may need to update your `~/.bash_profile` to source your ~/.bashrc, or you can just modify ~/.bash_profile directly.)

```bash
source ~/git-prompt.sh
```

If you are using `bash`, you should call `__posh_git_ps1` in your `PROMPT_COMMAND` variable. The function `__posh_git_ps1` takes two parameters (`__posh_git_ps1 <prefix> <suffix>`), and sets PS1 to `<prefix><status><suffix>`. You can also use `__posh_git_echo` to echo only the status.

**Bash example:**

```bash
PROMPT_COMMAND='__posh_git_ps1 "\u@\h:\w " "\\\$ ";'$PROMPT_COMMAND
```

This shows username, at-sign, host, colon, cwd, then various status strings, followed by dollar and space, as your prompt. This invocation prepends this instruction to the existing value of `PROMPT_COMMAND`.

**Example `.bashrc`**

```bash
source ~/git-flow-completion.bash
source ~/git-prompt.sh

PROMPT_COMMAND='__posh_git_ps1 "\[\033[01;32m\]\h \[\033[00m\]: \[\033[01;34m\]\w \[\033[00m\]: " "\n \[\033[00m\]$ ";'$PROMPT_COMMAND

alias gs='git status'
```

----
