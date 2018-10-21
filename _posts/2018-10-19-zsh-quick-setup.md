---
layout: post
title: "ZSH Quick Setup on Ubuntu"
date: 2018-10-19 23:07:00 +0700
categories: zsh tutorial
description: zsh, oh-my-zsh, zplug, how to install
---

First Install _zsh_:

``` sh
sudo apt install zsh
```

and then, install _oh-my-zsh_, the zsh framework:

``` sh
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

then, install zplug, the plugin manager for zsh:
```sh
curl -sL --proto-redir -all,https https://raw.githubusercontent.com/zplug/installer/master/installer.zsh | zsh
```

Finally, edit `.zshrc` to install or load some plugin for your _zsh_. With oh-my-zsh installed, you already have hundreds plugins installed. But they must be activated or loaded by _zplug_. Append these lines into `.zshrc`:
> Actually this is my personal config, most of plugins already available inside `~/.oh-my-zsh/plugins/`, it won't need internet connection. Choose plugins which only what you need

``` sh
# zplug config

source ~/.zplug/init.zsh

# external Plugins
zplug "zsh-users/zsh-syntax-highlighting"
zplug "zsh-users/zsh-history-substring-search"
zplug "zsh-users/zsh-autosuggestions"
zplug "zsh-users/zsh-completions"
zplug "lukechilds/zsh-nvm"

# oh-my-zsh plugins
zplug "plugins/colored-man-pages", from:oh-my-zsh
zplug "plugins/colorize", from:oh-my-zsh
zplug "plugins/command-not-found", from:oh-my-zsh
zplug "plugins/cp", from:oh-my-zsh
zplug "plugins/gem", from:oh-my-zsh
zplug "plugins/git", from:oh-my-zsh
zplug "plugins/github", from:oh-my-zsh
zplug "plugins/gitignore", from:oh-my-zsh
zplug "plugins/git-prompt", from:oh-my-zsh
zplug "plugins/man", from:oh-my-zsh
zplug "plugins/npm", from:oh-my-zsh
zplug "plugins/nvm", from:oh-my-zsh
zplug "plugins/pip", from:oh-my-zsh
zplug "plugins/rbenv", from:oh-my-zsh
zplug "plugins/ruby", from:oh-my-zsh
zplug "plugins/sudo", from:oh-my-zsh
zplug "plugins/tmux", from:oh-my-zsh
zplug "plugins/ubuntu", from:oh-my-zsh

# Install plugins if there are plugins that have not been installed
if ! zplug check --verbose; then
    printf "Install? [y/N]: "
    if read -q; then
        echo; zplug install
    fi
fi

# Then, source plugins and add commands to $PATH
zplug load
```

Lastly, save and restart your _terminal_
> Quit terminal session and open it again, if you want to add plugin outside oh-my-zsh plugins, then internet connection is needed for installation process.
