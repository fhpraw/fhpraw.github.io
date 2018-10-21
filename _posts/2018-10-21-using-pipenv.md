---
layout: post
title:  "Using pipenv"
date:   2018-10-21 11:00:00 +0700
categories: tutorial python
---

First of all, install python3 and pip3

```sh
sudo apt install python3 python3-pip
```

Then, install pipenv (user installation)

```sh
pip3 install --user pipenv
```

Installing packages for you project, for example PyPDF2 then

```sh
cd your_project_folder
pipenv install PyPDF2
```

This will automatically make a virtualenv and install PyPDF2. how to run?

```sh
pipenv run python yourscript.py
```

To activate virtualenv (not necessary),

```sh
cd your_project_folder
pipenv shell
```

To deactivate,
```sh
deactivate
```
