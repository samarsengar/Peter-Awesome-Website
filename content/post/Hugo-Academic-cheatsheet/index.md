---
title: Hugo-Academic CheatSheet
author: Peter Tea
date: "2019-11-28T13:00:00Z"
categories:
  - Demo
tags:
  - Academic
  - Demo
  - Fun
authors:
  - admin
draft: no
featured: no
image:
  caption: 
  focal_point: ''
  placement: 2
  preview_only: no
lastmod: '2019-12-01T13:00:00Z'
subtitle: 'The basics of Hugo-Academic :boom:'
summary: The sparknotes for some awesome aesthetics.
geometry: margin = 1.75 cm
output:
  html_document:
    keep_md:true
---

## The lazy way to hugo-academic

This post is currently under construction. Here, I'll post some quick tips with navigating through using hugo-academic on ``R blogdown``.

# Table of contents
1. [Emoticons](Emoticons)
2. [Browser Icon](#Browser Icon)
3. [Quick Links](#Quick Links)
4. [Customize Dropdown Menu](#Drop menu)


# Emoticons <a name="Emoticons"></a>
[This site](https://www.webfx.com/tools/emoji-cheat-sheet/) provides a cheatsheet on available emoticons you can use like :relieved: or :see_no_evil:.

# Adding personalized icon on browser tab <a name="Browser Icon"></a>
![](tennis_icon.png)

On the top left of the image (the browser tab), I've added a customized image of a tennis ball. You can do the same with any image by going to this folder:

```
Themes --> hugo-academic --> static --> img 
```
You will see in this folder, there are three ``.png`` files named: ``icon-32.png``, ``icon-192.png``, and ``icon-512.png``. Go ahead and upload the same image 3x to this folder, and change their names to the above.


# Quick links to your slides, poster, code, datasets and more! <a name="Quick Links"></a>
In your preamble, you can specify the options:
``url_slides:``, ``url_poster:``, ``url_cite:``, ``url_code:``, ``url_video:``, ``url_Dataset:``, ``url_PDF:`` and ``url_project:`` if you wanted to add quick links to these documents on your posts. Just make sure these files are in the same directory as your post directory.

-- Peter you should add an image of this here.

# Adding icons to your "About Me" page

You can add cool icons that links to your email or other social media. In the image below, I have icons set up to my email, linkedin, github and instagram accounts.

Here's how to do it:
```
Content --> authors --> admin --> _index.md
```

In the preamble of this ``-index.md`` file, you will need to add an "icon" section that looks like this:


```
- icon: linkedin
  icon_pack: fab
  link: URL link
- icon: github
  icon_pack: fab
  link: URL link
- icon: instagram
  icon_pack: fab
  link: URL link
```


# Adding Resume to dropdown menu <a name="Drop menu"></a>

```
Config --> _default --> menus.toml
```



