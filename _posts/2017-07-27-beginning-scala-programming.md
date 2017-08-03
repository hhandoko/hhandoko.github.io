---
layout: post
title:  "Beginning Scala Programming"
date:   2017-07-27 10:45:58 +0800
categories: posts
tags: update
---
### "Why do you use Scala?"

&hellip;is a question that came up more and more often as people are gaining more awareness of the programming language. I normally spoke of my own personal experience, but for the most part, Scala is my go-to language because it offers me flexibility on how I can express my thoughts into code. '[Code is Prose](https://medium.com/@mb/code-is-prose-18461ee400e7)' is certainly very apt here. <!--more-->

<br>

### "But there are other, more elegant programming languages out there&hellip;"

[Scala is not perfect](http://www.lihaoyi.com/post/WartsoftheScalaProgrammingLanguage.html), but it is a pragmatic one. I am enjoying the flexibility and power it offers while being able to tap into the rich and diverse JVM ecosystem. By no means Scala should be the only programming language you use, but it does strike a nice balance between: usability, community size, and employment opportunity <img draggable="false" class="emoji" style="margin-top:-3px" alt="😜" src="https://twemoji.maxcdn.com/16x16/1f61c.png">

<br>

### "Java has lambdas!"

But Scala is much, much more than lambdas. Interesting things can happen when you have a language that combines __Object-Oriented__ (OO) with __Functional Programming__ (FP) approach, complemented with a __rich type system__. Pattern matching, Algrebraic Data Types (ADT), and monadic comprehensions are some *very useful* constructs that does not exists 'natively' in Java.

<br>

### "Why should I learn Scala?"

Well, for the reasons aforementioned! I'll be honest, I didn't seek out to learn it. What began as an exercise to keep a hobby project up-to-date (Play 1.2 to 2.x migration) have allowed me to learn FP concepts, actor model, reactive systems, and many others.

<br>

### "I heard Scala code is impossible to read!"

It depends, I think there are some contributing factors here:

* __Scala is highly contextual__<br>It will be challenging for Scala beginners to identify these contexts (e.g. the use of symbols, implicits, syntax styles), but once learnt it's quite amazing how a concise piece of code can carry so much information. I highly recommend going through Manabu Nakamura's slides on '[Readable Scala](http://gakuzzzz.github.io/slides/readable_scala/)' presented at [Scala Matsuri 2017](http://2017.scalamatsuri.org/index_en.html).
<br><br>
* __Scala code molds according to the engineering culture__<br>Because Scala is flexible, from [syntax styles](https://github.com/jsuereth/scala-arm/wiki/Basic-Usage), choice of libraries, to architecture, it's not uncommon for new developers putting in non-trivial effort to match and adapt to the existing team's culture. Regardless, have mentoring and / or pair programming in place.
<br><br>
* __Scala evolves relatively quickly__<br>Scala releases are highly iterative and changes faster compared to languages such as Java. Syntax styles, design patterns, and libraries that was considered best practices three years ago might already be outdated now. Developers (new and experienced alike) need to pay special attention when using Scala code found in blog posts and StackOverflow responses. Check the publish date <img draggable="false" class="emoji" style="margin-top:-8px" alt="👌" src="https://twemoji.maxcdn.com/16x16/1f44c.png">

<br>

### "But where do I start?"

&hellip;you ask? Being a general purpose language, Scala materials out there can cover anything from concurrent programming to recommendation systems. I hope to address various different categories separately in the future, but here are some good resources to get you on your journey:

* [I just want to give it a quick spin&hellip;](#i-just-want-to-give-it-a-quick-spin)
* [How to run it on my machine?](#how-to-run-it-on-my-machine)
* [I am a Java developer](#i-am-a-java-developer)
* [I want to learn more Scala](#i-want-to-learn-more-scala)
* [I need to level up in Scala!](#i-need-to-level-up-in-scala)
* [Where can I find other Scala developers?](#where-can-i-find-other-scala-developers)

Last but not least, check out [Awesome Scala](https://github.com/lauris/awesome-scala) for a community-curated list of awesome Scala libraries.

<br>

---

<br>

#### "I just want to give it a quick spin&hellip;"

Skip a bunch of installation steps and just get right to coding! Both websites are free, but requires you to link your GitHub account to unlock the entire functionalities.

1. Head over to [Scala Exercises](https://www.scala-exercises.org/) and try out the `STD LIB` exercises (ignore the others for now).
1. Play around with [Scastie](https://scastie.scala-lang.org/), a web-based interactive Scala editor.

<br>

#### "How to run it on my machine?"

Well, it doesn't surprise me if you think Scala is awesome <img draggable="false" class="emoji" style="margin-top:-5px" alt="😁" src="https://twemoji.maxcdn.com/16x16/1f601.png"> Depending on what you want to do next:

* Install Java SDK 1.8 (I recommend [Azul Zulu](http://www.azul.com/downloads/zulu/)), to run your application.
* For interactive console / REPL only:
   * Install [Scala](http://scala-lang.org/download/) binaries.
* To start writing Scala applications: 
   * Install [SBT](http://www.scala-sbt.org/), the de-facto build tool for Scala projects, and / or
   * Install a text editor or IDE with Scala support, I highly recommend [IntelliJ IDEA](https://www.jetbrains.com/idea/) for a no-fuss setup (community edition is free).

*Note: You can start writing Scala applications just by downloading Java SDK and IntelliJ IDEA. IDEA can take care various mundane tasks such as downloading SBT and Scala binaries as part of its workflow when creating new Scala projects.*

<br>

#### "I am a Java developer"

I'm glad to hear that, it means you are already familiar with the Java ecosystem and should have a head-start in Scala programming. However, besides learning the language, I would also recommend you to spend a bit of time to learn SBT (Scala Build Tool). While you can use Maven or Gradle for Scala projects, SBT will be a far more pleasant experience:

* [SBT: The Missing Tutorial](https://github.com/shekhargulati/52-technologies-in-2016/blob/master/02-sbt/README.md) gives a quick rundown of SBT basics.
* [SBT in Action](https://www.manning.com/books/sbt-in-action) covers SBT in depth, from extending your project workflow to creating plugins.
* [Awesome SBT Plugins](https://github.com/meloniasty/awesome-sbt-plugins) lists various plugins to enhance your SBT capabilities. Also check out [the list of SBT plugins I'm using](http://www.hhandoko.com/notes.html#sbt-plugins).

<br>

#### "I want to learn more Scala"

That's great! I can point you to a few resources to help you improve your Scala knowledge:

* [Atomic Scala](http://atomicscala.com/) is a good '[soup-to-nuts](https://en.wikipedia.org/wiki/Soup_to_nuts)' introductory book on Scala.
* [Scala for the Impatient](http://www.horstmann.com/scala/index.html) is a comprehensive introduction to Scala with useful exercises.
* [Scala in Action](https://www.manning.com/books/scala-in-action) takes a practical approach in learning Scala.

<br>

#### "I need to level up in Scala!"

Once you have an understanding of basic Scala concepts, now it's the time to explore Actors and the functional side of Scala:

* [Akka Concurrency](https://www.artima.com/shop/akka_concurrency) covers most of the core concepts in Akka actor model programming.<br>*Note: Google for updated examples as the ones in the book contains a few bugs and hasn't been updated.*
* [Functional Programing in Scala](https://www.manning.com/books/functional-programming-in-scala) (a.k.a. the Red Book) is pretty much a reference for developers exploring the pure-FP approach in Scala.
* [Functional Programming in Scala Specialization](https://www.coursera.org/specializations/scala) is a good course to explore FP concepts within Scala, delivered by Prof. Odersky himself.
* [Introduction to programming with dependent types in Scala](https://stepik.org/course/ThCS-Introduction-to-programming-with-dependent-types-in-Scala-2294/) is an FP course which covers type-level programming in Scala, suitable for developers already familiar with type systems and experience in FP concepts.
* [Scala in Depth](https://www.manning.com/books/scala-in-depth) takes you further into more Scala features and eases you into advanced FP concepts.

<br>

#### "Where can I find other Scala developers?"

Learning is much better together! 

* [Scala on Gitter](https://gitter.im/scala/scala) is the official Scala channel on Gitter messaging platform.
* [#scala on IRC](irc://irc.freenode.net/#scala) for various Scala-related chat on IRC.
* [Scala Space](http://scala.space/) shows various Scala-related groups near you, such as Meetup groups.

<br>

---

<br>

<u>Referenced blogs, docs, and presentations (A-Z):</u>

* *'Code is Prose'* by __Matthew Bischoff__<br>[https://medium.com/@mb/code-is-prose-18461ee400e7](https://medium.com/@mb/code-is-prose-18461ee400e7)
<br><br>
* *'Readable Scala'* by __Manabu Nakamura__<br>[http://gakuzzzz.github.io/slides/readable_scala/](http://gakuzzzz.github.io/slides/readable_scala/)
<br><br>
* *'Scala ARM (Automatic Resource Management) Basic Usage'* Wiki page by __Josh Suereth__<br>[https://github.com/jsuereth/scala-arm/wiki/Basic-Usage](https://github.com/jsuereth/scala-arm/wiki/Basic-Usage)
<br><br>
* *'Warts of the Scala Programming Language'* by __Li Haoyi__<br>[http://www.lihaoyi.com/post/WartsoftheScalaProgrammingLanguage.html](http://www.lihaoyi.com/post/WartsoftheScalaProgrammingLanguage.html)

<br>

---

<br>

<u>Updates:</u>

__[2017-08-03]__ &mdash; Added community resources and Scala for Java developers based on feedback