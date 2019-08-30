--- 
layout: post
title:  Customizing  Your Jekyll Static Site
date:   2019-08-24 11:10:32 -0400
tags: jekyll static blog markdown css tutorial ruby git
categories: tutorial
comments: true
---

Now that we've got our basic Jekyll blog site [Jekyll Tutorial](/tutorial/2019/08/23/jekyll-tutorial.html),
we'll learn how to customize it to our liking. Please follow that tutorial to create a blog before proceeding.

First we need to locate our theme's folder on our computer

```bash 
bundle show minima # minima is the default theme
```

> /Users/username/.rbenv/versions/2.5.1/lib/ruby/gems/2.5.0/gems/minima-2.5.1

Customization works because Jekyll reads local files first before referencing theme files. 
So copy the files  you want to your project folder and edit as you please.

You can copy the complete directory, but then  you will not receive any updates to the theme.


See [jekyllrb](https://jekyllrb.com/docs/themes/#overriding-theme-defaults){:target="_blank"} for more details.