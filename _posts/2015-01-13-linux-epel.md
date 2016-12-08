---
layout: post
title:  "How I started..."
date:   2016-12-8
desc: "How to create this blog site and why I started"
keywords: "blog,start"
categories: [Life]
tags: [FirstBlog,HowToBlog,jekyll]
icon: icon-centos
---

In the true nature of why I started this blog, I'm going to document how to get started.  But first, bare with me while I give you the "why I started doing this" memo...

So, I started this because I've been an engineer for all but 9 months now and have had my fair amount of struggles getting started.  Plus, I'm in a leadership position where I interview more experienced individuals and it seems like everyone has a site similar to this. And now, this is me giving back.  I'm going to document code I write, things I learn, and just general thoughts as I go.  Ok, thanks for sticking through this...

Here are the steps to create the site (I used a Mac so command lines may differ between platforms):

1. Create a GitHub account if you haven't already.  It's free, so no issue.
2. Create a new repository following this format: username.github.io
3. Clone the repository (where username is what you defined in step 2)
```
  git clone https://github.com/username/username.github.io
```
4. Fork/Clone the jalpc_jekyll_theme repository:
```
  $ git clone https://github.com/<your githubname>/jalpc_jekyll_theme.git
```
5. Navigate into the forked/cloned repository and download jekyll
```
  $ gem install jekyll bundler
```
6. Now copy the contents of the jekyll clone and put in the repository you created in step 1
7. Check in all the code and GitHub will host the site for you.

It's that simple.  Now have fun and customize to your needs.  Some tips:
* Blogs are stored in the `_posts` directory.
* Site html code (which really doesn't need to be touched unless you want to change it) is in the `_site` directory.
* All main page documentation is the `_config.yml` file
* If your main pages aren't taking place, I had to modify the html because it was pointing to a JSON file.  This was in the `_site/blog/index.html` file.
* To run and refresh your build locally, run `jekyll serve --watch`
