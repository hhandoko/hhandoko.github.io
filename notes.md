---
layout: page
title: Notes
permalink: /notes.html
---

A collection of useful notes on development environment configurations and other findings.

* [SBT Plugins](#sbt-plugins)

<br>

---

<br>

### SBT Plugins

The following is a list of useful global SBT plugins I'm using in my Scala / SBT projects:

* [sbt-coursier](https://github.com/coursier/coursier) - An improved Scala artifact fetcher, with parallel downloads and better offline mode.
* [sbt-dependency-graph](https://github.com/jrudolph/sbt-dependency-graph) - Add support to visualize dependency graph within SBT (supports both ASCII and HTML output).
* [sbt-dependency-updates](https://github.com/rtimush/sbt-updates) - Add support to fetch and display available dependency updates in current project.
* [sbt-ensime](http://ensime.org/build_tools/sbt/) - Adds an SBT command to generates `.ensime` file in SBT projects for use by [ENSIME](http://ensime.org/) (e.g. in Atom, emacs, or VS Code).
* [scala-clippy](https://github.com/softwaremill/scala-clippy) - Improved compiler error messages and syntax colorizer.
