---
layout: post
title:  "Extract a rar on Ubuntu"
date:   2017-07-15 14:14:00 +0200
categories: linux
---
# To extrat a .rar on Ubuntu we need :
## Install unrar-free & rar
```bash
sudo apt install rar
sudo apt install unrar-free
```
## Create a rar :
```bash
rar a file.rar file-to-compress
```
## Extract a rar :
```bash
unrar x file.rar
```
## Extract multiple rar :
```bash
for i in *.rar; do unrar x "$i"; done
```

[Sources](https://doc.ubuntu-fr.org/rar)
