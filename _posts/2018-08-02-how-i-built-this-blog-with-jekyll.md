---
layout: post
title: How I Built this Blog with Jekyll Pt. I
author: Julie Bacon
date:   2018-08-02 11:00:00 -04:00
categories: code
image: "/assets/img/posts/code.jpg"
---

Blogs are a great way to reach a niche audience about something you're passionate about. For me, I've always loved reading technology blogs, but often find them unrelatable, and most *definitely* not pink. When you "wish" something existed in the world, tech can play as an instrument in creating that thing and putting it infront of the massess.

I’ve been toying with the idea of building my own blog for some time now. It’s always been one of those “why do today what you can put off 'til tomorrow”-esque things that’s been on my To-Do list since like, last December. I finally stopped putting it off and decided to materialize this idea I've had into this fancy tech blog that I coded myself.

And *you too* can code your own blog from scratch!



## But Why Code a Blog?

Do you have a topic you’re passionate about? Maybe you want to start an online business making money in your sleep through a passive income stream. Or maybe you're applying to colleges or job hunting and want to impress the eff out of those recruiters. Code your own blog, because it’s a pretty badass thing to do. Coding your own blog takes a little more work than a Content Manaegement Systems (CMS) like [wordpress](https://wordpress.org/) or [squarespace](https://www.squarespace.com/) but it coding yourself gives you greater control over everything from functionality to look and feel, can be more performant, and is a great learning opportunity.

I assessed various [static blog frameworks](https://www.netlify.com/blog/2017/05/25/top-ten-static-site-generators-of-2017/) such as Hugo and Gatsby and ultimately decided to go with [Jekyll](https://jekyllrb.com/) because it seemed to have a relatively low learning curve, a wide community of users, and it's integrated with [GitHub pages](https://pages.github.com/) for free hosting. In fact, I got the initial blog up in seconds. Yes literal seconds.



## TLDR; Get Set Up in 4 Lines of Code

I set up my GitHub repository, which is named after my GitHub username [j-bacaonator.github.io](https://github.com/j-baconator/j-baconator.github.io)

In my terminal I run the following commands:
1. `gem install bundler jekyll`
2. `jekyll new myblog`
3. `cd myblog`
4. 	`bundle exec jekyll serve`

I navigate to `localhost:4000` in my broswer and vioala, I have a blog. ✨like magic✨.

Jekyll allows you to write your posts in [Markdown](https://daringfireball.net/projects/markdown/syntax) and uses the [Liquid templating language](https://github.com/Shopify/liquid/wiki).



## Deep-Dive: Setup and Installation

The previous section gives you an overview of just how fast it is to create and run a Jekyll blog. But of course, there are a few requirements we'll need if you don't already have them. Let's do a deep dive into this set up and installation process.


### Requirements
To run this project locally and to set up Jekyll, we'll need to install a few required technologies first. We call these dependencies. The dependencies in our case are the [Ruby](https://www.ruby-lang.org/en/) programming language and [Bundler](https://bundler.io/) which helps manage Ruby dependencies.

1. Open up Terminal.
2. Check if Ruby is already installed. Run the following command in Terminal:
	`ruby --version`
3. If the latest version of Ruby isn't already installed, go ahead and install it. I use [Homebrew](https://brew.sh/) as my package manager on my mac. With homebrew, I can run the following command in Terminal to install ruby:
	`brew install ruby`
4. Next install Bundler with
	`gem install bundler`



### Create a Repository on Github
1. Go to Github.com

2. Click "New Repository" button on Github sidebar
![New Repository on Github](/assets/img/posts/new-repo-1.png)

3. Give your repository a new name. For a portfolio site, you can use `your-username.github.io` for free hosting. I.e. my portfolio lives at a repo called j-baconator.github.io. Don't check the box to initialize with a README.
![Name your repository](/assets/img/posts/new-repo-2.png)



### Get our Jekyll Site Files Locally
We want to run the project locally so that we can write code and preview the changes before we push updates to GitHub. In order to do so, we need the Jekyll site files on our local machine.

In a new directory:
`bundle exec jekyll _3.3.0_ new jekyll-blog`

Navigate into the new directory:
`cd jekyll-blog`

In your text editor, open the Gemfile. Remove the line that looks like:
`gem "jekyll", "~> 3.7.3"`

While you're in the Gemfile, uncomment the line that says:
`gem "github-pages", group: :jekyll_plugins`

Initialize a new empty git repository
`git init`

Connect your local files to the remote repository we just created.
`git remote add origin https://github.com/username-or-organization/remote-repository-name`

Push all our code files to the repository on github.
`git push -u origin master`

When you open up the project in your text editor on your local, you'll see the new files we just generated.

Screenshot of code files generated from the Jekyll Install
![Screenshot of code files from Jekyll Install](/assets/img/posts/boilerplate.png)

Navigate to Github and you should see the same Jekyll files that were generated on our local.

![Files in our Repository on Github](/assets/img/posts/new-repo-3.png)


### Run the Project Locally
`bundle exec jekyll serve --watch`

This command tells the computer to run the jekyll files. The --watch flag does exactly what it sounds like, it watches your files for changes and updated the browser whenever you save a change. Without this flag, you can still see the changes when you refresh the browser.

The server will continue running and watching your changes as you develop. To quit the server, press control-c.

When you're ready to start it up again, simply run the serve command above.

View your project running locally by opening up your web browser and going to
_localhost:4000_ You'll see the basic Jekyll site with sample posts.

Jekyll site running locally at localhost:4000
![Jekyll site running locally](/assets/img/posts/jekyll-default.png)


#### Github Cheatsheet
1. `git add .` will add any and all file modifications
2. `git commit -m "initial jekyll site"` will commit our code changes. The -m flag signals that we have a commit message, which describes what changes we made. You can replace the "initial jekyll site" with any message you like, but keep it meaningful and brief.
3. `git push` will push the commit to Github.
4. Go to your repository on github.com and confirm that you see your commit!



#### Further reading:
- [Jekyll and Github Pages](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/)