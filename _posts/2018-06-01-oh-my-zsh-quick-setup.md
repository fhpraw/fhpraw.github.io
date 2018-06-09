---
layout: post
title: "oh-my-zsh Quick setup"
date: 2018-06-01 23:07:00 +0700
categories: zsh tutorial
description: zsh, setup oh-my-zsh, how to install and configure oh-my-zsh
---

First Install _zsh_ (on Ubuntu):

``` sh
sudo apt install zsh
```

and then, install _oh-my-zsh_:

``` sh
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

What is [oh-my-zsh](http://ohmyz.sh) ? It is a zsh customizer framework, you can add plugins or themes, or whatever you can.

and then, install _antigen_ (make sure curl is available):

``` sh
curl -L git.io/antigen > ~/.antigen.zsh
```

What is [antigen](http://antigen.sharats.me) ? It is plugin manager for zsh. You can install any plugin you want in easiest way.

Finally, edit `.zshrc` to install or load some plugin for your _zsh_. With oh-my-zsh installed, you already have hundreds plugins installed. But they must be activated or loaded by _antigen_. Append these lines into `.zshrc`:
> Actually this is my personal custom, most of plugins already available inside `~/.oh-my-zsh/plugins/`, it won't need internet connection. Choose plugins which only what you need

``` sh
source ~/.antigen.zsh

# Load Antigen
source ~/.antigen.zsh

# Load the oh-my-zsh's library
antigen use oh-my-zsh

# Load the theme
antigen theme robbyrussell

# Load oh-my-zsh's plugins below
# ------------------------------
# Productivity
antigen bundle colored-man-pages
antigen bundle colorize
antigen bundle command-not-found
antigen bundle cp
antigen bundle man
antigen bundle tmux
antigen bundle ubuntu
antigen bundle vundle

# Build tools
antigen bundle git


# Ruby plugins
antigen bundle bundler
antigen bundle gem
antigen bundle ruby

# Python plugins
antigen bundle pip
antigen bundle pylint
antigen bundle python
antigen bundle virtualenv
antigen bundle virtualenvwrapper

# Node plugins
antigen bundle node
antigen bundle npm
antigen bundle nvm
antigen bundle lukechilds/zsh-nvm

# Load other plugins
# ------------------------------
antigen bundle zsh-users/zsh-syntax-highlighting
antigen bundle zsh-users/zsh-autosuggestions
antigen bundle zsh-users/zsh-completions

# Tell antigen that you're done
antigen apply
```

Lastly, save and restart your _terminal_
> Quit terminal session and open it again, if you want to add plugin outside oh-my-zsh plugins, then internet connection is needed for installation process.
