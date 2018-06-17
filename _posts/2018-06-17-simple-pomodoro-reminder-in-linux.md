---
layout: post
title: "Simple Pomodoro Reminder in Linux"
date: 2018-06-17 11:33:00 +0700
categories: productivity tutorial
description: simple pomodoro reminder in linux
---

Recomended pomodoro time is 25 minutes or 25x60s equals to 1500s. Then type this in shell:

```sh
sleep 1500 && notify-send "Time Up!"
```

it will send a notification. After 25 minutes, notification bubble show up and tell you a message "Time Up!".
