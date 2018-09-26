---
layout: post
title: "Run Simple Web Server for Testing"
date: 2018-09-26 10:47:00 +0700
categories: productivity tutorial
description: simple web server for testing only
---

If you want to testing your web project, simply use http-server.
Install it with npm on global

```sh
npm install -g http-server
```

After installing, `cd` into your project then run

```sh
http-server
```

your server probably can be accessed on http://127.0.0.1:8080

or

with built-in web server on python 3, `cd` into your project then run

```sh
python3 -m http.server 8000
```

or in python 2

```sh
python -m SimpleHTTPServer 8000
```

your server can be accessed on http://127.0.0.1:8000
