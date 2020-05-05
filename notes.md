---
layout: page
title: Notes
permalink: /notes.html
---

A collection of useful notes on development environment configurations and other findings.

* [Ubuntu Desktop Setup Tips](#ubuntu-desktop-setup-tips)
* [Gradle Plugins](#gradle-plugins)
* [SBT Plugins](#sbt-plugins)

<br>

---

<br>

### Ubuntu Desktop Setup Tips

The following is a collection of resources (e.g. packages, PPAs, themes) I'm using in my Ubuntu desktop:

#### General

* [Apple Keyboard Fn switch](https://superuser.com/a/223471) - Switch `Fn` key function in Ubuntu for use with Mac keyboards (`echo 2 | sudo tee /sys/module/hid_apple/parameters/fnmode`).
* [emoji-keyboard](https://github.com/OzymandiasTheGreat/emoji-keyboard) - Emoji support via virtual keyboard.
* [rtl8192cu-fixes](https://github.com/pvaret/rtl8192cu-fixes) - Repackaged Realtek 8192CU USB WiFi driver.
* [Intel Graphics screen tear fix](https://askubuntu.com/a/1119262) - Fixes Screen tearing issue with Intel Integrated Graphics.

#### Developer Tools

* [asdf](https://github.com/asdf-vm/asdf) - Extendable version control manager for Erlang, Elixir, Elm, etc.
* [bat](https://github.com/sharkdp/bat) - Better `cat`.
* [fd](https://github.com/sharkdp/fd) - Better `find`.
* [Fira Code](https://github.com/tonsky/FiraCode) - Monospaced font for coding with ligature support.
* [nvm](https://github.com/nvm-sh/nvm) - Install and manage multiple versions of Nodejs.
* [Ruby package](https://www.brightbox.com/docs/ruby/ubuntu/) - Use 3<sup>rd</sup> party Ruby repository to get the latest version, including dev packages and version switch utility.
* [SDKMAN](https://sdkman.io/) - Install and manage multiple versions of Java SDKs and build tools.

#### Productivity Tools

* [Joplin](https://joplinapp.org/) - Note-taking tool with sync capabilities.
* [Remmina](https://remmina.org/) - RDP client for Linux.

#### OS Tools

* [f.lux](https://justgetflux.com/) - Adapt computer monitor glow by time of day.
* [indicator-multiload](http://thaeial.blogspot.sg/p/indicator-multiload-faq.html) - Show system resource usages (e.g. CPU, memory, network) in toolbar.
* [psensor](http://wpitchoune.net/psensor/) - Show system temperature in toolbar.
* [Stacer](https://github.com/oguzhaninan/Stacer) - Linux system optimiser and monitoring.
* [tilix](https://gnunn1.github.io/tilix-web/) - Tiling terminal emulator.

#### Shell Customisation

* [Bashstrap](https://github.com/barryclark/bashstrap) - Theme and aliases for OSX bash.
* [Oh My Zsh](https://ohmyz.sh/) - Zsh terminal customisations.
* [Powerline for Agnoster](https://blog.zhaytam.com/2019/04/19/powerline-and-zshs-agnoster-theme-in-vs-code/) - Fix Powerline fonts for ZSH Agnoster theme.

#### Theming (20.04)

* [Gnome Shell Extension](http://ubuntuhandbook.org/index.php/2017/05/enable-shell-theme-in-gnome-tweak-tool-in-ubuntu/) - Enable Gnome user-shell extension for Gnome Tweak tool.
* [Starship.rs](https://starship.rs/) - Cross-shell shell customisations.
* [Sushi](https://github.com/GNOME/sushi) - Smart file previews.
* [Yaru Dark VLC](https://gitlab.com/NovaQC/vlc-yaru-dark/) - Ubuntu's Yaru Dark VLC theme.
* Change dock 'on click' behaviour:
  * View options: `gsettings range org.gnome.shell.extensions.dash-to-dock click-action`
  * Set value (e.g. preview): `gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'previews'`
* Remove mounted drives on dock `gsettings set org.gnome.shell.extensions.dash-to-dock show-mounts false`

#### Theming (18.04)

* [Adapta](https://github.com/adapta-project/adapta-gtk-theme) - Google Material design theme.
* [Flatpak](https://flatpak.org/setup/Ubuntu/) - Cross-distro Linux application distribution platform.
* [Gnome Shell Extension](http://ubuntuhandbook.org/index.php/2017/05/enable-shell-theme-in-gnome-tweak-tool-in-ubuntu/) - Enable Gnome user-shell extension for Gnome Tweak tool.
* [Papirus - Icons](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme) - Flat icons with Adapta theme.
* Change dock 'on click' behaviour:
  * View options: `gsettings range org.gnome.shell.extensions.dash-to-dock click-action`
  * Set value (e.g. preview): `gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'previews'`

#### Theming (16.04)

* [Arc Theme - Firefox](https://github.com/horst3180/arc-firefox-theme) - Arc theme extension for Firefox.
* [Arc Theme - GTK](https://github.com/horst3180/arc-theme) - Flat theme with transparent element for GTK (incl. Unity).
* [Arc Theme - Thunderbird](https://github.com/JD342/arc-thunderbird-integration) - Arc theme extension for Thunderbird.
* [Flatabulous - Icons](https://github.com/anmoljagetia/Flatabulous#flat-icons) - Flat icons collection.
* [Unity Dash Icon update](http://askubuntu.com/a/654404) - Update Unity dash with a custom icon.
* [Unity Tweak](https://apps.ubuntu.com/cat/applications/unity-tweak-tool/) - Easily change themes and fonts in Unity.

#### Other

* [Random string generation](https://unix.stackexchange.com/a/230676) - Generate random string in bash (`</dev/urandom tr -dc 'A-Za-z0-9!"#$%&'\''()*+,-./:;<=>?@[\]^_{|}~' | head -c 64; echo`)
* [Restore grub](https://itsfoss.com/no-grub-windows-linux/) - Restore grub after Windows 10 update (`bcdedit /set {bootmgr} path \EFI\ubuntu\grubx64.efi` in command shell).

<br>

---

<br>

### Gradle Plugins

The following is a list of useful Gradle plugins I'm using in my Java / Kotlin / Scala projects:

* [gradle-test-logger](https://github.com/radarsh/gradle-test-logger-plugin) - Test output formatting with themes and parallel execution support.
* [gradle-scoverage](https://github.com/scoverage/gradle-scoverage) - Enable Scoverage in Scala project
* [gradle-stats](https://github.com/aalmiray/stats-gradle-plugin) - Provides source code statistics in individual or aggregate project.
* [spotless](https://github.com/diffplug/spotless) - Source code formatter support; supports Java, Scala, Kotlin, SQL, etc.

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
