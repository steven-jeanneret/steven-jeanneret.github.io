---
layout: post
title:  "Use the font Courier Prime on Jekyll"
date:   2017-07-15 14:34:00 +0200
category: jekyll
---

- [Install jekyll](#install-jekyll)
	- [Cloning the repository from git and finish installation](#cloning-the-repository-from-git-and-finish-installation)
- [Run jekyll](#run-jekyll)
- [Use Courier Prime on a site](#use-courier-prime-on-a-site)
	- [Prerequisites](#prerequisites)
	- [Generate all format](#generate-all-format)
	- [Place files on the site](#place-files-on-the-site)
	- [Modification of the base.scss](#modification-of-the-basescss)
		- [Import the files](#import-the-files)
		- [Use the font](#use-the-font)
	- [Then push all on Github](#then-push-all-on-github)
- [Use rouge on jekyll for highlighting](#use-rouge-on-jekyll-for-highlighting)
	- [First we need to install kramdown and rouge](#first-we-need-to-install-kramdown-and-rouge)
	- [Then modify the _config.yml and add this](#then-modify-the-configyml-and-add-this)
	- [Now we can generate a css file from a template](#now-we-can-generate-a-css-file-from-a-template)

# Install jekyll

```bash
sudo apt update
sudo apt upgrade
sudo apt install ruby ruby-dev gem zlib1g-dev

sudo gem install jekyll
sudo gem install bundle
```

## Cloning the repository from git and finish installation
```bash
git clone https://github.com/steven-jeanneret/steven-jeanneret.github.io.git
cd steven-jeanneret.io
bundle
```

# Run jekyll
```bash
sudo bundle exec jekyll serve --watch
```

# Use Courier Prime on a site
## Resources for fonts
[Resources of fonts that are free for commercial use](https://www.websiteplanet.com/blog/best-free-fonts/)

## Prerequisites
[Download Courier Prime](/linux/2017/07/15/install-font-courier-prime.html)

## Generate all format
[here](https://www.fontsquirrel.com/)

## Place files on the site
I put all the files in /asserts/font/

## Modification of the base.scss

### Import the files
```css
@font-face {
font-family: 'courierprime';
src: url('font/courierprime.eot');
    src: url('font/courierprime.eot?#iefix') format('embedded-opentype'),
         url('font/courierprime.woff2') format('woff2'),
         url('font/courierprime.woff') format('woff'),
         url('font/courierprime.ttf') format('truetype'),
         url('font/courierprime.svg#courierprime') format('svg');
font-weight: normal;
font-style: normal;
}

@font-face {
font-family: 'CourierPrime';
src: url('font/courierprimebold.eot');
    src: url('font/courierprimebold.eot?#iefix') format('embedded-opentype'),
         url('font/courierprimebold.woff2') format('woff2'),
         url('font/courierprimebold.woff') format('woff'),
         url('font/courierprimebold.ttf') format('truetype'),
         url('font/courierprimebold.svg#courierprime') format('svg');
font-weight: bold;
font-style: normal;
}

@font-face {
font-family: 'CourierPrime';
src: url('font/courierprimebolditalic.eot');
    src: url('font/courierprimebolditalic.eot?#iefix') format('embedded-opentype'),
         url('font/courierprimebolditalic.woff2') format('woff2'),
         url('font/courierprimebolditalic.woff') format('woff'),
         url('font/courierprimebolditalic.ttf') format('truetype'),
         url('font/courierprimebolditalic.svg#courierprime') format('svg');
font-weight: bold;
font-style: italic;
}

@font-face {
font-family: 'CourierPrime';
src: url('font/courierprimeitalic.eot');
    src: url('font/courierprimeitalic.eot?#iefix') format('embedded-opentype'),
         url('font/courierprimeitalic.woff2') format('woff2'),
         url('font/courierprimeitalic.woff') format('woff'),
         url('font/courierprimeitalic.ttf') format('truetype'),
         url('font/courierprimeitalic.svg#courierprime') format('svg');
font-weight: normal;
font-style: italic;
}
```

### Use the font
Add the 2 last lines at the code selector
```css
/*Near line 115*/
code {
  padding: 1px 5px;
  color :  white; 
  /*Adding font for the code part*/
  @import url("CourierPrime");
  font-family: "Courier Prime", "Courier New";
}
```
Courier New is here if Courier Prime can't be find!
## Then push all on Github

# Use rouge on jekyll for highlighting
## First we need to install kramdown and rouge

```bash
gem install kramdown rouge
```

## Then modify the _config.yml and add this
```bash
markdown: kramdown
highlighter: rouge
```

## Now we can generate a css file from a template
```bash
rougify style colorful > ./assets/tmp.css
```
I choose to take colorful but I have made a lot of change.
Then we need to copy the content of the file and add it to the scss of your site.

Note that Github have already rouge, when you push your modification it will work. This installation is only to saw the highlight localy.

[sources](https://benhur07b.github.io/2017/03/25/add-syntax-highlighting-to-your-jekyll-site-with-rouge.html)
