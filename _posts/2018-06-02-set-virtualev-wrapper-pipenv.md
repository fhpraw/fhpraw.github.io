---
layout: post
title:  "Setting Up Virtual Environment for Python Project"
date:   2018-06-02 00:45:00 +0700
categories: python tutorial
description: python quick tutorial, virtualenv, virtualenvwrapper, pipenv
---

Make sure you have _pip_ for _python 3_ is installed, if not, install it first:

``` sh
sudo apt install python3-pip
```

then install _virtualenv_, _virtualenvwrapper_, _pipenv_:

``` sh
pip install --user virtualenv virtualenvwrapper pipenv
```

after installing them, append some lines below into `.zshrc`:

``` sh

# prevent installing pip packages on global scope
export PIP_REQUIRE_VIRTUALENV=true

# function (command) for installing pip packages on global scope python3
# for example
#   gpip install <name of package>
gpip() {
  PIP_REQUIRE_VIRTUALENV="" pip3 "$@"
}

# virtualenvwrapper for python 3 path
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3

# virtualenvwrapper for virtualenv (for python 3) path
export VIRTUALENVWRAPPER_VIRTUALENV=~/.local/bin/virtualenv

# virtualenv site
export WORKON_HOME=~/.virtualenvs

# python project home
export PROJECT_HOME=~/Projects

# virtualenvwrapper script
source ~/.local/bin/virtualenvwrapper.sh
```

> I prefer to use _zsh_, so `.zshrc` is edited. Make sure those configurations script append at the top of `.zshrc` , I mean before oh-my-zsh configurations (if available).
> If you still use _bash_, then edit `.bashrc`.
> You see `PROJECT_HOME` is set to `~/Projects`, this is my personal preference. You can change your project directory wherever you like.

Finally, you can create _virtual environment_, simply with:

```sh
mkproject MyProject
```

This command line automagically will install new _virtual environment_ on `~/Projects/MyProject` then activate it. To quit, type:

``` sh
deactivate
```

If you want come back, type:

``` sh
workon MyProject
```

To list your projects those have been created:

``` sh
lsvirtualenv
```

To delete your project:

``` sh
rmvirtualenv MyProject
```

Or another way to manage your project dependencies in easy way, then create the project using _pipenv_:

``` sh
mkdir MyProject2
pipenv install <packages>
```

It will create _virtual environment_ for your project and _pipfile_. _Pipfile_ is a text file contains list of pip package names which is used by your current project. This pipfile is useful when you want to deploy your project to another machine. You don't have to remember what packages are needed, pipfile help remember it for you.
> Further explanation about pipenv  and pipfile will come soon. Actually, I still learn how to use it, to get the most advantages of its features.

Reference:

- [Pipenv & Virtual Environments](http://docs.python-guide.org/en/latest/dev/virtualenvs/)