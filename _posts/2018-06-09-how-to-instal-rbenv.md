---
layout: post
title:  "How To Install rbenv"
date:   2018-06-09 20:41:00 +0700
categories: ruby tutorial
description: how to install rbenv for managing many versions of ruby
---

## What is rbenv

it is a simple ruby version manager that won't hurt your root system.

## Install rbenv

1. Clone rbenv into `~/.rbenv`

```sh
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
```

2. Add `~/.rbenv/bin` to your `$PATH` for access to the `rbenv` command-line utility

    - for zsh:
        ```sh
        echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc
        ```
3. Set up rbenv in your shell
```sh
~/.rbenv/bin/rbenv init
```

Close your terminal emulator then open again.

## Install ruby-build

Install ruby-build as an rbenv plugin

```sh
mkdir -p "$(rbenv root)"/plugins
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
```

## Reference
[rbenv](https://github.com/rbenv/rbenv)

