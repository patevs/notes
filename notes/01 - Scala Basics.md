---
title: 01 - Scala Basics
created: '2019-03-17T23:30:57.500Z'
modified: '2019-03-17T23:41:29.591Z'
tags: [Notebooks/Scala, Scala]
---

# 01 - Scala Basics

<span style="text-decoration: underline black;">18/03/2019</span>

Introduction to the [`Scala`](https://scala-lang.org/) programming language.

> "`Scala` is a general-purpose programming language providing support for functional programming and a strong static type system. Designed to be concise, many of Scala's design decisions aimed to address criticisms of `Java`." [Wikipedia](https://en.wikipedia.org/wiki/Scala_(programming_language))

You can run Scala in your browser with [ScalaFiddle](https://scalafiddle.io).

----

### Links & Resources

* [Homepage](https://scala-lang.org/)
* [Download](https://scala-lang.org/download/)
* [Documentation](https://docs.scala-lang.org/)
* [Getting Started](https://docs.scala-lang.org/getting-started.html)
* [Tour of Scala](https://docs.scala-lang.org/tour/tour-of-scala.html)
* [Cheat Sheet](https://docs.scala-lang.org/cheatsheets/index.html)
* [Library Index](https://index.scala-lang.org/)

----

### Hello World Example

```scala
object HelloWorld extends App {
  println("Hello, World!")
}
```

When the program is stored in file `HelloWorld.scala`, the user compiles it with the command: 

```cmd
scalac HelloWorld.scala
```

and runs it with:

```cmd
scala HelloWorld
```

----
