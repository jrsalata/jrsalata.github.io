---
title: "Creating This Blog"
date: 2024-11-26T00:52:49Z
draft: true
---

# The Beginning
So I never had the long-term plan of creating this website for myself. I remembered that I had an old repo using GitHub pages for a different project (TODO: Make that blog) that was no longer used.  It was filled with old code from high school that was not a good representation of my best work.  I wanted to delete it and put a placeholder in there.  However, I felt a particular desire to find a good way of making a static website since I disliked working with raw HTML/CSS/JS.  That is when I came across Hugo.

# Hugo
A Redditor once commented something along the lines of "Hugo is the front-end for back-end developers".  I am paraphrasing and couldn't find the exact source, but I wholeheartedly agree!  Hugo works by transforming markdown with other themes, templates, and content into HTML and CSS.  This makes it easy to style, develop, and write without having to worry about tags, formatting, or unexpected errors.  Written in Go, it is _extremely_ fast and lightweight.  Speed and size were not my main draws, but they were nice to haves for deployment.  \
Now, to be fair I did not look that deeply for different tools or solutions.  I took a look at Hugo and said "Ah, yes. That one".  However, I don't regret it at all.  It is an extremely easy to use tool once you learn the general structure of how it works.

# Theme Choices
Once I did the basic tutorial, I looked for a cool theme to use.  Afterall, I wanted this to be an extension of my personality and general nerdiness. [Risotto](https://github.com/joeroe/risotto/) was exactly what I was looking for.  It was stylish, minimal, and had a general nerdy vibe.  It displayed releveant information and made it extremely easy to find what a user would be looking for.  While other themes look more professional and offer more functionality, they weren't me.  I am not a fancy or flashy person. I prefer function over form almost any day of the week.\
I was also able to chose a theme pretty easily as Risotto supports the [base-16](https://github.com/chriskempson/base16) format which made swapping themes extremely easy.  I chose the [horizon-dark](http://github.com/michael-ball/) theme and modified it to contrast a bit better.  The result was this webpage you see now.

# Deployment
I am using [GitHub Pages](https://pages.github.com/) to host this site.  Previously, I stored everything in separate html files and wasn't sure how to deploy this Hugo project.  Everything by default was redirecting me to the README.md file in this repo.  I found an action on the GitHub Marketplace to deploy everything automatically without having to think about what I was doing.  Great!\
I ran the action and it reported that it successfully deployed. Hooray!\
Then when I checked on the site, it wasn't there.  Hmm.. odd. It said it deployed.  What could be going on?\
I did a bit more research and found another guide with a different file.  It was similar in a lot of places but had a few differnt version numbers and thought maybe something went wrong that the logs didn't show.  

# Final Thoughts
Overall, I went into this side project not really knowing what I was doing or how anything works.  In a way, I still don't.  However, I loved getting to learn this incredibly powerful tool