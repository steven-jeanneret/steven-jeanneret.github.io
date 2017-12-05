---
layout: post
title:  "Markdown to PDF"
date:   2017-12-03 20:22:00 +0200
category: utilitaires
---

- [Prérequis](#pr%C3%A9requis)
- [Configuration des en-têtes](#configuration-des-en-t%C3%AAtes)
- [Génération du pdf](#g%C3%A9n%C3%A9ration-du-pdf)

# Prérequis
```bash
wget https://github.com/jgm/pandoc/releases/download/2.0.3/pandoc-2.0.3-1-amd64.deb
sudo dpkg -i pandoc-2.0.3-1-amd64.deb
sudo apt install ttf-mscorefonts-installer
sudo apt install texlive-full
```

# Configuration des en-têtes
```yaml
---
title: Titre du rapport
lang: fr
author: Steven Jeanneret
date: \today
papersize: a4
geometry: margin=3cm
toc: true
toc-depth: 5
documentclass: scrreprt
colorlinks: blue
mainfont: Times New Roman
---
```

> toc génère une table des matières jusqu'à 5 niveaux.
>
> documentclass permet d'utiliser un template

# Génération du pdf
```bash
pandoc rapport.md -o rapport.pdf
```