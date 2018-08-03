---
layout: post
title: How I Built this Blog with Jekyll Pt. I
author: Julie Bacon
date:   2018-08-02 11:00:00 -04:00
categories: code
image: "/assets/img/posts/code.jpg"
---

I’ve been toying with the idea of building my own blog for some time now. It’s always been one of those “why do today what you can leave til tomorrow” -esk things that’s been on my “To Do” list since last December. Well I finally sat down, spent a couple of hours, and here we are! The Technista Blog was born.

And *you too* can code your own blog from scratch!

## Why Code a Blog?

Do you have a topic you’re passionate about? Do you want to start an online business making money in your sleep? Are you applying to colleges or job hunting and want to impress the eff out of those recruiters? Code your own blog, it’s a pretty badass thing to do if I do say so myself.


## Set Up in 4 Lines of Code

I assessed various static blog frameworks such as [xyz] and decided to go with [Jekyll](https://jekyllrb.com/) because it seemed to have a relatively low learning curve, a wide community of users, and it's integrated with GitHub pages for free hosting. In fact, I got the initial blog up in seconds. Yes literal seconds.

I set up my GitHub repository [j-bacaonator.github.io](https://github.com/j-baconator/j-baconator.github.io)
In my terminal I run the following commands:
1. `gem install bundler jekyll`
2. `jekyll new myblog`
3. `cd myblog`
4. 	bundle exec jekyll serve`

I navigate to `localhost:4000` in my broswer and vioala, like magic.

Jekyll allows you to write your posts in [Markdown](https://daringfireball.net/projects/markdown/syntax) and uses the [Liquid templating language](https://github.com/Shopify/liquid/wiki).