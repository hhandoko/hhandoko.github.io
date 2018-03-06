###
# File     : Gemfile
# License  :
#   Copyright (c) 2017 Herdy Handoko
#
#   Licensed under the Apache License, Version 2.0 (the "License");
#   you may not use this file except in compliance with the License.
#   You may obtain a copy of the License at
#
#           http://www.apache.org/licenses/LICENSE-2.0
#
#   Unless required by applicable law or agreed to in writing, software
#   distributed under the License is distributed on an "AS IS" BASIS,
#   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#   See the License for the specific language governing permissions and
#   limitations under the License.
#
# Notes    :
#   - https://www.gitignore.io/api/windows,osx,linux,intellij,eclipse,netbeans,ensime,java,scala,sbt,playframework,vagrant
###
source "https://rubygems.org"
ruby RUBY_VERSION

# Jekyll
# ~~~~~~
# NOTE: If upgrading Jekyll version, run `bundle install` then `bundle exec`, e.g.
#       `bundle exec jekyll serve`.
#gem "jekyll", "3.7.3"

# GitHub Pages
# ~~~~~~
# NOTE: To use GitHub Pages, remove the "gem "jekyll"" above and uncomment the line
#       below. To upgrade, run `bundle update github-pages`.
gem "github-pages", group: :jekyll_plugins

# Jekyll theme
# ~~~~~~
gem "minima", "~> 2.0"

# Jekyll plugins
# ~~~~~~
group :jekyll_plugins do
   gem "jekyll-feed", "~> 0.6"
end

# Windows utils
# ~~~~~~
# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]
# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.0" if Gem.win_platform?
