---
layout: page
title: Notes
permalink: /notes.html
---

A collection of useful notes on development environment configurations and other findings.

* [Ubuntu Desktop Setup Tips](#ubuntu-desktop-setup-tips)
* [SBT Plugins](#sbt-plugins)

<br>

---

<br>

### Ubuntu Desktop Setup Tips

The following is a collection of resources (e.g. packages, PPAs, themes) I'm using in my Ubuntu desktop:

#### General

* [Apple Keyboard Fn switch](https://superuser.com/a/223471) - Switch `Fn` key function in Ubuntu (`echo 2 | sudo tee /sys/module/hid_apple/parameters/fnmode`).
* [emoji-keyboard](https://github.com/OzymandiasTheGreat/emoji-keyboard) - Emoji support via virtual keyboard.
* [rtl8192cu-fixes](https://github.com/pvaret/rtl8192cu-fixes) - Repackaged Realtek 8192CU USB WiFi driver.

#### Developer Tools

* [Fira Code](https://github.com/tonsky/FiraCode) - Monospaced font for coding with ligature support.
* [Ruby package](https://www.brightbox.com/docs/ruby/ubuntu/) - Use 3<sup>rd</sup> party Ruby repository to get the latest version, including dev packages and version switch utility.
* [Visual Studio Code package](https://code.visualstudio.com/docs/setup/linux) - Install VSCode via PPA, rather `deb` package for ease-of-update.

#### OS Tools

* [f.lux](https://justgetflux.com/) - Adapt computer monitor glow by time of day.
* [indicator-multiload](http://thaeial.blogspot.sg/p/indicator-multiload-faq.html) - Show system resource usages (e.g. CPU, memory, network) in toolbar.
* [psensor](http://wpitchoune.net/psensor/) - Show system temperature in toolbar.
* [Stacer](https://github.com/oguzhaninan/Stacer) - Linux system optimiser and monitoring.

#### Theming

* [Arc Theme - Firefox](https://github.com/horst3180/arc-firefox-theme) - Arc theme extension for Firefox.
* [Arc Theme - GTK](https://github.com/horst3180/arc-theme) - Flat theme with transparent element for GTK (incl. Unity).
* [Arc Theme - Thunderbird](https://github.com/JD342/arc-thunderbird-integration) - Arc theme extension for Thunderbird.
* [Flatabulous - Icons](https://github.com/anmoljagetia/Flatabulous#flat-icons) - Flat icons collection.
* [Unity Dash Icon update](http://askubuntu.com/a/654404) - Update Unity dash with a custom icon.
* [Unity Tweak](https://apps.ubuntu.com/cat/applications/unity-tweak-tool/) - Easily change themes and fonts in Unity.

#### Other

* [Restore grub](https://itsfoss.com/no-grub-windows-linux/) - Restore grub after Windows 10 update (`bcdedit /set {bootmgr} path \EFI\ubuntu\grubx64.efi` in command shell).

<br>

---

<br>

### SBT Plugins

The following is a list of useful global SBT plugins I'm using in my Scala / SBT projects:

* [sbt-coursier](https://github.com/coursier/coursier) - An improved Scala artifact fetcher, with parallel downloads and better offline mode.
* [sbt-dependency-graph](https://github.com/jrudolph/sbt-dependency-graph) - Add support to visualize dependency graph within SBT (supports both ASCII and HTML output).
* [sbt-dependency-updates](https://github.com/rtimush/sbt-updates) - Add support to fetch and display available dependency updates in current project.
* [sbt-ensime](http://ensime.org/build_tools/sbt/) - Adds an SBT command to generates `.ensime` file in SBT projects for use by [ENSIME](http://ensime.org/) (e.g. in Atom, emacs, or VS Code).
* [sbt-stats](https://github.com/orrsella/sbt-stats) - Provides source code statistics in individual or aggregate project.
* [scala-clippy](https://github.com/softwaremill/scala-clippy) - Improved compiler error messages and syntax colorizer.
