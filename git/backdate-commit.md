# Backdating a Git Commit

---

* [Backdating Git Commits](https://stackoverflow.com/questions/44559560/backdating-git-commits)

    ```bash
    git commit --amend --no-edit --date="Mon Mar 1 20:00:00 2021 +1300"
    ```

[](.)

* [Backdating GitHub Commits](https://www.reddit.com/r/git/comments/8hzji1/backdating_commitspushes_to_github/)

    ```bash
    export GIT_AUTHOR_DATE="Mon Mar 1 20:00:00 2021 +1300"
    export GIT_COMMITTER_DATE="Mon Mar 1 20:00:00 2021 +1300"
    git commit
    ```

The environment variables `GIT_AUTHOR_DATE` and `GIT_COMMITTER_DATE` can be used to make commits in the past.

More info [here](https://alexpeattie.com/blog/working-with-dates-in-git).

---
