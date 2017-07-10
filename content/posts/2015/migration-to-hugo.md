+++
date = "2015-09-17T17:51:31+08:00"
description = ""
title = "Migration to Hugo"
slug = "migration-to-hugo"
aliases = [
    "migration-to-hugo"
]
tags = ["tech"]
+++

# Again?

I know, I know, I **JUST** migrated over to Ghost a few months ago. But no one really reads this anyway, so I don't think I'm offending that many people.

[Hugo](http://gohugo.io) is a Go based static site generator. Its really damn quick, and looks pretty good too! At first I thought [Ghost](https://ghost.org) would've been a good platform to work from.

But as it turns out, even though Ghost works really well, sorting out:

- Backend hosting requirements
- nginx
- npm dependencies
- Raspberry Pi/ARM issues
- Outside hackers trying to muscle in on my open port 80
- All the other things

It was too much effort. In the end I gave up and shut down the blog (then switch it on whenever I travel).

Hugo suits my purposes much better, since it spits out static pages, I can just throw it up on Github pages and just leave it there.

# Alternatives

[Jekyll](https://jekyllrb.com) was probably the main alternative to Hugo but it was Ruby based. Nothing wrong with that but I'm trying to learn more about Golang so why not use the closest competitor that was built entirely with Go?
