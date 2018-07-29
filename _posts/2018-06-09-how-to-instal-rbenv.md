---
layout: post
title:  "How To Install rbenv on Ubuntu"
date:   2018-07-28 17:41:00 +0700
categories: ruby tutorial
description: how to install rbenv for managing many versions of ruby
---

# What is rbenv

it is a simple ruby version manager that won't hurt your root system.

# Install rbenv

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

4. Set up rbenv hooks into your shell
    1. Sets up your shims path, add `~/.rbenv/shims` to your `PATH`

         ```sh
         export PATH="$HOME/.rbenv/bin:$HOME/.rbenv/shims:$PATH"
         ```

    2. Install autocompletion (for zsh)

         ```sh
         ~/.rbenv/completions/rbenv.zsh
         ```

    3. Rehashes shims

        ```sh
        rbenv rehash
        ```

    4. Run

         ```sh
         rbenv init -
         ```

Close your terminal emulator then open again.

# Prerequisite before installing (building) ruby using rbenv

I actually use ubuntu, so install these

```sh
sudo apt install autoconf bison build-essential libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libncurses5-dev libffi-dev libgdbm5 libgdbm-dev
```

these are dependencies required for building ruby from source file.

# Install ruby-build

Install ruby-build as an rbenv plugin

```sh
mkdir -p "$(rbenv root)"/plugins
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
```

# Finally, you can install ruby

```sh
rbenv install <version of ruby>
```

for example

```sh
rbenv install 2.5.1
```

to list available versions of ruby:

```sh
rbenv install --list | less
```

Reference:

- [rbenv](https://github.com/rbenv/rbenv)
