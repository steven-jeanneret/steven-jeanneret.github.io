---
layout: post
title:  "Use rouge on Jekyll for highlighting"
date:   2017-07-22 22:23:00 +0200
category: jekyll
---
# First we need to install kramdown and rouge

```bash
gem install kramdown rouge
```

# Then modify the _config.yml and add this
```bash
markdown: kramdown
highlighter: rouge
```

# Now we can generate a css file from a template
```bash
rougify style colorful > ./assets/tmp.css
```
I choose to take colorful but I have made a lot of change.
Then we need to copy the content of the file and add it to the scss of your site.

Note that Github have already rouge, when you push your modification it will work. This installation is only to saw the highlight localy.

[sources](https://benhur07b.github.io/2017/03/25/add-syntax-highlighting-to-your-jekyll-site-with-rouge.html)