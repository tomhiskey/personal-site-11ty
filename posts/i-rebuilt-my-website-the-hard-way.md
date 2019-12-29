---
title: I rebuilt my website the hard way
description: Static site generators, Nunjucks, Git, Jekyll, Terminal, code editors... my knowledge of this sort...
date: 2019-12-29
layout: layouts/post.njk
---

Static site generators, Nunjucks, Git, Jekyll, Terminal, code editors... my knowledge of this sort of thing has been lacking. I thought I'd be a better designer if I knew about it, so I decided to rebuild my website (formerly in Wordpress) the hard way. 

## What I did

* Came up with a project to focus my efforts - rebuilding my personal website
* Updated my 10-year-old CSS knowledge by learning about CSS grids. [CSS Grid Garden](https://cssgridgarden.com/) was a fun way to learn the basics, then I messed around with it using Glitch ([here's my test site](https://gaudy-apostosaurus.glitch.me/blog.html)).
* Downloaded Visual Studio Code
* Using Terminal, I [installed Jekyll](https://jekyllrb.com/docs/installation/), a static site generator, and everything it needs (Ruby, etc). Jekyll seems to be the prevalent static site generator and a good place to start. 
* Ran through all of [this step by step Jekyll tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/) to learn the basics
* Switched to a different static site generator - [Eleventy](https://www.11ty.dev/) - because I understand from [Charlotte Dann](https://twitter.com/charlotte_dann?lang=en) that it's what the cool kids are using
* Downloaded the [Eleventy base blog](https://github.com/11ty/eleventy-base-blog) and began tinkering
* Copied the content from my Wordpress blog posts and used an online converter to change it to markdown (which is what Eleventy uses), then added the images manually
* Deployed my site to GitHub Pages, which [turned out to be quite tricky](/personal-site-11ty/posts/deploying-eleventy-to-github-pages-one-way)

☝️ All this took time and effort.

## The good stuff

* It was hard and I came across lots of minor problems - by solving them, I learnt a lot
* I loved the challenge and to be doing some proper (albeit very basic) coding - it's been a lot of fun
* Glitch was easy and fun
* I've ended up with a faster, better website 
* It's great to move away from Wordpress, which I've increasingly found to be slow, bloated and susceptible to hackers (not to mention it's very uncool for a designer's website)

## The bad stuff

* Using a code editor / Terminal / static site generator is such a unintuitive way to build a website - probably not worth it unless you want to learn how things work under the hood or you're already working in this way
* There's lots to remember, e.g. every time I load the project in Visual Studio Code I had to type "Eleventy --serve" into Terminal
* It's a shame I won't be able to write blog posts using my phone - I'll have to launch Visual Studio Code on my Mac every time I want to write something
* Git feels like a black box that I don't yet feel comfortable enough with
* It was painful trying to deploy my Eleventy site to GitHub Pages ([I've written about it here](/personal-site-11ty/posts/deploying-eleventy-to-github-pages-one-way))

![Building my website - Visual Studio Code](/personal-site-11ty/img/visual-studio-code.png)<em>The murky (but fun) world of code editors and Terminal - this is what I'm looking at while I write this blog post</em>

## Something I'd do differently

Eleventy and GitHub Pages don't slot together seamlessly, but it looks like [Jekyll and GitHub Pages do](https://help.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll). So if I was doing it all again I'd probably stick with Jekyll, particularly as for my meagre needs there seemed to be no discernible difference between that and Eleventy.

## Too Long Didn't Read

I'm glad I made the effort to rebuild my website the hard way. It was fun and I learnt a lot.
