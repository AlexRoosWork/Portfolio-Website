+++
title = "My Portfolio Website"
author = ["Alex Roos"]
publishDate = 2021-03-03
tags = ["emacs", "web"]
draft = false
+++

> [Check this website out on GitHub!](https://github.com/AlexRoosWork/Portfolio-Website)

## Working with Hugo through Doom Emacs and org-mode {#working-with-hugo-through-doom-emacs-and-org-mode}

A big fascination of mine has always been hosting websites. Being in full control over a site on the internet allows communication with the entire globe. Therefore, I began learning about webhosting.

Along my journey I discovered Hugo - a static site generator. Hugo uses markdown files to generate beautiful, lean webpages, which makes it ideal for blogs or a website like this.

Moreover, I am able to leverage other tools from my tech stack, namely [Doom Emacs]({{< relref "doom" >}}) and [org-mode](https://orgmode.org/). For those that don't know, org-mode is basically another markdown format. However, it is very feature rich. For instance, I can create codeblocks in any language and execute them within the file. Like this:

```sh
ls
```

```nil
#+RESULTS:
| alex-roos-website.org |
| archetypes            |
| config.toml           |
| content               |
| data                  |
| layouts               |
| readme.org            |
| resources             |
| static                |
| themes                |
```

Amazing, isn't it? I am getting carried away!

The package [ox-hugo](https://ox-hugo.scripter.co/) allows me to export my single `.org` file to Hugo, along with images, formatting etc. It creates markdown files in the appropriate directories for Hugo to reach.

## Making changes to the default settings {#making-changes-to-the-default-settings}

The `alex-roos-website.org` file provides basically all the content on the website, such as this article. But for the landing page, I have actually created a custom `layouts/index.html`.

Since the site is fairly light-weight I wrote some CSS inline. I know this is not something to do, but for my purposes here, it did the trick.

Nevertheless, I still need a custom `/static/style.css` sheet, to add a breakpoint on my portrait for small devices and to center the images in articles.

## Updating the website {#updating-the-website}

To update the website I use the `SPC m e H A` key chord in org-mode. This exports my file directly to my VPS. From there I simply `ssh` into the VPS, `rm -rf public/` and `hugo` to generate the new site based on the new markdown files. `hugo` generates the `public/` folder that [NGINX](https://nginx.org/en/) routes any requests to.

This ox-hugo export means I do not have to worry about image files being in the wrong location. It also generates the folder structure to bundle articles like [Thoughts](thoughts/.org) and [Projects](projects/.org).

Anyway, I'm a big fan.
