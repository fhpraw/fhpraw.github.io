---
layout: post
title:  "youtube-dl Quick Tutorial"
date:   2018-05-21 19:41:00 +0700
categories: python tutorial
description: youtube-dl quick tutorial, download all videos on youtube channel, download bulk of youtube links
---

How To Install on Ubuntu:

``` sh
sudo apt-get install youtube-dl
```

How To Use:

Simple Download

``` sh
youtube-dl <youtube-links>
```

Download spesific formats

``` sh
youtube-dl --list-formats <youtube-links>
```

the output sample usually like this:

    [youtube] vKtwZmhX0lw: Downloading webpage
    [youtube] vKtwZmhX0lw: Downloading video info webpage
    [youtube] vKtwZmhX0lw: Extracting video information
    [youtube] vKtwZmhX0lw: Downloading DASH manifest
    [youtube] vKtwZmhX0lw: Downloading DASH manifest
    [info] Available formats for vKtwZmhX0lw:
    format code  extension  resolution note
    171          webm       audio only DASH audio  113k , vorbis@128k (44100Hz), 1.86MiB
    140          m4a        audio only DASH audio  128k , m4a_dash container, aac  @128k (44100Hz), 2.14MiB
    141          m4a        audio only DASH audio  255k , m4a_dash container, aac  @256k (44100Hz), 4.30MiB
    278          webm       180x144    DASH video   63k , webm container, vp9, 1fps, video only, 946.76KiB
    160          mp4        180x144    DASH video  112k , avc1.4d400c, 15fps, video only, 1.86MiB
    242          webm       300x240    DASH video  170k , vp9, 1fps, video only, 2.50MiB
    133          mp4        300x240    DASH video  247k , avc1.4d400d, 25fps, video only, 4.11MiB
    243          webm       400x320    DASH video  288k , vp9, 1fps, video only, 4.07MiB
    13           3gp        unknown    small
    17           3gp        176x144    small ,  mp4a.40.2, mp4v.20.3
    36           3gp        320x240    small ,  mp4a.40.2, mp4v.20.3
    5            flv        400x240    small
    43           webm       640x360    medium ,  vorbis, vp8.0
    18           mp4        640x360    medium ,  mp4a.40.2, avc1.42001E (best)

Then if you want to download the spesific formats, choose it by typing the format code like this:

``` sh
youtube-dl -f <format code> <youtube-links>
```

Download with list of youtube links

``` sh
youtube-dl -a list-of-youtube-links.txt
```

Download the entire channel

``` sh
youtube-dl -f best -citw -v <url-of-youtube-channel>
```