# Git: Fix CRLF Line Endings

---

* [Configure `git diff` to ignore `^M`](https://stackoverflow.com/questions/1889559/git-diff-to-ignore-m)

Convert from `CRLF` to `LF`:

```bash
# Remove everything from the index.
$ git rm --cached -r .
#
# Re-add all deleted files to the index.
$ git diff --cached --name-only -z | xargs -0 git add
#
# Note for Windows users: 
#   `xargs` is provided by git unix tools and will be 
#   available by adding `$GIT_HOME/usr/bin` to `$PATH`.
#
# Commit
$ git commit -m "Fix CRLF"
```

More info [here](https://docs.github.com/en/get-started/getting-started-with-git/configuring-git-to-handle-line-endings).

---
