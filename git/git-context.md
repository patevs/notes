# Remove 'Git GUI Here' From Context Menu

> How to remove 'Git GUI Here' from the windows explorer right-click context menu.
---

## Links & Resources

- [Remove Git GUI Here](https://www.reddit.com/r/git/comments/a8lk83/how_do_i_remove_git_gui_here_and_git_bash_here/)
- [Remove msysgits menu options](https://stackoverflow.com/questions/2459763/how-do-i-remove-msysgits-right-click-menu-options)

---

## Instructions

Delete the following registry keys:


```
HKEY_CLASSES_ROOT\Directory\shell\git_gui
HKEY_CLASSES_ROOT\Directory\shell\git_shell
HKEY_CLASSES_ROOT\LibraryFolder\background\shell\git_gui
HKEY_CLASSES_ROOT\LibraryFolder\background\shell\git_shell
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Directory\background\shell\git_gui
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Directory\background\shell\git_shell
```

---
