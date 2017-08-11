---
layout: post
title: Creating a Personal Blog Using Jekyll And Github Page
date: 2017-07-07
tags: Blog   
---

This is my first time building a personal blog and I have to admit, there were quite a few hassle at first. This blog will go through the steps I took have my personal blog site running, and also some of the issues I had during the process. So, let's begin. 

### Introduction

Jekyll is a simple, blog-aware, static site generator perfect for personal, project, or organization sites. 
Jekyll takes your content, renders Markdown and Liquid templates, and spits out a complete, static website ready to be served by Apache, Nginx or another web server. Jekyll is the engine behind GitHub Pages, which you can use to host sites right from your GitHub repositories.

Oh and yeah, it is FREE!

There are few things you need to do before you get started. First, make sure you are on a Windows because this tutorial is for Windows users only...

If you are on Windows, you need to make sure you have property setup [Git](https://git-scm.com/downloads), [Ruby](http://www.ruby-lang.org/en/downloads/) (Jekyll is based on Ruby), and [RubyGems](http://rubygems.org/pages/download) (A package manager for Ruby).

### Jekyll Environment Setup

Install jekyll

```     
$ gem install jekyll     
```    

Create a new blog

```    
$ jekyll new myBlog    
```   

Navigate to new blog directory

```
$ cd myBlog  
```

Run server locally

```
$ jekyll serve
```

And now go to <http://localhost:4000>，there you can see your personal blog!

![](/images/posts/jekyll/image1.png)

### Jekyll Directory Structure
　
Jekyll is, at its core, a text transformation engine. The concept behind the system is this: you give it text written in your favorite markup language, be that Markdown, Textile, or just plain HTML, and it churns that through a layout or a series of layout files. Throughout that process you can tweak how you want the site URLs to look, what data gets displayed in the layout, and more. This is all done through editing text files; the static web site is the final product.

I personally prefer Markdown so I'm gonna stick with Markdown in this tutorial. 

A basic Jekyll site usually looks something like this:


    ├── _config.yml
    ├── _includes
    |   ├── footer.html
    |   └── header.html
    ├── _layouts
    |   ├── default.html
    |   ├── post.html
    |   └── page.html
    ├── _posts
    |   └── 2016-10-08-welcome-to-jekyll.markdown
    ├── _sass
    |   ├── _base.scss
    |   ├── _layout.scss
    |   └── _syntax-highlighting.scss
    ├── about.md
    ├── css
    |   └── main.scss
    ├── feed.xml
    └── index.html


You could find out more about it ad [Jekyll Directory Structure](https://jekyllrb.com/docs/structure/) 

Go into _config.yml and try change some of the fields there, restart jekyll server, refresh browser, and now you can see the changes you just made.

### Github Page

First make sure you have a github account. Create a new repo named _yourAccountName_.github.io. For example my github account is called [rockthebesr](https://github.com/rockthebesr), my new github repo's name would be rockthebesr.github.io. Now push your changes to your newly created repo, open up your browser, go to username.github.io, and there you should see your blog up and running.

### Writing Posts

All blogs are under the directory __posts_, and they are all in markdown format. (like I said before, I prefer markdown)

Writing a new blog is simple, you can take a look at _post\2017-07-07-welcome-to-jekyll.markdown first to see how it is formatted. You could copy and paste that md file and write your new article based on that. Note: article names need to begin with 2016-10-31- etc.. It has to be YEAR-Month-Day. After that it's your article's name. 

At the top of the md, you will see 


    layout: post
    title:  "Welcome to Jekyll!"
    date:   2016-01-01 11:29:08 +0800
    categories: jekyll update


title: eh....title of your article.                    
date:  the date of your article (doesn't have to be today, can be any date)                        
categories: the category this article is in. 

If you are not too familiar with markdown, here is good [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)    

### Conclusion

Now you have just created your personal blog using Jekyll and Github page. But the blog might look... a bit simple, maybe overly simplistic. Well, once you are familiar with the environment and the tools, you could dive into [Jekyll Themes](http://jekyllthemes.org/). There are hundreds, if not thousands, or themes you could choose from. Pick anyone you like, as all of them should have their own little installation tutorial. Have fun!







