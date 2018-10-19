---
layout: post
title:  "How To Install rbenv on Ubuntu in Simple Way"
date:   2018-10-19 21:41:00 +0700
categories: ruby tutorial
description: how to install rbenv for managing many versions of ruby
---

# What is rbenv

it is a simple ruby version manager that won't hurt your root system.

# Prerequisite before installing (building) ruby using rbenv

These are dependencies required for building ruby from source file. Install them:

```sh
sudo apt install autoconf bison build-essential libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libncurses5-dev libffi-dev libgdbm5 libgdbm-dev
```

# Install rbenv using rbenv-installer

There is another alternative for installing rbenv, which is using rbenv-installer

```sh
# with curl
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-installer | bash

# alternatively, with wget
wget -q https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-installer -O- | bash
```

Add this script into .zshrc or .bashrc:

```sh
  # rbenv config
  export PATH="$HOME/.rbenv/bin:$PATH"
  eval "$(rbenv init -)"
```

Close and open terminal again. To list available versions of ruby:

```sh
rbenv install --list | less
```

To make sure rbenv has been installed properly, use rbenv-doctor:

```sh
wget -q https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor -O- | bash
```

# Finally, you can install ruby (globally)

```sh
rbenv install <version of ruby>
rbenv global <version of installed ruby>
```

for example ruby v2.5.1, then

```sh
rbenv install 2.5.1
rbenv global 2.5.1
```

and, done. Congratulation, you officially has installed rbenv and ruby successfully !

Reference:

- [rbenv](https://github.com/rbenv/rbenv)
- [rbenv-installer](https://github.com/rbenv/rbenv-installer)
