---
layout: post
title:  "Use the font Courier Prime on Jekyll"
date:   2017-07-15 14:34:00 +0200
category: jekyll
---
# Prerequisites
[Installation of Courier Prime on Ubuntu](/linux/2017/07/15/install-font-courier-prime.html)
# Add the file to the site folder
```bash
cp ~/Downloads/Courier\ Prime/*.ttf ./assets
```
# Modification of the base.scss
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
# Then push all on Github