# Delete Git Commits

* [Delete Commits from a branch in Git](https://stackoverflow.com/questions/1338728/delete-commits-from-a-branch-in-git)

**Caution**: `git reset --hard` *WILL DELETE YOUR WORKING DIRECTORY CHANGES*.<br />
Be sure to stash any local changes you want to keep before running this command.

```bash
# Delete one commit before `HEAD` (latest commit):
$ git reset --hard HEAD~1
# HEAD~1 means the commit before head.
# Increasing the `1` will delete the given number of commits before HEAD.
#
# You can also delete commits by their SHA-1 hash:
$ git reset --hard <sha1-commit-id>
#
# If the commit has already been pushed, you must force push to delete:
$ git push origin HEAD --force
# 
# If collaborating, it may be better to create a 'mirror image' commit:
$ git revert
# This will undo the changes but both commits will be in the log.
```

---
