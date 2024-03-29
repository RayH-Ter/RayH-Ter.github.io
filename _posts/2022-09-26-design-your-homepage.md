---
title: Design Your Homepage
author: raymond
date: 2022-09-26 17:11:00 +0800
category: [Linux, Basis]
tags: [Jekyll, Homepage]
pin: false
mermaid: true
image:
  path: https://chirpy-img.netlify.app/commons/devices-mockup.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

## RayH-Ter.github.io

Personal website for something interesting

### Create your own homepage based on Github Page and Jekyll

1. Create a new repo named yourGithubName.github.io.
2. Create an index.html and start to edit this file to make you homepage look as pretty as you can.
3. Plenty of ready-made templates are avaviliable on [Jekyll Themes](http://jekyllthemes.org/). Just download one you like, and add files you downloaded to the repo you've created, then almost everything is done except filling in your own information and notes you'd like to show on your homepage.

### Install Jekyll

If you want to edit files offline and get the scene freshed as soon as possible, you are supposed to install Jekyll.

1. Install the dependencies for Jekyll on Ubuntu, refer [Jekyll on Ubuntu](https://jekyllrb.com/docs/installation/ubuntu)
2. Run `jekyll server`
```bash
jekyll server
# 如果报错则运行
bundle install
bundle exec jekyll serve
```

### Other reference

> [Jekyll on Ubuntu](http://jekyllrb.com/docs/installation/ubuntu/)
>
> [个人主页 — github + jekyll](https://blog.csdn.net/pentiumCM/article/details/106004574)
>
> [启动jekyll服务报错：Could not find gem 'github-pages'](https://dovesandy.github.io/2020/03/12/jekyll-start-jekyll-error/#1-前期准备)
>
> [Chirpy Jekyll Theme](https://github.com/cotes2020/jekyll-theme-chirpy)

### Advice

1. 在撰写具有大量公式的博客时，需注意公式的规范性，github上markdown行内公式容错性较Typora markdown低，且应搭载mathjax。
2. 调整博客文章主题可以套用平时Typora中.css文件

