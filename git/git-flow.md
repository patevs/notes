# Introduction the GitFlow Branching Model

> **GitFlow** is a branching model for `Git`, created by Vincent Driessen. It has attracted a lot of attention because it is very well suited to collaboration and scaling the development team.

---

## Links & Resources

- [GitFlow Branching Model](https://nvie.com/posts/a-successful-git-branching-model/)
- [Intro to GitFlow](https://datasift.github.io/gitflow/IntroducingGitFlow.html)
- [GitFlow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

---

## GitFlow Workflow

At the core, the development model is greatly inspired by existing models out there. The central repo holds two main branches with an infinite lifetime:

- master
- develop

The master branch at origin should be familiar to every Git user. Parallel to the master branch, another branch exists called develop.

We consider `origin/master` to be the main branch where the source code of HEAD always reflects a production-ready state.

---

## The Develop Branch

We consider `origin/develop` to be the main branch where the source code of HEAD always reflects a state with the latest delivered development changes for the next release. Some would call this the “integration branch”. This is where any automatic nightly builds are built from.

When the source code in the develop branch reaches a stable point and is ready to be released, all of the changes should be merged back into master somehow and then tagged with a release number.

---

## Feature Branches

May branch off from:
    `develop`
Must merge back into:
    `develop` 
Branch naming convention:
    anything except `master`, `develop`, `release-*`, or `hotfix-*`

Feature branches (or sometimes called topic branches) are used to develop new features for the upcoming or a distant future release.

When starting work on a new feature, branch off from the develop branch.

```bash
$ git checkout -b myfeature develop
# Switched to a new branch "myfeature"
```

Finished features may be merged into the develop branch to definitely add them to the upcoming release:

```bash
$ git checkout develop
# Switched to branch 'develop'
$ git merge --no-ff myfeature
# Updating ea1b82a..05e9557
# (Summary of changes)
$ git branch -d myfeature
# Deleted branch myfeature (was 05e9557).
$ git push origin develop
# Update origin/develop
```

---

## Release Branches

May branch off from:
    `develop`
Must merge back into:
    `develop` and `master`
Branch naming convention:
    `release-*`

Release branches support preparation of a new production release. They allow for last-minute dotting of i’s and crossing t’s. Furthermore, they allow for minor bug fixes and preparing meta-data for a release (version number, build dates, etc.). By doing all of this work on a release branch, the `develop` branch is cleared to receive features for the next big release.

Release branches are created from the develop branch.

```bash
$ git checkout -b release-1.2 develop
# Switched to a new branch "release-1.2"
$ ./bump-version.sh 1.2
# Files modified successfully, version bumped to 1.2.
$ git commit -a -m "Bumped version number to 1.2"
# [release-1.2 74d9424] Bumped version number to 1.2
# 1 files changed, 1 insertions(+), 1 deletions(-)
```

When the state of the release branch is ready to become a real release, some actions need to be carried out. First, the release branch is merged into `master` (since every commit on `master` is a new release by definition, remember). Next, that commit on `master` must be tagged for easy future reference to this historical version. Finally, the changes made on the release branch need to be merged back into `develop`, so that future releases also contain these bug fixes.

```bash
$ git checkout master
# Switched to branch 'master'
$ git merge --no-ff release-1.2
# Merge made by recursive.
# (Summary of changes)
$ git tag -a 1.2 -m "Release version 1.2"
# Tag release version
$ git push origin master --tags
# Update origin/master including tags
```

To keep the changes made in the release branch, we need to merge those back into `develop`, though.

```bash
$ git checkout develop
# Switched to branch 'develop'
$ git merge --no-ff release-1.2
# Merge made by recursive.
# (Summary of changes)
```

Now we are really done and the release branch may be removed, since we don’t need it anymore:

```bash
$ git branch -d release-1.2
# Deleted branch release-1.2 (was ff452fe).
```

---

## Hotfix Branches

---
