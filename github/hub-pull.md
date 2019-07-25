# GitHub Pull Request and Merge

> How to create a github pull request and then merge that pull request from the command line.

---

## Links & Resources

- [hub-pull-request](https://hub.github.com/hub-pull-request.1.html)
- [hub-merge](https://hub.github.com/hub-merge.1.html)

---

## Usage

Create a pull request:

```sh
$ hub pull-request --browse -m "My title"
# Creates a pull request with the given title and opens it in a browser
```

Merge a pull request:

```sh
$ hub merge https://github.com/jingweno/gh/pull/73
# Merge pull request number 73
```

---
