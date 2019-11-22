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

## Feature Branchs

## Hotfix Branchs

## Release Branchs

---
