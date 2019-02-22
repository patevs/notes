---
title: Python Basics
created: '2019-02-19T22:14:54.049Z'
modified: '2019-02-22T05:47:44.124Z'
tags: [Notebooks/Python, Python]
---

# Python Basics

> 20/02/2019

----

Introduction to the [`Python`](https://www.python.org/) programming language including installation methods and basic commands.

> "Python is an interpreted, high-level, general-purpose programming language. Python features a dynamic type system and automatic memory management. It supports multiple programming paradigms, including object-oriented, imperative, functional and procedural, and has a large and comprehensive standard library." 
[Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

Python Home: https://www.python.org/

----

## Installing Python

There are many ways of installing Python so choose **ONLY ONE** of the methods below.

1. Download and run **Python** installer: 
  https://www.python.org/downloads/

2. Download and run **Anaconda** installer:
  https://www.anaconda.com/distribution/

3. Install using Chocolatey:
  https://chocolatey.org/packages/python
  https://chocolatey.org/packages/anaconda3
  *Note:* requires Chocolatey to be installed.
  ```powershell
  # Run from an elevated (Administrator) command prompt
  choco install python -y 
  # OR
  choco install anaconda3 -y
  ```

## Basic Commands

```powershell
# Print Python version
# Useful to check Python has been correctly installed
python -V

# Print a help message 
# Includes an overview of useful commands
python -h
```


----
