---
layout: post
title: [How to blog in markdown using Github and Jekyll Now](https://howchoo.com/g/yzg0yjdmntl/how-to-blog-in-markdown-using-github-and-jekyll-now)
---

**by Tyler (216)Time to complete: 10 minutes**

<!-- TOC -->
- [1.Sign up for a Github account](#1sign-up-for-a-github-account)
- [2.Fork Jekyll Now and rename the repository](#2fork-jekyll-now-and-rename-the-repository)
- [3.Clone this repository to your local computer (optional)](#3clone-this-repository-to-your-local-computer-optional)
- [4.Customize the site in _config.yml](#4customize-the-site-in-_configyml)
- [5.Customize the About page](#5customize-the-about-page)
- [6.Write your first post](#6write-your-first-post)
- [7.Future blog posts](#7future-blog-posts)
- [8. Now it's time to master markdown](#8-now-its-time-to-master-markdown)
<!-- /TOC -->

I've wanted to start blogging again after a few years off. I was thrilled to find that I can blog using markdown in Vim and publish using git. This guide will show you how to use Github pages to set up a blog and how to publish your first post.

What you'll need:

||||
|:--|:--|:--|
|github	|×	|1	|
|git	|×	|1|	

# 1.Sign up for a Github account

If you don't already have a Github account, go ahead and sign up on http://github.com.

# 2.Fork Jekyll Now and rename the repository 

Go ahead and fork the [Jekyll Now](https://github.com/barryclark/jekyll-now) repository. To fork simply click the link, and find the button that says "Fork". If necessary, choose where you want to fork the repository.

Then rename the repository to:
```
yourgithubusername.github.io
```
# 3.Clone this repository to your local computer (optional)
This step is only required if you want to manage your blog from your local machine. Otherwise you can post directly from Github's site.

To clone the repository (unix), first go to the directory that you want to hold the repo. I usually put things like this in a folder in my home directory called Developer.
```sh
cd ~/Developer
```
Now type the following, replacing the variable with your Github username:
```sh
git clone git@github.com:{your github username}/{your github username}.github.io.git
```
For clarity, mine is:
```sh
git clone git@github.com:josephtyler/josephtyler.github.io.git
```
# 4.Customize the site in _config.yml
With the repository forked and renamed, now it's time to customize the details. To do this simply open up the file in the root level of the repo called _config.yml. You can edit this file right in Github or on your local machine if you've cloned the repository.

Read through the file and change out all of the necessary settings. This file let's you customize things like your name, site description, social media links, etc.
Here's an example:
```
#
# This file contains configuration flags to customize your site
#

# Name of your site (displayed in the header)
name: Your Name

# Short bio or description (displayed in the header)
description: Web Developer from Somewhere

# URL of your avatar or profile pic (you could use your GitHub profile pic)
avatar: https://raw.githubusercontent.com/barryclark/jekyll-now/master/images/jekyll-logo.png
```
# 5.Customize the About page
At this point you can customize or remove the About page.

To customize edit the file:
```
about.md
```
If you want to add other pages, you'll need to edit the navigation menu in:
```
_layouts/default.html
```
and add a link to the page you want to create. Following the example of the about page, and make your link point to:
```
{{ site.baseurl }}/page-name
```
and name the file:
```
page-name.md
```
You can simply copy the about.md file and change the name. At this point you'll need to commit your changes (and push).


# 6.Write your first post
You'll notice that the home page of your blog shows a post that you didn't write. The easiest way to write your first post is to edit this one.

You can find this post in:
```
_posts/2014-3-3-Hello-World.md
```
The construction of the filename is important. You'll first want to change to date to todays date using the format:
```
yyyy-mm-dd
```
And then you'll want to change the text "Hello-World" to whatever you are going to call your first post. You'll see that the "Hello-World" portion of the file name is what will be used as the permalink.

When you open this file to edit you'll notice a configuration at the top:
```
---
layout: post
title: You're up and running!
---
```
Keep the layout as post, but you can edit the title of the blog post. Below this is the body of the post written in markdown. You can edit this as you please.

In order to publish, you'll need to commit (and push).

# 7.Future blog posts
Future posts can be added by creating a new file using the same format as the previous step.
```
_posts/yyyy-mm-dd-Permalink-Title.md
```
After you finish your post, remember to commit to master.

If you're managing the blog from you computer, you'll need to commit and push.
```sh
git add .
git commit -am "Added a blog post."
git push origin master
```
# 8. Now it's time to master markdown
Now that you've got your blog set up and understand the basics, you can start blogging, but make sure to take full advantage of all the features of markdown.

https://guides.github.com/features/mastering-markdown/

---
[origin](https://howchoo.com/g/yzg0yjdmntl/how-to-blog-in-markdown-using-github-and-jekyll-now)
