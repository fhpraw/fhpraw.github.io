---
layout: post
title:  "Useful Linux CLI"
date:   2018-06-09 20:41:00 +0700
categories: cli tutorial
description: a collections of useful cli in linux
---
show total size of filename or directory

```sh
du -sh filename
du -sh dirname
```

compress files into zip archive

```sh
zip archive.zip file0 file1 file3

# using regex
zip c_source.zip "*.[ch]"

# adding file into zip archive
zip -r archive.zip file4
```

extract zip file into directory

```sh
unzip archive.zip -d <destination dir>

# list filenames inside archive.zip
unzip -l archive.zip
```

compress file into tar archive

```sh
# into tar
tar -cvf archive.tar dirname

# into tar.gz or tgz
tar cvzf archive.tgz dirname

# into tar.bz2 or tbz
tar cvfj archive.tbz
```

uncompress tar archive

```sh
tar -xvf archive.tar -C destination_dir
tar -xvf archive.tgz -C destination_dir
tar -xvf archive.tbz -C destination_dir

# list content
tar -tvf archive.tar
```

play mp3 (need [vlc](https://www.videolan.org/))

```sh
nvlc file.mp3

# interactive player with random play
nvlc --random /path/to/your/mp3/folder

# no interface with random play
cvlc --random /path/to/your/mp3/folder
```