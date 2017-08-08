---
layout: post
title: "Deploy Phoenix to AWS ElasticBeanstalk: Setup Phoenix and Distillery"
date: 2017-08-08 13:24:33 +0800
categories: posts
tags: aws devops distillery docker elasticbeanstalk elixir phoenix 
---
In this second post of the series, I will focus on setting up a new (Elixir) Phoenix project and briefly cover some high-level concepts relevant to the goal.<!--more-->

<br>

### Table of Contents

* Preface
* Setup Phoenix Framework and Distillery
  * [Create a New Phoenix Project](#create-new-phoenix-project)
  * [Phoenix Folder Structure 101](#phoenix-folder-structure-101)
  * [Configure Distillery](#configure-distillery)
* Configure Build and Packaging
* Deployment to AWS ElasticBeanstalk

<br>

### Create New Phoenix Project

Assuming that all prerequisites have been met, let's create a new Phoenix project by running the following `mix` command:

```shell
$ mix phx.new phoenix_on_awseb --no-ecto
```

Let's break it down:

* `mix` is the build tool executable name that ships with Elixir
* `phx.new` is the archive name to scaffold a new Phoenix project
* `phoenix_on_awseb` will be our application name
* `--no-ecto` is a flag to opt-out from Ecto setup (i.e. no database)

*NOTE: I exclude Ecto specifically to make the example simpler and focused. I'll cover Ecto migrations in a follow up post.*

<br>

### Phoenix Folder Structure 101

Let's examine the standard application structure in our new Phoenix application, and discuss a few key directories and their significance: 

```shell
├── README.md
├── _build/
├── assets/
│   ├── brunch-config.js
│   ├── css/
│   ├── js/
│   ├── node_modules/
│   ├── package-lock.json
│   ├── package.json
│   ├── static/
│   └── vendor/
├── config/
│   ├── config.exs
│   ├── dev.exs
│   ├── prod.exs
│   ├── prod.secret.exs
│   └── test.exs
├── deps/
├── lib/
├── priv/
├── mix.exs
├── mix.lock
└── test/
```

<br>

#### deps/

The `deps` folder contains all of our Phoenix project dependencies (and their dependencies) as listed in `mix.exs`:

```elixir
  ...
  # Specifies your project dependencies.
  #
  # Type `mix help deps` for examples and options.
  defp deps do
    [
      {:phoenix, "~> 1.3.0"},
      {:phoenix_pubsub, "~> 1.0"},
      {:phoenix_html, "~> 2.10"},
      {:phoenix_live_reload, "~> 1.0", only: :dev},
      {:gettext, "~> 0.11"},
      {:cowboy, "~> 1.0"}
    ]
  end
  ...
```

Upon running `mix deps.get`, Mix will download the `tar` packages from the Hex repo. However, not until `mix compile` is first invoked that both Erlang and Elixir-based dependencies are compiled into Erlang bytecode, i.e. `*.beam` files.

<br>

#### config/

The `config` folder contains different environment context, or runtime configuration, that our Phoenix application can use, such as: `dev.exs` for development, `prod.exs` for production, and `test.exs` for test.

There are a couple of observable default behaviours:

1. Running tests (e.g. `mix test`) will implicitly use the `test` context
1. Running other Mix commands will implicitly use the `dev` context

Other contexts, such as `prod` is only effective if called explicitly by setting / passing the `MIX_ENV` environment variable. For example:

```shell
$ MIX_ENV=prod mix compile
```

Please take a note of the `MIX_ENV` environment variable usage, as it's an important feature for our production 'compile and package' workflow.

Please read the [Phoenix Configuration](https://hexdocs.pm/phoenix/config.html) documentation section for more info.

<br>

#### _build/

The `_build` folder is ___the___ directory where all compiled code are emitted, and its direct child folder corresponds against the environment context used. Taking the default environment context: `dev`, `test`, and `prod`, we might have the following folder structure.

```shell
├── _build
│   ├── dev
│   ├── prod
│   └── test
...
```

One important thing to note here, is that under the `dev` and `test` environment contexts, the `/_build/dev/lib` contains dependency subfolders that are symlinked to `/deps`, e.g. `/build/dev/lib/cowboy/ebin`. While it's fine for development, it's less than ideal for production.

<br>

#### assets/

The `assets` folder contains all front-end assets which forms part of the Brunch workflow. It can be considered the root project directory for all front-end work, indicated by the existence of `package.json` and `brunch-config.js` files, and of course the `node_modules` folder.

A few things to note here, in relation to Phoenix and Brunch:

* Configuration in `brunch-config.js` emits the compiled / transpiled and processed front-end assets to the `/priv/static` folder (refer to `paths.public` setting)
* Running `mix phx.server` in `dev` will trigger the `brunch watch --stdin` command and enables live reload, but these settings are absent from `prod.ex` and `test.ex`
* `package.json` has script aliases for `brunch watch` and `brunch deploy`, but they aren't linked to Mix tasks, simply for convenience running Brunch command from npm (e.g. `npm run deploy`)

One thing I noticed which might not be readily apparent, is that Mix and Brunch workflows aren't as integrated as I has initially thought. Some use cases that could lead to erroneous deployments:

* Compiling in development mode for production packaging (leads to bloat)
* Forgetting to compile front-end assets before publishing (leads to `404`s)
* Forgetting to clean old, digested assets (leads to bloat)
* etc.

The problems above can be alleviated of course. As before, just keep them in mind for now as I will address them in the next section on streamlining the deployment workflow.

<br>

### Configure Distillery

*TBA*

<br>

*<center>continue to: Setup Phoenix Framework and Distillery</center>*
