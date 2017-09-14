---
layout: post
title:  "Backup a Linux"
date:   2017-07-29 19:13:00 +0200
category: linux
---
# We will simply copy all files of the system in a tar
## First step log as root
```bash
 sudo su
 ``` 
## Here we could start the backup
```bash
tar cvpzf backup.tgz --exclude=/proc --exclude=/lost+found --exclude=/backup.tgz --exclude=/mnt --exclude=/sys --exclude=/media --exclude=~/Videos  /
```
## Then we just have to move the backup to an external disk
```bash
 sudo cp /backup.tgz /media/steven/Elements/
 ```