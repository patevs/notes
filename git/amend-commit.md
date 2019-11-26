# Amending a Commit Message

> If a commit message contains unclear, incorrect, or sensitive information, you can amend it locally and push a new commit with a new message to GitHub. You can also change a commit message to add missing information.

---

## Links & Resources

- [Changing a Commit Message](https://help.github.com/en/github/committing-changes-to-your-project/changing-a-commit-message)

---

## Instructions

Run the following command to change the most recent local commit message:

```bash
git commit --amend
```

If the commit has been push to remote then run the previous command then push over the previous commit using:

```bash
git push --force example-branch
```

---
