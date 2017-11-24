---
layout: post
title:  "Use the font Courier Prime on Jekyll"
date:   2017-07-15 14:34:00 +0200
category: jekyll
---
# Use Courier Prime on a site
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