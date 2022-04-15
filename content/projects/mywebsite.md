---
title: "Building my personal website"
date: 2022-04-03T23:51:55-04:00
draft: false
---

# Background
So, I've been wanting to make my own personal website for a while now, both for professional and personal reasons. (Theoritically, this was/is supposed to double as centralised place to see my projects, resume, and personal writings on my blog).

Hence, I've decided to create a little bit of a mini-guide/summary on how I got my personal website up; and hopefully If I've explained everything correctly you too can have your own nice slice of the internet dedicated to yourself, by the time you finish this tutorial!

## Theoritical aside - what's this website written in?
As you might've guessed from the watermarking at the bottom of the pages, this (static) website was made using Hugo; a very nice framework written in Go; Hugo makes creating a website a breeze. The various page files you'll find on my website are all written in markdown, which again thanks to Hugo is translated into HTML during "compile" time. It's worth mentioning that Hugo is a *static* website framework, meaning that what you, the end client sees, are my HTML files the way they're stored. There is no intermediatery fetching of data from some server - what you see is what you get.

In terms of the interesting backend stuff, this website is hosted on Netlify, based on my github respository that you can find here: https://github.com/TacitusKilgore/hugoWebsite. In short, everytime my github repository is updated, say using VSCode and git, my website is updated, very quickly. If you're lucky enough, you might be browsing in the middle of an update, to which you'd note the website briefly refresh.

## First step (installation)
Now, first thing you'll need to do this, is download Hugo, git, and choclately if you're on windows. If you're a Mac or Linux user, sorry - but this tutorial won't be for you. Anyway, you can find and download the 3 at https://gohugo.io/, https://git-scm.com/, and https://chocolatey.org/. Also, make sure you're on an administrator when you run powershell, or your terminal of choice!

## Second step (setup)
Now that you've got git, hugo, and chocolatey setup, we now will actually set up the website. Using powershell or whatever terminal of choice you have, simply navigate to your directory of choice and type "hugo new site (your site name here) -f toml" to create a websites frame. This will be where all your files, config, etc will be placed. Note, you may opt to have a yml config file, but for this tutorial (and my website) I've opted to use toml. With that said and done, configuare your config.toml file properly. If you don't know how to do this, I'd recommend watching https://www.youtube.com/watch?v=hjD9jTi_DQ4&t=1032s (an excellent tutorial I've partially used), OR simply just copy paste a config file from a theme's github respository of your choice (this is typically okay, as most themes follow an MIT free use license.), of course for maximal freedom though, it's best to write your own config.

Anyway, it's time to pick a theme for your website. You can find a wide assortment of themes from https://themes.gohugo.io/ although my website as you might have seen at the bottom of the page, is running the https://themes.gohugo.io/themes/hermit/ theme.

Now, using git - you should find a command on the associated github respository of your chosen theme that will autoinstall your theme of choice to hugo. For exampole, the command for hermit's install is "git clone https://github.com/Track3/hermit.git themes/hermit". If everything has been done properly, you should see "your_themes_name" installed under the themes portion of your hugo files you created earlier with that "hugo new" command.

Finally, to test your website you can use the "hugo server" command in your terminal to create a locally hosted version of your website to check out how your (currently) blank website would look! (typically, this website should be found at localhost:1313 in your web browser.)

## Third step (adding stuff to your website)
I won't go over this part in too much detail and thus will just discuss how to add new text posts, and images to your website.

To create a new post in your chosen catergory, simply type in hugo new foldername/file_name.extension. For example, If I wanted to create a new markdown file in my blog folder, I'd type "hugo new blog/example.md" while in my hugo website directory. If you're feeling more creative and are familiar with html, I'd create your posts in .html for again better freedom, but since I don't plan on doing anything too crazy with this website, I'll just assume you're okay with writing stuff in markdown for now.

Anywho, assuming you've created your new sample_post.md, you'll notice that opening your file with VSCode or whatever IDE you're using will show an autoinserted header with a title, date, and draft status. If a file has draft state set to *true*, as you may have expected, it **WONT** show up on your website! set this to false in order to ensure your posts show up!

Otherwise, start writing your desired stuff (or if you don't know what the heck to write, I'd suggest reading up on how to use markdown - don't worry it's very easy!). 

Before I move on to the final stage, let's go ahead and cover how to upload images to your website. Now, in your same markdown file (or html file) corresponding to the the post you've made, ensure first and foremost that your image file is actually within your website's directory, and simply just type (assuming you're using markdown) '![image_text](image_path)'. 

NOTE: MAKE SURE THAT YOUR BASE URL IN YOUR CONFIG FILE IS THE SAME AS YOUR WEBSITE'S URL, OTHERWISE IMAGES WILL ONLY APPEAR ON YOUR LOCAL HOSTED SERVER, AND NOT YOUR LIVE WEBSITE! 

By the way, before moving on - please please please ensure you've properly configured your config file. 9/10 times, if something is not showing up on your website it's because you haven't included an appropriate path in your config file. For example, you'll notice the URL you're on should be hassanismail.ca/projects/mywebsite. I've attached an image below of my config.toml file, so you get an idea of what I mean:
![my config file](static/img/myconfigfile.png)
 
    

## Fourth Step (Setting your website up to go live!)



