---
title: "My personal website"
date: 2022-04-03T23:51:55-04:00
draft: false
---

# Background
So, I've been wanting to make my own personal website for a while now, both for professional and personal reasons. (Theoritically, this was/is supposed to double as centralised place to see my projects, resume, and personal writings on my blog).

Hence, I've decided to create a little bit of a mini-guide/summary on how I got my personal website up; and hopefully If I've explained everything correctly you too can have your own nice slice of the internet dedicated to yourself, by the time you finish this tutorial!

## Theoritical aside - what's this website written in?
As you might've guessed from the watermarking at the bottom of the pages, this (static) website was made using Hugo; a very nice framework written in Go; Hugo makes creating a website a breeze. The various page files you'll find on my website are all written in markdown, which again thanks to Hugo is translated into HTML during "compile" time. It's worth mentioning that Hugo is a *static* website framework, meaning that what you, the end client sees, are my HTML files the way they're stored. There is no intermediatery fetching of data from some server - what you see is what you get.

In terms of the interesting backend stuff, this website is hosted on Netlify, based on my github respository that you can find here: [link]"https://github.com/TacitusKilgore/hugoWebsite". In short, everytime my github repository is updated, say using VSCode and git, my website is updated, very quickly. If you're lucky enough, you might be browsing in the middle of an update, to which you'd note the website briefly refresh.

## First step
