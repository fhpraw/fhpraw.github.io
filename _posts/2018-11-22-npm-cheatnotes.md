---
layout: post
title:  "NPM NVM Cheatnotes"
date:   2018-11-22 21:00:00 +0700
categories: npm cheatsheet
---
## NVM

show current node

```sh
nvm current
```

install the latest lts node
```sh
nvm install --lts
```

install particular node (ex: node v1.1.1)
```sh
nvm install 1.1.1
```

use particular node (ex: node v1.1.1)
```sh
nvm use 1.1.1
```

list installed version of node
```sh
nvm ls
```

uninstall particular node (ex: node v1.1.1)
```sh
nvm uninstall 1.1.1
```

## NPM

npm list top level modules

```sh
npm list -g --depth=0
```

installing global package

```sh
npm install -g package
```
