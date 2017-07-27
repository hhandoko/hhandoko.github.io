---
layout: post
title:  "Beginning Scala Programming"
date:   2017-07-27 10:45:58 +0800
categories: posts
tags: update
---
Recently someone asked me *"Why Scala?"*, or a variation of it, e.g. *"Why do you use Scala?"*, or *"Why should I learn Scala?"*. The question had came up more and more often as Scala becomes more 'mainstream' and people are gaining more awareness of it.

I'll be honest, I didn't seek out to learn Scala (I'll tell this story later), but I am thankful to have learnt it: a language that's enjoyable to work in and supported by the rich and diverse JVM ecosystem.<!--more-->

For the most part, I am enjoying Scala because it offers me flexibility on how I can express my thoughts into code. '[Code is Prose](https://medium.com/@mb/code-is-prose-18461ee400e7)' is certainly very apt, and only possible because of its approach by way of a hybrid __Object-Oriented__ (OO) and __Functional Programming__ (FP), complemented with a __rich type system__.

*"I heard Scala code is impossible to read!"*. It depends, I think there are two contributing factors here:

* __Scala is full of context__<br>It will be hard and challenging for Scala beginners to identify them (e.g. the use of implicits, syntax styles), but once learnt it's quite amazing how a concise piece of code can carry so much information.
<br><br>
* __Scala code molds according to *YOUR* engineering culture__<br>Because Scala offers a high degree of flexibility, it requires significant effort for new developers to match or adapt to the existing team and culture. For example: some might prefer the 'better Java' approach, while others lean towards pure FP.

They are definitely known challenges, but something that can be overcome with active effort. So don't be discouraged! Learn Scala for all the good reason aforementioned.

*"But where do I start?"* you ask? Well below are some resources to get you started. There are others I can recommend; however, being a general purpose language, Scala materials out there covers everything from concurrent programming to recommendation systems. I hope to address a few different category separately in the future.

* [I just want to give it a quick spin&hellip;](#i-just-want-to-give-it-a-quick-spin)
* [How do run it on my machine?](#how-do-run-it-on-my-machine)
* [I want to learn more Scala](#i-want-to-learn-more-scala)
* [I need to level up in Scala!](#i-need-to-level-up-in-scala)

<br>

---

<br>

### "I just want to give it a quick spin&hellip;"

Skip a bunch of installation steps and just get right to coding!

1. Head over to [Scala Exercises](https://www.scala-exercises.org/) and try out the `STD LIB` exercises (ignore the others for now).
1. Play around with [Scastie](https://scastie.scala-lang.org/), a web-based interactive Scala editor.

*Note: Both website are free, but requires you to link your GitHub account info to unlock full functionalities*

<br>

---

<br>

### "How do run it on my machine?"

Well, it doesn't surprise me if you think Scala is awesome :) Depending on what you want to do next:

* Install Java SDK 1.8 (I recommend [Azul Zulu](http://www.azul.com/downloads/zulu/)), to run your application.
* For interactive console / REPL only:
   * Install [Scala](http://scala-lang.org/download/) binaries.
* To start writing Scala applications: 
   * Install [SBT](http://www.scala-sbt.org/), the de-facto build tool for Scala projects, and / or
   * Install a text editor or IDE with Scala support, I highly recommend [IntelliJ IDEA](https://www.jetbrains.com/idea/) for a no-fuss setup (community edition is free).

*Note: You can start writing Scala applications just by downloading Java SDK and IntelliJ IDEA. IDEA can take care various mundane tasks such as downloading SBT and Scala binaries as part of its workflow when creating new Scala projects.*

<br>

---

<br>

### "I want to learn more Scala"

That's great! I can point you to a few resources to help you improve your Scala knowledge:

* [Atomic Scala](http://atomicscala.com/) is a good '[soup-to-nuts](https://en.wikipedia.org/wiki/Soup_to_nuts)' introductory book on Scala.
* [Scala for the Impatient](http://www.horstmann.com/scala/index.html) is a comprehensive introduction to Scala with useful exercises.
* [Scala in Action](https://www.manning.com/books/scala-in-action) takes a practical approach in learning Scala.

<br>

---

<br>

### "I need to level up in Scala!"

Once you have an understanding of basic Scala concepts, now it's the time to explore Actors and the functional side of Scala:

* [Akka Concurrency](https://www.artima.com/shop/akka_concurrency) covers most of the core concepts in Akka actor model programming. *Note: Google updated examples as the ones in the book contains a few bugs and hasn't been updated.*
* [Functional Programing in Scala](https://www.manning.com/books/functional-programming-in-scala) is pretty much a reference book for developers exploring the pure-FP approach in Scala.
* [Functional Programming in Scala Specialization](https://www.coursera.org/specializations/scala) is a good course to explore FP concepts within Scala, delivered by Prof. Odersky himself.
* [Scala in Depth](https://www.manning.com/books/scala-in-depth) takes you further into more Scala features and eases you into advanced FP concepts.
