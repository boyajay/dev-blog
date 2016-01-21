---
layout: post
title: How to Host a Blog on Github in 15 Minutes 
---

This will be a guide on the easiest and fastest way to set up and host a blog on your github quickly and free! Jekyll is a open-source static site generator that you can store along with your posts on github. Here's a simple way set one up without touching the command line. You can use it right out of the box, or bling it out with some jQuery and Bootstrap.

### 1. Create a fork or clone repository from Jekyll-Now
You can go through the trouble to install and create your own [Jekyll blog](http://jekyllrb.com/docs/home/), or you can use Barry's Clark's [Jekyll-Now](https://github.com/barryclark/jekyll-now) and save yourself all troubles. You're reading this blog on a Jekyll-Now clone right now!

### 2. Under Settings, Rename the Repo: yourGithubName.github.io

This will be the same url that you and others will use to visit your blog. This repo name is your one freebie to host a site on github. It should look like below, with boyajay as my username.

![github repo](/images/githubio.png "an image title")  

### 3. Open up and fill out _config.yml and about.md

Create your local clone of the repo, and open _config.yml and about.md. This information will populate different parts of the website, so fill in what you can.

### 4. Add new blog posts in the folder _posts

That's it! Your blog is ready to go! By default, your blogs should follow the YEAR-MM-DD-Post-Name.md so that it formats correctly through the site generator. Use [this guide](http://www.jekyllnow.com/Markdown-Style-Guide/) to style your posts. But before you commit and push, maybe you want to test it?

### 5. See your site locally before you commit and push it

Ok, I lied a little bit. You technically don't need to preview your site, but if you do, you're going to have to use your command line to download the Jekyll gem. In the terminal, type "gem install Jekyll." Go to the root folder of your repo in the terminal, and type "jekyll serve" to host your blog locally. Finally, type the url "localhost:4000" into your web browser. 

### 6. Bling out your blog!

All the HTML files are found in the _layouts folder, and the style.scss in the root folder contains all the css content you want to change. Where you go from you is up to you.
