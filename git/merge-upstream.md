# Merging an upstream repository into your fork

> If you don't have push (write) access to an upstream repository,
> then you can pull commits from that repository into your own fork.

[source](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/merging-an-upstream-repository-into-your-fork)

---

1. Open Git Bash.
2. Change the current working directory to your local project.
3. Check out the branch you wish to merge to. Usually, you will merge into master.

    `$ git checkout master`

4. Pull the desired branch from the upstream repository. This method will retain the commit history without modification.

    `$ git pull https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git BRANCH_NAME`

5. If there are conflicts, resolve them. For more information, see "Addressing merge conflicts".
6. Commit the merge.
7. Review the changes and ensure they are satisfactory.
8. Push the merge to your GitHub repository.

    `$ git push origin master`

---
