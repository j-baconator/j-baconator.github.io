---
layout: post
title: How I Built this Blog with Jekyll Pt. I
author: Julie Bacon
date:   2018-08-02 11:00:00 -04:00
categories: code
image: "/assets/img/posts/code.jpg"
---

I’ve been toying with the idea of building my own blog for some time now. It’s always been one of those “why do today what you can put off 'til tomorrow”-esque things that’s been on my To-Do list since like, last December. Well I finally sat down, spent a couple of hours, and alas, the Technista blog was born.

And *you too* can code your own blog from scratch!

## Why Code a Blog?

Do you have a topic you’re passionate about? Do you want to start an online business making money in your sleep? Are you applying to colleges or job hunting and want to impress the eff out of those recruiters? Code your own blog, it’s a pretty badass thing to do if I do say so myself. Coding your own blog takes a little more work than a Content Manaegement Systems (CMS) like [wordpress](https://wordpress.org/) or [squarespace](https://www.squarespace.com/) but coding your own blog gives you the control over everything and is just overall more badass IMHO.

## TLDR; Get Set Up in 4 Lines of Code

I assessed various [static blog frameworks](https://www.netlify.com/blog/2017/05/25/top-ten-static-site-generators-of-2017/) such as Hugo and Gatsby and ultimately decided to go with [Jekyll](https://jekyllrb.com/) because it seemed to have a relatively low learning curve, a wide community of users, and it's integrated with [GitHub pages](https://pages.github.com/) for free hosting. In fact, I got the initial blog up in seconds. Yes literal seconds.

I set up my GitHub repository, which is named after my GitHub username [j-bacaonator.github.io](https://github.com/j-baconator/j-baconator.github.io)

In my terminal I run the following commands:
1. `gem install bundler jekyll`
2. `jekyll new myblog`
3. `cd myblog`
4. 	`bundle exec jekyll serve`

I navigate to `localhost:4000` in my broswer and vioala, I have a blog. ✨like magic✨.

Jekyll allows you to write your posts in [Markdown](https://daringfireball.net/projects/markdown/syntax) and uses the [Liquid templating language](https://github.com/Shopify/liquid/wiki).

## Deep-Dive: Setup and Installation

### Requirements
To run this project locally and to set up Jekyll, we'll need to install a few required technologies first. We call these dependencies. The dependencies in our case are the Ruby programming language and Bundler.

1. Open up Terminal.
2. Check if Ruby is already installed. Run `ruby--version` in the terminal.
3. If the latest version of Ruby isn't installed, go ahead and install it. I use [Homebrew](https://brew.sh/) as my package manager on my mac. `brew install ruby`
4. Next install Bundler with `gem install bundler`

### Create a Repository
1. Go to your Terminal.
2. Navigate to where you'd like the files to live. I.e. `cd Documents/Dev`
3. Initialize a new, empty git repository `git init PROJECT-NAME`
4. Go into the new directory that was created `cd PROJECT-NAME`

### Install Jekyll
1. Create a new file in your directory called "Gemfile" `touch Gemfile`
2. Open up the new file in your text editor. I use [Sublime Text](https://www.sublimetext.com/)
3. Add the following lines to your Gemfile
`source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins`
4. Install Jekyll `bundle install`

### Running the Project Locally
We want to run the project locally so that we can write code and preview the changes before we push updates to GitHub. In order to do so, we need the Jekyll site files on our local machine.





### Create New Jekyll Site
1. Open Terminal.
2. Navigate to where your development files live. For example, mine live in a Dev folder under my Documents. `cd Documents/Dev`
3. `gem install jekyll bundler`
4. `jekyll new PROJECT-NAME` where PROJECT-NAME is whatever you'd like the project to be called. This command tells jekyll to create a new jekyll site by installing any necessary files and dependencies in a folder called PROJECT-NAME. This is your project folder.
5. `cd PROJECT-NAME` 
6. You'll notice a bunch of new files in this folder that jekyll installed.


### Run the Project Locally
{% highlight ruby %}
1. `bundle exec jekyll serve --watch`
{% endhighlight %}

`​`` html
<a href="#">Hello world</a>
`​``

This command tells the computer to run the jekyll files. The --watch flag does exactly what it sounds like, it watches your files for changes and updated the browser whenever you save a change. Without this flag, you can still see the changes when you refresh the browser.

The server will continue running and watching your changes as you develop. To quit the server, press control-c. When you're ready to start it up again, simply run `bundle exec jekyll serve --watch`.

View your project running locally by opening up your web browser and going to `localhost:4000`. You'll see the basic Jekyll site with sample posts.


### Push the Code to GitHub
Congratulations, you just ran your blog locally! Now it's time for the fun part - putting it all on the Web for others to see.

In order to do this, we'll open the terminal back up and make sure we're in our website directory `PROJECT-NAME` We'll enter a few commands into the terminal:

1. `git add .` will add any and all file modifications
2. `git commit -m "initial jekyll site"` will commit our code changes. The -m flag signals that we have a commit message, which describes what changes we made. You can replace the "initial jekyll site" with any message you like, but keep it meaningful and brief.
3. `git push` will push the commit to Github.
4. Go to your repository on github.com and confirm that you see your commit!

