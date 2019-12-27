---
title: Deploying Eleventy to GitHub Pages - another method
description: I used Eleventy to rebuild my website, and had a bit a headache getting it deployed...
date: 2019-12-31
layout: layouts/post.njk
---

I used Eleventy to rebuild my personal website, and had a bit a headache getting it deployed to GitHub Pages. 

There's not much guidance online. Jonathan Snook has written about [deploying an 11ty site to GitHub Pages](https://snook.ca/archives/servers/deploying-11ty-to-gh-pages) - but it felt a little daunting to me so I thought I'd try and cobble together a different approach that doesn't involve using Travis CI for the build. 

I'm very new to all of this so I'm not sure what's best, but here's how I ended up doing it - hopefully it's helpful, and I'd be interested to know if I could have done it better.

## 1 - Build locally and get everything on GitHub

Unlike Jonathan Snook's method, I built the site locally and published it to GitHub.

By default, Eleventy won't publish the local build to GitHub.

So I found .gitignore and removed this line:

```
_site/
```

That means the content of the local site (in the _site folder) gets pushed to GitHub.

## 2 - Set up GitHub Pages and set the build directory to /docs/

I set up GitHub Pages for the respository [as described here](https://guides.github.com/features/pages/).

For the 'Source', I picked the 'docs' folder in the master branch.

![GitHub Pages settings](/personal-site-11ty/img/github-pages-settings.png)

## 3 - Tell GitHub Pages I'm not using Jekyll 

GitHub Pages seemed to be getting confused that I wasn't using Jekyll (I was getting build error emails). So [as described here](https://help.github.com/en/github/working-with-github-pages/about-github-pages#static-site-generators) I added a blank file called .nojekyll. 

![Adding .nojekyll file](/personal-site-11ty/img/nojekyll.png)

## 4 - Change the 11ty output directory to /docs/

Nothing was working yet because Eleventy builds sites to the _site folder by default, whereas GitHub pages was looking for the /docs folder (see #2).

So I [followed the instructions here](https://v0-7-1.11ty.dev/docs/config/#output-directory) to change Eleventy's output folder. This is the relevant bit in eleventy.js:

```
dir: {
      input: ".", // was . //
      includes: "_includes",
      data: "_data",
      output: "docs" // was _site, I changed for github
    }
```

## 5 - Change the site prefix

Once I'd pushed everything to GitHub, the site appeared on GitHub Pages! But it looked like this:

![Adding .nojekyll file](/personal-site-11ty/img/eleventy-github-pages-site-prefix.png)

Links to my CSS, my .js file and images were broken. 

So [as described here](https://v0-7-1.11ty.dev/docs/config/#deploy-to-a-subdirectory-with-a-path-prefix), I headed back to eleventy.js and changed my site's path prefix to match my respository name. This is the relevant bit:

```
    pathPrefix: "/personal-site-11ty/",  
    // I un-commented this and updated it to try and make github pages work
```

## 5 - Change the path for images

That fixed a lot, but not my .js file or images. 

So I headed to base.njk and found the reference to the .js file. I added the URL prefix manually.

I.e. I changed this:
```
    <script src="/css/script.js" defer="defer"></script>
```
to this:
```
    <script src="/personal-site-11ty/css/script.js" defer="defer"></script>
```

For the images, I did a find and replace.

I found all instances of this:
```
/img/
```

and replaced them with this:
```
/personal-site-11ty/img/
```

That did the trick. 

It took a lot of time and Googling to figure out. I'm not at all sure if it's a sensible method but it worked for me. 






