---
title: Python Basics
created: '2019-02-19T22:14:54.049Z'
modified: '2019-03-05T02:11:08.121Z'
tags: [Notebooks/Python, Python]
---

# Python Basics

> 20/02/2019

----

Introduction to the [`Python`](https://www.python.org/) programming language including installation methods and basic commands.

> "Python is an interpreted, high-level, general-purpose programming language. Python features a dynamic type system and automatic memory management. It supports multiple programming paradigms, including object-oriented, imperative, functional and procedural, and has a large and comprehensive standard library." 
[Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

----

## Links & Resources

* [Homepage](https://www.python.org/)
* [Documentation](https://www.python.org/doc/)

----

### Installing Python

Choose one of the following installation methods

#### Native Python

* Download and run the native **Python** installer: 
  https://www.python.org/downloads/

#### Anaconda

* Download and run the **Anaconda** installer:
  https://www.anaconda.com/distribution/

#### Chocolatey
*Note:* requires Chocolatey to be installed.
  * [`python3`](https://chocolatey.org/packages/python)
  * [`anaconda3`](https://chocolatey.org/packages/anaconda3)
  ```powershell
  # Run from an elevated (Administrator) command prompt
  choco install python -y 
  # OR
  choco install anaconda3 -y
  ```

## Basic Commands

#### Python

```powershell
# Print Python version
# Useful to check Python has been correctly installed
python -V

# Print help message 
# Overview of useful commands
python -h
```

#### Anaconda

```powershell
# Print anaconda version
conda -v

# Print help message
conda -h
```


----
