# Git Context Menu Intergation Windows 10

---

## Remove 'Git GUI Here' from Context Menu

> How to remove 'Git GUI Here' from the windows explorer right-click context menu.

---

- [Remove Git GUI Here](https://www.reddit.com/r/git/comments/a8lk83/how_do_i_remove_git_gui_here_and_git_bash_here/)
- [Remove msysgits menu options](https://stackoverflow.com/questions/2459763/how-do-i-remove-msysgits-right-click-menu-options)

---

### Instructions

Delete the following registry keys:

```md
HKEY_CLASSES_ROOT\Directory\shell\git_gui
HKEY_CLASSES_ROOT\LibraryFolder\background\shell\git_gui
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Directory\background\shell\git_gui
```

---

## Add `Git Bash Here` to Context Menu

> How to add 'Git Bash Here' to the windows explorer right-click context menu.

---

- [Add Git Bash to Windows 10 Context Menu](https://github.com/Jackool/add-git-bash-to-windows10-context-menu)
- [GitHub For Windows "Open with Git Bash" Context Menu Script](https://gist.github.com/branden-akana/a9e07c1f0bfe193f47fe)
- [Open Git Bash Here Context Menu](https://stackoverflow.com/questions/24386657/how-to-add-a-open-git-bash-here-context-menu-to-the-windows-explorer)

---
