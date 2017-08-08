---
layout: post
title:  "Deploy Phoenix to AWS ElasticBeanstalk: Preface"
date:   2017-08-08 08:37:16 +0800
categories: posts
tags: aws devops distillery docker elasticbeanstalk elixir phoenix 
---
In these series of posts, I would like to cover a basic (Elixir) Phoenix Framework deployment to AWS ElasticBeanstalk. After researching and reading about various Phoenix deployment workflows / configurations, I found no complete example that I am happy with. So here's my own take, and I hope they'll prove to be useful.<!--more-->

<br>

### Table of Contents

* Preface
  * [Context](#context)
  * [Out of Scope](#out-of-scope)
  * [Prerequisites](#prerequisites)
* Setup Phoenix Framework and Distillery
* Configure Build and Packaging
* Deployment to AWS ElasticBeanstalk

<br>

### Context

For the past few years, I have been working almost exclusively with web frameworks in compiled languages (e.g. ASP.NET MVC in C#, ServiceStack in C#, Play Framework in Scala). One of the things I appreciate is the ability to create distribution packages: an __immutable__ collection of files and binaries, __ready-to-run__ on your (web) server.

It is important to me because it eliminates the startup overhead of code compiling, asset pipeline processing, and allows us to capture a snapshot of a complete and (tested) working application.

Much like how Scala, Kotlin, or Clojure code compiles down to Java bytecode to run on the Java Virtual Machine ('JVM'), Elixir code compiles down to Erlang bytecode to run on the Erlang Virtual Machine ('BEAM'). In addition, similar to how Java-based applications can embed the Java runtime ('JRE'), Elixir and Erlang applications can embed the Erlang runtime ('ERTS') which allows them to be run standalone.

<br>

__My goal is to share some knowledge on creating and deploying a standalone Phoenix application deployment package to AWS ElasticBeanstalk via Distillery and Docker.__

<br>

*Why AWS ElasticBeanstalk?*<br>There are other SaaS provider out there, but I prefer to work with AWS due to familiarity and its comprehensive offering (database, caching, queue, etc.). Whilst it's specific for AWS ElasticBeanstalk, the use of Docker allows for adaptation for deployment on other providers wherever it's supported (e.g. Digital Ocean, Linode, Hertzner, etc.)

<br>

*Why Distillery?*<br>It seems to be where the mindshare is at the moment. Simple to use, especially for beginners like me!

<br>

*Why Docker?*<br>It's a good container solution. Plus, most developers are familiar with Docker (or at least heard of it), so it will be easier to get up-to-speed and find additional learning resources. Vagrant (+ Virtualbox) is an alternative, however it's beyond the scope of this series of posts.

<br>

### Out of Scope

The following is only a basic example, covering only the basic Phoenix application structure, not an umbrella or multi-module ones. I'm still researching the following deployment topics, hopefully covering them in follow-up posts:

* Ecto / database schema migrations on application start,
* Erlang distribution and clustering, and
* hot swapping when upgrading cluster.

While this is a fully working example, for my own deployments I use [Codeship](https://codeship.com/) to test and deploy to AWS ElasticBeanstalk, check them out <img draggable="false" class="emoji" style="margin-top:-3px" alt="😁" src="https://twemoji.maxcdn.com/16x16/1f601.png">

<br>

### Prerequisites

To follow the 'setup, compile, and package' examples, ensure the following prerequisites are met:

* [Erlang / OTP](http://www.erlang.org/downloads) `18.x` or above
* [Elixir](https://elixir-lang.org/install.html) `1.4.x`
* [Phoenix Framework](https://hexdocs.pm/phoenix/installation.html) `1.3.x`
* [Node](https://nodejs.org/en/) `6.x` or above
* [Docker](https://www.docker.com/) ([Mac](https://www.docker.com/docker-mac) \| [Win](https://www.docker.com/docker-windows)) &mdash; *tested on `17.06.0-ce-mac-19`*

To follow the deployment examples, you'll need to have an AWS account and the AWS CLI installed and configured (or just take my word for it <img draggable="false" class="emoji" style="margin-top:-3px" alt="😜" src="https://twemoji.maxcdn.com/16x16/1f61c.png">)

<br>

*<center>continue to: Setup Phoenix Framework and Distillery</center>*
